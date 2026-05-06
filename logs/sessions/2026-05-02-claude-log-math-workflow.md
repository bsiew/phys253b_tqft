---
created_at: 2026-05-02T01:41:00-04:00
updated_at: 2026-05-02T01:41:00-04:00
generated_by: claude-code
timestamp_source: session
project: QFT
scope: math-workflow-implementation
log_type: "generated_session"
---

# Math derivation workflow implementation log

## Goal

Implement the plan from `~/Downloads/Agentic Workflow for Math.md`:

- Replace `/math-derive` with a thin wrapper that drives a Python workflow.
- Introduce `research_tools/math_runtime/` with models, classifier, Mathematica
  executor, adversarial checker, and artifact writer.
- Expose `research math-derive` on the CLI and add `--math off|auto|required`
  to `research run`.
- Insert a `math_derivation` node between `worker_pool` and `synthesizer` in
  the research runtime graph.
- Port Codex-equivalent safeguards from `AGENTS.md` into root `CLAUDE.md`.
- Quarantine the prompt-only `/deep-research` command to `_holding/`.
- Fix the stale `scripts/reading_list_intake.py` reference in
  `/ingest-citations` to the current `research_tools.agents.reading_list_intake`
  module.
- Cover the changes with unit and integration tests, and run a dry
  `math-derive` smoke command.

## Files changed

### Cleanup pass

- `.claude/agents/citation-list-intake.md`: replaced the dead
  `python scripts/reading_list_intake.py` invocations (both occurrences) with
  `python -m research_tools.agents.reading_list_intake`, matching the current
  module location.
- `.claude/commands/deep-research.md`: moved to
  `_holding/claude_commands_retired/deep-research.md`. Added
  `_holding/claude_commands_retired/README.md` documenting the replacement
  pathway (`./research run --effort-level deep ...` with optional `--math`).
- `CLAUDE.md`: appended a "Project-semantic safeguards" block that mirrors the
  key Codex rules from `AGENTS.md` (identify active project, read
  `state/project_state.yaml`/`current_stage.yaml`/`weights.yaml` before
  substantial planning, preserve project separation, log scope/weight/stage
  changes in `decision_log.md`, use full ISO-8601 timestamps with timezone in
  generated markdown front matter, keep root `state/` operational only, prefer
  small auditable edits).

### math_runtime package

- `research_tools/math_runtime/__init__.py`: public API surface.
- `research_tools/math_runtime/models.py`: dataclasses for
  `MathDerivationRequest`, `MathDerivationPlan`, `MathObjectFamily` enum,
  `MathRouting`, `SubagentTask`, `VerificationTest`, `VerificationResult`,
  `VerificationStatus` enum, `DerivationAttempt`, and `MathDerivationRunState`
  with `from_dict` / `to_dict` round-trippers.
- `research_tools/math_runtime/classifier.py`: keyword-regex classifier over
  seven specialized families plus a generic fallback. Returns the family, a
  `MathRouting` record naming primary/secondary packages and formula
  databases, and the scored runners-up.
- `research_tools/math_runtime/mathematica_executor.py`: wolframscript
  executor that probes once at construction and degrades gracefully when the
  engine is missing. Probe looks at the last non-empty line of stdout to skip
  Intel MKL warnings emitted by Wolfram. Default probe timeout is 30s so cold
  starts on macOS do not mark the engine as unavailable.
- `research_tools/math_runtime/checker.py`: `AdversarialChecker` that emits
  identity, numeric, limit, series, and structural tests in Wolfram Language.
  Uses `Cases[expr, _Symbol?(Context[#] === "Global`" &), Infinity]` to
  extract free symbols correctly rather than relying on `Variables`, which
  returned composite heads like `{Cos[x], Sin[x]}` for trig identities.
- `research_tools/math_runtime/artifacts.py`: `MathArtifactWriter` that lays
  files out under `PROJECTS/<PROJECT>/artifacts/math_derivations/<run_id>/`,
  emits the project-standard YAML front matter on `derivation_report.md`,
  serializes `request.json`, `plan.json`, `verification_results.json`,
  `subagent_tasks/<task>.md`, `verification/<test>.wl`, and
  `attempts/<attempt>.md`.
- `research_tools/math_runtime/workflow.py`: `MathDerivationWorkflow.run`
  pipeline: classify -> build plan -> emit subagent task -> run verification
  -> optionally write artifacts. Strategy suggestions are family-specific.

### CLI and runtime integration

- `research_tools/research_cli.py`:
  - Added `math-derive` subcommand with `--project`, `--problem`, repeated
    `--assumption` / `--convention` / `--context`, `--target-expression`,
    `--target-result`, `--verification-level {standard,adversarial}`,
    `--run-label`, `--write`.
  - Added `--math {off,auto,required}` and `--math-max-tasks` to `run`.
  - Added `_render_math_summary` for the stdout block.
- `research_tools/research_runtime/models.py`: added `math_policy` (default
  `auto`) and `math_max_tasks` (default 3) on `ResearchRequest`, and
  `math_runs: list[dict]` on `ResearchRunState` (round-tripped in
  `from_dict`).
- `research_tools/research_runtime/runtime.py`:
  - New constructor argument `math_workflow_factory` for dependency injection.
  - `_math_trigger_patterns` for auto-mode triggering (keywords like
    "derive", "verify", "show that", TeX markers, `=` followed by a number).
  - `_math_derivation` node executing after `worker_pool` and before
    `synthesizer`. Skips when `math_policy == "off"`. Skips in `auto` when no
    trigger matches and the classifier returns the generic family. Runs
    unconditionally when `math_policy == "required"`. Appends a trace entry
    every time and records a summary dict in `state.math_runs`. When a report
    is written, a `Finding` referencing the math artifact is injected into
    the research findings.
  - Completion script updated to advertise `math-derive`.

