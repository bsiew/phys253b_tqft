# Stage III - Part I Mathematical Buildup B

**Duration:** 1.5 days (target: Day 3 through Day 4).
**Lead:** Brian.

## Objective

Write Chapters 6, 7, and 8: BF theory, Dijkgraaf-Witten theory, and generalized symmetries with anomaly inflow. Chapter 5 (Chern-Simons) is already written and sits in between these.

## Tasks

### Chapter 6 - BF Theory (~6-8 pp)

| # | Task | File |
|---|---|---|
| 6.1 | Draft §6.1 (action, equations of motion, observables) | [06_1_bf_action.md](../tasks/06_1_bf_action.md) |
| 6.2 | Draft §6.2 (compact BF <-> $\mathbb{Z}_N$ gauge theory) | [06_2_bf_to_ZN.md](../tasks/06_2_bf_to_ZN.md) |
| 6.3 | Draft §6.3 (Wilson/'t Hooft linking number, parallel to CS abelian calc) | [06_3_linking_number.md](../tasks/06_3_linking_number.md) |
| 6.4 | Draft §6.4 ($N^{2g}$ GSD via flat-connection moduli) | [06_4_gsd_genus_g.md](../tasks/06_4_gsd_genus_g.md) |

### Chapter 7 - Dijkgraaf-Witten (~8 pp main text)

| # | Task | File |
|---|---|---|
| 7.1 | Draft §7.1 (finite-group gauge theory, cocycle pairing path integral) | [07_1_dw_action.md](../tasks/07_1_dw_action.md) |
| 7.2 | Draft §7.2 (classify $H^3(\mathbb{Z}_N, U(1)) = \mathbb{Z}_N$; full bar resolution only if time permits) | [07_2_H3_ZN.md](../tasks/07_2_H3_ZN.md) |
| 7.3 | Draft §7.3 (untwisted $\mathbb{Z}_2$ DW = toric code, connect to Ch 6) | [07_3_toric_code_bridge.md](../tasks/07_3_toric_code_bridge.md) |
| 7.4 | Draft §7.4 (twisted DW as inflow laboratory) | [07_4_twisted_dw.md](../tasks/07_4_twisted_dw.md) |
| 7.5 | Cross-reference: DW feeds Ch 8, 10, and the outlook | [07_5_cross_ref_audit.md](../tasks/07_5_cross_ref_audit.md) |
| 7.6 | Appendix D handoff for discrete-gauge calculations | [07_6_appendix_D_handoff.md](../tasks/07_6_appendix_D_handoff.md) |

### Chapter 8 - Generalized Symmetries and Anomaly Inflow (~10 pp, strict cap)

| # | Task | File |
|---|---|---|
| 8.1 | Draft §8.1 (0-form symmetries in defect language) | [08_1_zero_form_defects.md](../tasks/08_1_zero_form_defects.md) |
| 8.2 | Draft §8.2 ($q$-form symmetries + dictionary table) | [08_2_q_form_dictionary.md](../tasks/08_2_q_form_dictionary.md) |
| 8.3 | Draft §8.3 (gauging higher-form symmetries, worked $\mathbb{Z}_N$) | [08_3_gauging.md](../tasks/08_3_gauging.md) |
| 8.4 | Draft §8.4 (anomalies as obstructions to gauging) | [08_4_anomaly_definition.md](../tasks/08_4_anomaly_definition.md) |
| 8.5 | Draft §8.5 (anomaly inflow, general statement) | [08_5_anomaly_inflow_general.md](../tasks/08_5_anomaly_inflow_general.md) |
| 8.6 | Draft §8.6 (HEP example: chiral anomaly from 5D CS bulk) | [08_6_hep_inflow_example.md](../tasks/08_6_hep_inflow_example.md) |
| 8.7 | Draft §8.7 (CM example: FQH edge inflow; TI story only if space remains) | [08_7_cm_inflow_example.md](../tasks/08_7_cm_inflow_example.md) |
| 8.8 | Draft §8.8 (SymTFT in one page) | [08_8_symtft_onepage.md](../tasks/08_8_symtft_onepage.md) |
| 8.9 | Scope guardrail: ~10 pp; trim SymTFT or secondary breadth material if over | [08_9_scope_guard.md](../tasks/08_9_scope_guard.md) |

## Acceptance criteria

- All three chapters compile as part of `paper/main.tex`.
- Chapter 6 derives (not states) the compact-BF <-> $\mathbb{Z}_N$ equivalence.
- Chapter 7 states the $\mathbb{Z}_N$ classification cleanly in the main text; the full bar-resolution proof is carried only if time permits, otherwise it lives in Appendix D.
- Chapter 8 contains the mandatory dictionary table.
- Both anomaly-inflow examples (HEP and CM/FQH) are in Chapter 8, with the secondary example compressible if needed.
- Page counts: Ch 6 ~6-8 pp, Ch 7 ~8 pp main text, Ch 8 ~10 pp.

## Dependencies

- Blocks: Stage IV (Chapter 9 toric-code discussion cites Chapter 6/7; Chapter 11 FQH edge-inflow cites Chapter 8).
- Depends on: Stage II (gauge-transformation material) and Stage 0 (CS chapter for parallel Wilson-loop calculation).

## Risks

- **Chapter 8 blow-up.** This is the biggest risk in the entire plan. Strict cap and Task 8.9 guardrail.
- **Ghost citations creep in.** Freed-notes and Nakahara references must be verified against the actual texts before they survive Stage VI.
- **Cohomology computation errors.** Task 7.2 is the place most likely to pick up a sign mistake. Sanity-check against a standard group-cohomology reference.
