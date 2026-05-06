---
created_at: "2026-05-02T18:46:50-04:00"
updated_at: "2026-05-02T18:46:50-04:00"
generated_by: "codex_gpt5"
model_detail: "Codex session; exact 5.x variant and reasoning effort are not exposed in this workspace transcript."
reasoning_effort: "not_exposed"
timestamp_source: "agent_clock"
project: "QFT"
log_type: "generated_session"
---

# QFT Doc Consolidation

## Scope

Cleanup pass for QFT docs, final-paper local copies, generated session logs,
research-report quarantine, and figure inventory consolidation.

## Changes

- Replaced final-paper pointer files in `llm_docs/current/` with full copies of
  QFT state files: writing context, writing pipeline, writing review, next
  actions, and figure inventory.
- Kept one metadata-bearing active copy of `Final QFT Project Overview.md` in
  `llm_docs/reference/` and quarantined duplicate overview logs.
- Quarantined duplicate research reports whose findings said no grounded
  findings were available.
- Merged QFT quick-reference and agent/architecture docs into root/QFT active
  guidance and archived the old separate files under
  `PROJECTS/QFT/docs/archive/merged_2026-05-02/`.
- Collapsed `figure_inventory.md` and `figure_wishlist.md` into one active
  seven-section-aware figure inventory.
- Relabeled active generated session logs from the old unknown model label to `claude_opus`
  where the provenance was known, and marked Codex logs with explicit
  model-unrecorded metadata where the exact model/reasoning was unavailable.

## Verification

- Confirmed state and final-paper `current/` copies match with `diff -q`.
- Confirmed active research-report folders no longer contain no-grounded reports.
- Confirmed no active `figure_wishlist.md` remains in `llm_docs/current/`.
- Confirmed active session logs no longer contain the old unknown model label.
