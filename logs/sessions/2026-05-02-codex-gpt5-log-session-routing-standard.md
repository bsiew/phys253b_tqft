---
created_at: "2026-05-02T18:16:10-04:00"
updated_at: "2026-05-02T18:16:10-04:00"
generated_by: "codex_gpt5"
model_detail: "Codex session; exact 5.x variant and reasoning effort are not exposed in this workspace transcript."
reasoning_effort: "not_exposed"
timestamp_source: "agent_clock"
project: "QFT"
log_type: "generated_session"
---

# Session Routing Standard

## Scope

Standardized generated session logs for QFT and the 253b final-paper nested git
repository.

## Changes

- Added shared `research log-session` CLI support through `research_tools/session_logs.py`.
- Documented canonical generated session log routing in root `logs/README.md`.
- Updated root, template, QFT, and Claude/Codex-facing guidance to use
  `PROJECTS/<PROJECT>/logs/sessions/` first and mirror nested deliverables.
- Migrated existing QFT/final-paper generated session records into standardized
  filenames in `PROJECTS/QFT/logs/sessions/`.
- Mirrored the same standardized logs into `PROJECTS/QFT/253b_final_paper/llm_docs/logs/`.
- Archived old nonstandard filenames under `llm_docs/archive/nonstandard_session_logs/`
  or `PROJECTS/QFT/logs/archive/nonstandard_session_sources/`.
- Replaced `PROJECTS/QFT/docs/MATHEMATICA_SETUP.md` with a pointer and added
  `PROJECTS/QFT/docs/TOOLING.md` as the consolidated math/tooling note.
- Mirrored `PROJECTS/QFT/state/next_actions.md` into
  `PROJECTS/QFT/253b_final_paper/llm_docs/current/next_actions.md`.

## Verification

- `python3 -m py_compile research_tools/session_logs.py research_tools/research_cli.py research_tools/research_runtime/runtime.py`
- `./research log-session --help`
- `./research completion zsh`
- `diff -q PROJECTS/QFT/state/next_actions.md PROJECTS/QFT/253b_final_paper/llm_docs/current/next_actions.md`
