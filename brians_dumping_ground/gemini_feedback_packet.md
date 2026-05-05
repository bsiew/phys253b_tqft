# Gemini Feedback Packet

Use this file as the context packet for a Gemini review of the revised `plan/` tree.

## What changed

1. The page target is no longer `75-100` main text. The revised working target is `110-120` pages main text plus about `10-15` pages appendix, for roughly `120-135` pages overall.
2. The timeline no longer pretends to be 10 days. It is now 8 scheduled days plus 1 explicit buffer day.
3. The plan no longer treats `TQFT_outline_v2.tex` as binding. It is now an input, not the source of truth.
4. The existing `paper/chern_simons_theory.tex` is treated as the mathematical anchor of Part I. The revised plan preserves it as a standalone archival compile target and integrates it non-destructively via wrapper/body architecture.
5. The experimental plan has been refreshed from `Werkmeister 2024` to `Werkmeister 2025`, with optional mention of later 2025 follow-up results if they sharpen the narrative.
6. The appendix boundaries are more explicit:
   - Appendix B carries the heaviest Frobenius details.
   - Appendix D carries the longest discrete-gauge / bar-resolution details.
   - Appendix E carries the topological entanglement entropy derivation.
7. The prose-pass rules were softened so they ban AI filler but do not ban ordinary mathematical connective tissue like natural uses of "note that" or "observe that".
8. The presentation tasks were corrected so Brian's minute-10 showpiece is the actual `SU(2)` large-gauge level-quantization argument, and Helena's Hall-conductance formula now matches the corrected CS normalization.

## Current architecture decisions

1. Canonical paper architecture: `paper/main.tex` with `report`-style chapter structure.
2. Standalone archival source preserved: `paper/chern_simons_theory.tex`.
3. Integration route: create `paper/ch05_chern_simons.tex` plus an extracted body file, instead of destructively stripping the standalone CS file on Day 1.
4. `tasks/` is the canonical operational layer; `stages/` is the human summary layer; `plan_of_attack.tex` is the executive narrative layer.

## What I want Gemini to evaluate

Please review the revised `plan/` tree and answer these questions concretely.

1. Is the new page budget realistic, or does it still hide an overlong draft under smaller chapter caps?
2. Is the 8-day-plus-1-buffer structure believable, given the technical weight of Chapters 4, 7, and 8?
3. Is the non-destructive Chern-Simons integration architecture the right choice, or is there a cleaner repo structure that still preserves the verified standalone source?
4. Are the new appendix boundaries sensible, especially Appendix D for discrete gauge theory and Appendix E for TEE?
5. Is the current decision to avoid a standalone Witten-Jones chapter the right editorial choice, or should a short knot-invariants bridge be made more explicit somewhere?
6. Is Chapter 8 still too ambitious even after compression, and if so what should be cut first?
7. Is the experimental arc now the right one for a pedagogical review:
   - Nakamura 2020
   - Werkmeister 2025
   - Andersen 2023
   - optional short mention of 2025 follow-ups
8. Are there any remaining internal inconsistencies, ghost assumptions, or task-ordering problems in the revised plan tree?

## Files Gemini should inspect first

1. `plan/plan_of_attack.tex`
2. `plan/README.md`
3. `plan/stages/stage_I_scope_freeze.md`
4. `plan/stages/stage_III_partI_B.md`
5. `plan/stages/stage_IV_partII_A.md`
6. `plan/stages/stage_V_partII_B.md`
7. `plan/stages/stage_VI_integration.md`
8. `plan/stages/stage_VII_presentation.md`
9. `plan/tasks/01_4_main_tex_skeleton.md`
10. `plan/tasks/01_5_merged_bibliography.md`
11. `plan/tasks/01_6_shared_preamble.md`
12. `plan/tasks/07_2_H3_ZN.md`
13. `plan/tasks/11_5_honesty_box.md`
14. `plan/tasks/12_2_werkmeister_2025.md`
15. `plan/tasks/14_11_prose_pass.md`
16. `plan/tasks/15_1_brian_board_script.md`
17. `plan/tasks/15_2_helena_board_script.md`

## Review instructions for Gemini

Please do not rewrite the whole plan from scratch. Instead:

1. identify internal inconsistencies,
2. flag weak assumptions,
3. propose concrete edits,
4. and prioritize the fixes by importance.

If you suggest adding or cutting material, explain how that changes the page budget and the 9-day schedule.
