---
created_at: "2026-05-05T19:15:08-04:00"
updated_at: "2026-05-05T19:15:08-04:00"
generated_by: "opus"
updated_by: "opus"
timestamp_source: "agent_clock"
project: "QFT"
log_type: "generated_session"
---

## Summary

Created three automation scripts for the 253b final paper that dispatch Claude Opus instances to write LaTeX chapter content overnight without human intervention.

## Deliverables

1. **[run_paper_tasks_09_13.sh](scripts/run_paper_tasks_09_13.sh)** — Writes chapters 9–13 (25 tasks). Runs 2 Opus instances in parallel, each chapter sequential internally. Already running.
2. **[literature_pedagogy_pass.sh](scripts/literature_pedagogy_pass.sh)** — Post-writing pass: reads `literature/*/codex_paper_summary.md` to triage relevance, then uses full `codex_section_extracts/` to improve chapter pedagogy. Explicit instructions to NOT make prose more research-paper-like.
3. **[run_paper_tasks_14_16.sh](scripts/run_paper_tasks_14_16.sh)** — Writes chapters 14–16 (9 tasks: theta vacua/chi_t, eta-prime/WV, strong CP/axion, QCD caveats, monopoles/lines, four-category taxonomy, outlook). Ch 14 + Ch 15 parallel, then Ch 16 after.

## Architecture decisions

- **Parallelism capped at 2** to respect credit budget and avoid model throttling.
- **Sequential within chapters** because later sections reference earlier ones (e.g., §14.3 uses chi_t from §14.1).
- **Literature pre-loaded in prompts** (tasks 14–16 script): each task spec names relevant `codex_paper_summary.md` files, which are cat-ed directly into the prompt so the agent does not waste tokens finding them.
- **Pedagogy pass is separate from writing** — runs after content exists, makes surgical edits only.
- **set -e throughout** — scripts halt on first failure (credits exhausted, network error) rather than silently continuing with broken state.

## Logs

- Per-task logs: `logs/paper_tasks_09_13/<task_name>.log`, `logs/paper_tasks_14_16/<task_name>.log`
- Per-chapter pedagogy logs: `logs/literature_pedagogy/<chapter_name>.log`
- Master logs: `logs/overnight_full_run.log` or `logs/paper_tasks_14_16.log`

## Current state

- `run_paper_tasks_09_13.sh` is running (kicked off earlier this session).
- `run_paper_tasks_14_16.sh` ready to run; user will start it.
- `literature_pedagogy_pass.sh` ready to run after writing passes complete.

## Next actions

- Monitor `logs/paper_tasks_09_13.log` for completion.
- Start `run_paper_tasks_14_16.sh`.
- After both writing passes, start `literature_pedagogy_pass.sh` (covers ch09–ch13; can be extended to ch14–ch16 later).
- Review generated tex output for correctness once all scripts complete.
