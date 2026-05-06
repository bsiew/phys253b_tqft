---
created_at: "2026-05-05T17:39:19-04:00"
updated_at: "2026-05-05T22:39:17-04:00"
generated_by: "claude-code"
updated_by: "us.anthropic.claude-opus-4-6-v1"
timestamp_source: hook
---
# Completed Work Guide

What was archived here and where the outputs live.

## Stage I — Scope Freeze (all acceptance criteria met)

| Archived task | Output location | Remaining work |
|---|---|---|
| 01_2 Author split walkthrough | `plan/notes/author_split_decisions.md` | None; file exists but is sparse. Add entries if ownership changes. |
| 01_3 MTC ownership | Implicit in ch10 header (Brian: 10.3-4, Helena: 10.1-2, 10.5) | None. |
| 01_12 Claim ledger | `plan/notes/verification_matrix.md` | Seeded with Ch 2 + Ch 5 claims. Append new claims as chapters get proofread (Stage VI task 14.9). |

Other Stage I tasks (1.1, 1.4–1.10) had no standalone task files in the plan but are done:
- Outline v3: superseded by the ch09–ch16 chapter structure.
- main.tex skeleton: `tex_docs/tex_docs_ch02_ch13_app_e_wrapper_20260505.tex`.
- Merged bibliography: `tex_docs/tqft_observables_unresolved_refs.bib` (545 lines; 7 placeholder keys remain — resolve during task 14.5).
- Shared preamble: in the compile wrappers.
- Figure directory + checklist: `tex_docs/figures/` (12 TikZ files) + `llm_docs/current/figure_inventory.md`.
- Build route: `scripts/compile_253b_tex_to_artifacts.sh`.

## Stage III — Part I Math B (Ch 6 BF, Ch 7 DW, Ch 8 Gen Sym)

| Archived task | Output location |
|---|---|
| 08_7 CM inflow example | `tex_docs/ch08_gensym.tex` §8.7 (881 lines total, 0 TODOs) |
| 08_8 SymTFT one-page | `tex_docs/ch08_gensym.tex` §8.8 |
| 08_9 Scope guard | Chapter is within budget |

Full chapters drafted: `ch06_bf.tex` (806 lines), `ch07_dw.tex` (684 lines), `ch08_gensym.tex` (881 lines). All 0 TODOs.

## Stage IV — Part II Applications (Ch 9, 10, 11)

| Archived task | Output location |
|---|---|
| 09_1–09_5 | `tex_docs/ch09_topological_order.tex` (368 lines, self-contained BF insert in §9.4) |
| 10_1–10_5 | `tex_docs/ch10_anyons.tex` (841 lines, comparison table in §10.5) |
| 11_1–11_4 | `tex_docs/ch11_fqhe.tex` §11.1–11.4 (migrated from part2_05) |

Ch 11 §11.5–11.7 completed (written during 14–16 wave; archived 2026-05-05):
- `11_5_honesty_box.md` → §11.7 written (platform status block + closing paragraph, ~40 lines)
- `11_6_maxwell_cs.md` → §11.6 written (Maxwell–CS action, topological mass, crossover, 75 lines)

## Stage V — Experiments + TQC (Ch 12, 13)

| Archived task | Output location |
|---|---|
| 12_1–12_4b | `tex_docs/ch12_experiments.tex` (349 lines, includes Bartolomei §12.4) |
| 13_1–13_4 | `tex_docs/ch13_tqc.tex` (531 lines, experimental status in §13.3) |

## Stage overview files archived

- `stage_I_scope_freeze.md` — all criteria met.
- `stage_III_partI_B.md` — all chapters drafted.
- `stage_IV_partII_A.md` — all chapters drafted.
- `stage_V_partII_B.md` — all chapters drafted.

## Part I chapters (Stage II) — no task files existed in plan/tasks/

These were specified only in `plan_of_attack.tex`. All drafted:
- `ch02_forms.tex` (781 lines), `ch03_axiomatic.tex` (491 lines), `ch04_frobenius.tex` (864 lines).
- `chern_simons_body.tex` (1780 lines) — the anchor.
- Task 5.1 (Witten-Jones bridge) was NOT implemented. `ch05_chern_simons.tex` is a 16-line wrapper only. Decide whether to write the bridge or explicitly cut it.

## llm_docs/current/ files archived to `llm_docs/archive/current_pre_2026-05-05/`

