---
created_at: "2026-05-04T18:14:24-04:00"
updated_at: "2026-05-04T18:14:24-04:00"
generated_by: "opus"
timestamp_source: "agent_clock"
project: "QFT"
log_type: "generated_session"
---

## Session: BSIEW Integration — Part II Restructure

### Decision
Reversed the structural assumption from the previous session: the BSIEW 14-chapter plan is the **target** structure, not legacy. The current 7-section observable-family organization is being migrated into it.

**Key structural choices made:**
- Adopt BSIEW Ch 9–13 for the condensed-matter core (topological order, anyons, FQHE, experiments, TQC)
- Graft current Secs 6–7 as new Ch 14 (QCD topology / strong CP / axions) and Ch 15 (monopoles / line operators / four-category taxonomy) — these have no BSIEW precursor
- Add Ch 16 (Outlook and Synthesis) absorbing the guide du routard from old Sec 7.3
- Defer Part I integration; make Ch 9 §9.4 a self-contained BF mini-derivation to remove the dependency on Part I Ch 6
- Through-line updated from "three touchstones (Frobenius, CS, DW)" to "ordinary QFT → CS isolates → TQFT formalizes → observable families organize"

### Files Changed

**Archive (9 files copied):**
- `tex_docs/archive_2026-05-04_pre_bsiew_integration/` — snapshot of all pre-integration .tex and .bib files

**New chapter files (8 created):**
- `tex_docs/ch09_topological_order.tex` — Ch 9, ~8 pp, Helena. Self-contained BF in §9.4
- `tex_docs/ch10_anyons.tex` — Ch 10, ~10 pp, Joint. Modular S-matrix derivation in §10.3
- `tex_docs/ch11_fqhe.tex` — Ch 11, ~10 pp, Helena. **Major migration**: all drafted content from part2_05 preserved verbatim and restructured into 7 BSIEW-aligned subsections
- `tex_docs/ch12_experiments.tex` — Ch 12, ~10 pp, Helena. Adds §12.4 (Bartolomei shot-noise, new)
- `tex_docs/ch13_tqc.tex` — Ch 13, ~8 pp, Helena. Adds §13.4 (TQC outlook, new)
- `tex_docs/ch14_sectors_3plus1d.tex` — Ch 14, ~15–20 pp, Helena. Copied from part2_06, renumbered
- `tex_docs/ch15_defects_synthesis.tex` — Ch 15, ~12–15 pp, Helena. Copied from part2_07, guide du routard removed
- `tex_docs/ch16_outlook.tex` — Ch 16, ~4 pp, Joint. Guide du routard migrated here

**Main wrapper updated:**
- `tex_docs/tex_docs_main_wrapper_20260501.tex` — Part II inputs changed to ch09–ch16

**Plan and stage files (5 edited, 1 created):**
- `llm_docs/bsiew_plan/migration_plan_2026-05-04.md` — comprehensive 9-section migration plan (CREATED)
- `llm_docs/bsiew_plan/stage_IV_partII_A.md` — integration notes added
- `llm_docs/bsiew_plan/stage_V_partII_B.md` — integration notes added
- `llm_docs/bsiew_plan/stage_VI_integration.md` — through-line and audit updated
- `llm_docs/bsiew_plan/stage_IV_B_partII_cross_disciplinary.md` — new stage for Ch 14–15 (CREATED)
- `BSIEW_README.md` — Stage IV-B added, through-line updated, task listings updated

**New task files (11 created in `tex_docs/bsiew_docs/`):**
- `11_5b_k_matrix.md`, `11_6_maxwell_cs.md`, `12_4b_bartolomei_shot_noise.md`, `13_4_tqc_outlook.md`
- `14B_1_theta_chi_u1a.md`, `14B_2_eta_prime_wv.md`, `14B_3_strong_cp_axion.md`, `14B_4_qcd_caveats.md`
- `14B_5_monopoles_line_operators.md`, `14B_6_when_topological.md`, `16_1_outlook_demonstrated.md`

### Open Threads
- Part I integration deferred: Ch 2–4 (math toolkit), Ch 5 (CS reorganization), Ch 6–8 (BF/DW/gen sym) still need structural decisions
- Ch 11 is the most-drafted chapter; writing priority order is Ch 11 → 9 → 12 → 10 → 13 → 14 → 15 → 16
- Compiled literature file from the plan still needs to be written
- Old part2_05/06/07 files should be quarantined to `_holding/` after verifying all content migrated