### Claude command

- `.claude/commands/math-derive.md`: now instructs the agent to invoke
  `./research math-derive ... --write`, consume the emitted artifact layout,
  author the actual derivation as `attempts/<attempt_id>.md`, and update the
  `derivation_report.md` summary section.

### Tests

- `tests/test_math_runtime.py`:
  - classifier routes tensor GR, QFT amplitudes, special functions,
    combinatorial, noncommutative, generic.
  - executor returns `VerificationStatus.UNAVAILABLE` with the probe reason
    when wolframscript is absent.
  - workflow writes every artifact (request/plan/results/report plus
    subagent_tasks, verification) under a temp root when `write=True`.
  - workflow does not write anything when `write=False`.
  - adversarial verification level emits limit/series/structural tests in
    addition to identity/numeric.
- `tests/test_research_cli_math.py`:
  - `--math` defaults to `auto` and accepts `off`/`auto`/`required`.
  - `math-derive` parser wires repeated `--assumption`, repeated
    `--convention`, target fields, and `--write`.
- `tests/test_research_runtime_math_node.py`:
  - node skipped when `math_policy="off"`.
  - node always runs when `math_policy="required"`.
  - node auto-triggers only on math-flavored questions, using a stub
    `MathDerivationWorkflow` with call-count instrumentation.

Every new test passes. `pytest` on the whole suite shows `39 passed, 1 failed`;
the single failure (`tests/test_writing_workflow.py::test_writing_plan_defaults_qft_to_outline_pack`)
is pre-existing and independent of this work. It fails because
`PROJECTS/QFT/state/writing_context.yaml` has `current_pack: "pedagogical_rewrite"`
which the `WritingWorkflow` correctly honors. The test's hard-coded expectation
of `"outline_architecture"` reflects a default that is no longer the project's
actual state. Flagging for a later fix; out of scope here.

## Smoke command

```
./research math-derive --project QFT --problem "Verify Sin[x]^2 + Cos[x]^2 = 1 for real x" \
  --assumption "Element[x, Reals]" --target-expression "Sin[x]^2 + Cos[x]^2" \
  --target-result "1" --verification-level standard --write
```

Result: `run_id=math-20260502T054130-34919e0d`, `verification=passed`,
`mathematica_available=true`, both the symbolic identity test and the numeric
random-point test returned `True`. Artifacts written at
`PROJECTS/QFT/artifacts/math_derivations/math-20260502T054130-34919e0d/`.

## Design decisions

- Classifier is keyword-regex, not embedding-based. For HEP/GR/math the object
  signals are crisp and an auditable deterministic router is easier to reason
  about than nearest-neighbor. Embeddings can be added later as a tiebreaker
  without changing the interface.
- Workflow does not perform LLM-driven derivation. Its output is a
  verifiable plan plus the Wolfram tests. Actual derivation authoring happens
  either inside the slash command (Claude writes the `attempts/*.md` file) or
  in a future subagent that reads the emitted `subagent_tasks/*.md`.
- Mathematica executor degrades to `UNAVAILABLE` rather than raising. This
  lets CI and machines without Wolfram still produce the plan, routing, and
  subagent task artifacts; only the verification claim is withheld.
- Numeric test extracts symbols via `Cases[..., _Symbol?(Context[#] === "Global`" &), Infinity]`
  instead of `Variables[...]`. The latter returns composite heads like
  `{Cos[x], Sin[x]}` for a trig expression, which produced bogus False
  verifications on the first live run.
- Probe timeout is 30s (not the original 5s) because wolframscript cold-start
  on macOS can take several seconds. Probe looks at the last non-empty stdout
  line to ignore the Intel MKL warning that Wolfram emits on newer Intel
  builds; the first attempt with `stdout.strip() == "2"` failed because of
  this noise.
- `math_policy="auto"` default on `research run`: the node only fires when a
  math trigger is present or the classifier picks a non-generic family.
  `required` guarantees the node runs at least once per research job;
  `off` disables the node entirely.

## Remaining risks / followups

- `WritingWorkflow` test assumes an outdated default writing pack. Not in
  scope here; flag it the next time writing workflow is touched.
- The math node currently injects at most one `Finding` per research run. If
  the research question contains multiple independent math subproblems, the
  node still runs a single workflow invocation. The `--math-max-tasks` flag
  is wired through but not yet consumed; a future iteration can split the
  question and run several derivations in parallel.
- Package-specific routing is advisory. The workflow does not yet call
  FeynCalc or xAct programmatically; it names them in the plan for the
  human/agent author. A direct FeynCalc/xAct executor is a natural next
  layer.
- The `simplify` skill was not invoked here; a follow-up pass can look for
  duplication between `mathematica_helpers.py` (legacy ad hoc verifier) and
  the new `math_runtime` executor. They can coexist for now because
  `mathematica_helpers.py` has additional domain helpers (Wick rotation,
  Feynman parameter, dim-reg) that are not yet ported.
- Claude subagents pointed at Bedrock will incur cost if the `/math-derive`
  agent is ever written with `model: inherit`. It currently delegates to the
  Python CLI, so the LLM cost stays in the main conversation turn that
  invokes `/math-derive`, not in a subagent.
