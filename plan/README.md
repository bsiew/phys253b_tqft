---
created_at: "2026-05-05T02:16:29-04:00"
updated_at: "2026-05-05T02:16:29-04:00"
generated_by: "codex"
timestamp_source: "agent_clock"
---

# Plan of Attack

This folder is the structured Brian/BSIEW planning mirror.

## Contents

- `plan_of_attack.tex`, review notes, and revision notes at the plan root
- `notes/` for claim ledgers, build notes, split decisions, and the
  2026-05-04 BSIEW migration plan
- `stages/` for stage summaries
- `tasks/` for granular task prompts
- `presentation/` for talk/rehearsal material

## Reconciliation notes

- Files pulled from the legacy Brian dump were moved here to match the original
  tree shape.
- Newer task/stage files that only existed in `tex_docs/bsiew_docs/` or
  `llm_docs/bsiew_plan/` were copied in so this folder is not missing the
  post-pull additions.
- Where the pulled dump and the current BSIEW task set disagree on a filename
  (notably `12_2_werkmeister_2025.md` vs `12_2_werkmeister_2024.md`), both
  copies were retained for provenance rather than guessing which label to
  delete silently.
- A small set of Chapter 11 task files was quarantined from `tex_docs` once the
  corresponding prose had already landed in `tex_docs/ch11_fqhe.tex`.
