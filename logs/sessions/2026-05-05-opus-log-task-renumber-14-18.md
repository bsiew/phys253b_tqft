---
created_at: "2026-05-05T18:51:12-04:00"
updated_at: "2026-05-05T18:51:12-04:00"
generated_by: "opus"
updated_by: "opus"
timestamp_source: "agent_clock"
project: "QFT"
log_type: "generated_session"
---

## Summary

Renumbered BSIEW task files to resolve the numbering collision between chapter-writing tasks and integration/presentation tasks. The old `14_*` (integration) tasks became `17_*`, the old `15_*` (presentation) tasks became `18_*`, and the new chapter-writing tasks dropped their `ch` prefix to claim the `14_*`, `15_*`, `16_*` namespace.

## Changes

### File renames

| Old name | New name | Scope |
|----------|----------|-------|
| `14_1_abstract.md` … `14_11_prose_pass.md` | `17_1_abstract.md` … `17_11_prose_pass.md` | Stage VI integration |
| `15_1_brian_board_script.md` … `15_7_submit.md` | `18_1_brian_board_script.md` … `18_7_submit.md` | Stage VII presentation |
| `ch14_1_theta_chi_u1a.md` … `ch14_4_qcd_caveats.md` | `14_1_theta_chi_u1a.md` … `14_4_qcd_caveats.md` | Ch 14 writing |
| `ch15_1_monopoles_line_operators.md`, `ch15_2_when_topological.md` | `15_1_…`, `15_2_…` | Ch 15 writing |
| `ch16_1_demonstrated.md` … `ch16_3_guide_du_routard.md` | `16_1_…` … `16_3_…` | Ch 16 writing |

### Internal reference updates

- `plan/stages/stage_VI_integration.md` — all task links and `#` column updated to `17.*`.
- `plan/stages/stage_VII_presentation.md` — all task links and `#` column updated to `18.*`.
- `plan/stages/stage_IVb_partII_crossdisciplinary.md` — task links updated to `14_*`/`15_*`; disambiguation section rewritten to reflect new scheme.
- All task file `# Task` headers updated to match their new number (e.g., `# Task 17.1`, `# Task 18.1`).

### Final numbering scheme

| Range | Content |
|-------|---------|
| `09_*` – `13_*` | Ch 9–13 writing (condensed-matter core) |
| `14_*` | Ch 14 writing (theta vacua, WV, axion, caveats) |
| `15_*` | Ch 15 writing (monopoles, taxonomy) |
| `16_*` | Ch 16 writing (outlook synthesis) |
| `17_*` | Stage VI integration (abstract, cross-refs, bib, figures, proofing) |
| `18_*` | Stage VII presentation (board scripts, rehearsal, submit) |

## Verification

- `grep -rl "ch14_\|ch15_\|ch16_"` returns no hits in the plan directory.
- All stage file links resolve to existing filenames.
- Task headers match their file numbers.
