# Task 1.10 - Build Route and Plan Scaffold

- **Status:** done (2026-05-03)
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)
- **Priority:** core

## Result

**Canonical compile route: Overleaf (browser-based), source lives locally.** Brian authors `.tex` files locally; Overleaf handles all compilation; tex files are the handoff medium between Brian and Helena.

Full route spec committed to [`plan/notes/build_route.md`](../notes/build_route.md).

### Key consequences for later tasks

- "Compile cleanly" means "Overleaf's `latexmk` compile produces a PDF with no error-level messages."
- No local-only `biber --validate-datamodel` is available; bib hygiene is confirmed by clean Overleaf compile.
- Claude / Codex cannot self-check compilation; Brian owns the Overleaf compile loop.

### Other deliverables

1. **Resolved the `claim_ledger.md` vs `verification_matrix.md` redundancy.** The canonical ledger is now `verification_matrix.md`, seeded with 10 claims from the Chapter 5 CS source. `claim_ledger.md` reduced to a 2-line pointer so task references still resolve. This also covers the seed step of Task 1.12.
2. **Added build-route pointers** to Tasks 14.4, 14.5, and 15.6 so "chosen build route" acceptance criteria anchor to `build_route.md`.
3. **Confirmed the `plan/notes/` and `plan/presentation/` scaffold** exist with their stubs.

## Goal

Make the plan executable in the actual repo: decide the canonical compile route and create the living `plan/notes/` and `plan/presentation/` directories that the rest of the plan already references.

## Steps

1. Decide the canonical compile route:
   - local TeX installation, if available;
   - shared Overleaf project;
   - or another remote/shared build workflow.
2. Record that decision in `plan/notes/build_route.md`.
3. Create these files if they do not exist:
   - `plan/notes/author_split_decisions.md`
   - `plan/notes/verification_matrix.md`
   - `plan/presentation/README.md`
4. Add one sentence to each later task that currently assumes `latexmk` or `biber`, pointing back to this build-route decision where needed.

## Acceptance criteria

- The compile route is written down.
- The `notes/` and `presentation/` directories exist and are not phantom references anymore.
- Later compile-related tasks have a clear source of truth for what "compile" means.

## Risks

- **Pretend-local tooling.** Do not keep writing acceptance criteria that assume local `latexmk` if the actual route is Overleaf or another shared build.