| File | Why archived |
|---|---|
| REORGANIZATION_STATUS.md | Describes the old 7-section structure from May 2; superseded by the May 4 migration to ch09–ch16. |
| content_mapping_2026-05-01.md | Source routing for the old 7-section plan; active routing now lives in `migration_plan_2026-05-04.md`. |
| next_actions.md | Priorities reference old §5.5/§2/§3 numbering; stale. |
| writing_pipeline.md | References the pedagogical_rewrite pack from the old modular-TeX pass. |
| writing_review.md | Summarizes the Brian CS review integration pass — that work is done. |
| writing_context.yaml | Describes old modular TeX integration scope. |

## Stage VI — Part II Applications (Ch 14, 15, 16)

Completed 2026-05-05 via `scripts/run_paper_tasks_14_16.sh` (parallel Opus spawns).

| Archived task | Output location | Notes |
|---|---|---|
| 14_1 Theta vacua, χ_t, U(1)_A | `tex_docs/ch14_sectors_3plus1d.tex` §14.1 | 0 TODOs |
| 14_2 η′ mass, Witten–Veneziano | `tex_docs/ch14_sectors_3plus1d.tex` §14.2 | 0 TODOs |
| 14_3 Strong CP, nEDM, axion | `tex_docs/ch14_sectors_3plus1d.tex` §14.3 | 0 TODOs |
| 14_4 QCD caveats / iffiness | `tex_docs/ch14_sectors_3plus1d.tex` §14.4 | 0 TODOs |
| 15_1 Monopoles, line operators | `tex_docs/ch15_defects_synthesis.tex` §15.1 | 1 residual TODO (minor) |
| 15_2 Four-category taxonomy | `tex_docs/ch15_defects_synthesis.tex` §15.2 | |
| 16_1 What this paper demonstrated | `tex_docs/ch16_outlook.tex` §16.1 | 0 TODOs |
| 16_2 Open directions | `tex_docs/ch16_outlook.tex` §16.2 | 0 TODOs |
| 16_3 Guide du routard | `tex_docs/ch16_outlook.tex` §16.3 | 0 TODOs |

Line counts post-completion: ch14 (596), ch15 (244), ch16 (133). Total: 973 new lines.

Ch 11 §11.5–11.7 completed (written during 14–16 wave; archived 2026-05-05):
- `11_5_honesty_box.md` → §11.7 written (platform status block + closing paragraph, ~40 lines)
- `11_6_maxwell_cs.md` → §11.6 written (Maxwell–CS action, topological mass, crossover, 75 lines)

## Stage VI — Integration Pass (Tasks 17.x)

Completed 2026-05-05 via `scripts/run_paper_tasks_17.sh` (4 waves).

### Wave 0 — Structural Surgery

| Task | What was done |
|---|---|
| 0a Kill ch05 forms rehash | Replaced ~250-line forms section in ch05 with compact convention-recall paragraph referencing ch02 |
| 0b BF/toric-code cross-refs | Added reader's note in ch09 §9.4, cross-reference in ch07 §DW at line 580 |

### Wave 1 — New Content

| Task | Output |
|---|---|
| 17_1 Abstract | Written (top of paper) |
| 17_2 Introduction | Written (ch01 or equivalent) |
| 17_6 Chapter glue | Transition paragraphs added between all chapters |
| 17_7 Figure generation | TikZ figures updated/created |

### Wave 2 — Proofreading

| Task | Output |
|---|---|
| 17_9 Math proof pass | `logs/paper_tasks_17/17_9_math_findings.md` — fixes applied in-place |
| 17_10 Physics proof pass | `logs/paper_tasks_17/17_10_physics_findings.md` — fixes applied |
| 17_4 Cross-references | `logs/paper_tasks_17/17_4_crossref_fixes.md` — broken refs resolved |
| 17_5 Bib consolidation | `logs/paper_tasks_17/17_5_bib_summary.md` — duplicates merged |

### Wave 3 — Style & Voice

| Task | Output |
|---|---|
| 17_11 Prose pass | All banned phrases at 0 count; AI-tell purge complete |
| 17_12 Decontamination | "Honesty box" → neutral headings; throat-clearing killed across all chapters |
| 17_13 Style overhaul | Chapter openings rewritten as physical questions (Tong/Brennan-Hong style); transitions fixed |

### Standalone

| Task | Output |
|---|---|
| 17_8 Core-deliverables audit | `logs/paper_tasks_17/17_8_audit_report.md` — 15 PASS, 4 PARTIAL, 1 FAIL (ch08 §8.7 CM inflow) |

Also archived: `01_11_figure_policy.md` (policy superseded by overwrite-all-figures directive).

---

Still active in `llm_docs/current/`:
- `migration_plan_2026-05-04.md` — current chapter map + writing priorities.
- `figure_inventory.md` — active figure tracker.
- `figure_specs/` — specs for the 4 blocked hand-drawn figures (now being overwritten by script-generated TikZ).
- `writing_style_guide.md` — still-applicable prose rules.
