# Task 3.5b — Chapter 3 §3.5 Level Quantization with Assumptions and Caveats

- **Status:** pending
- **Owner:** Brian
- **Duration:** 75 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Tighten the level-quantization subsection so it states exactly when the standard integer-quantization argument is valid, what normalization is being used, and which nearby cases require refinement.

## Content

1. **Transformation law.** Write the gauge transformation of the Chern-Simons functional as an exact term plus the cubic Maurer-Cartan/Wess-Zumino term.
2. **Normalized integer.** For the standard `SU(2)` normalization, show
   $$
   \frac{1}{24\pi^2}\int_{S^3}\mathrm{tr}\bigl((g^{-1}dg)^3\bigr)=n\in\mathbb{Z}.
   $$
3. **Conclusion.** Requiring `e^{iS_{CS}}` to be invariant forces `k\in\mathbb{Z}` for compact simple simply connected `G` in the chosen trace normalization.
4. **Caveat paragraph.** Add one short paragraph covering:
   - semisimple products give one integer per simple factor;
   - non-simply-connected groups and spin-Chern-Simons theories need refined global statements;
   - abelian examples used later are consistent with integer level, but arise by a slightly different global story.
5. **Forward pointer.** Point ahead to the FQH section, where that integer becomes the effective-theory datum controlling Hall response and braiding.

## Source bundle

- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/dense_derivation_expansion.tex`
- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/homotopy_group_literature_intake_2026-05-04.md`
- Bott 1956, Dunne 1999, Witten 1989, Elitzur-Moore-Schwimmer-Seiberg 1989

## Acceptance criteria

- The integer-quantization statement includes its assumptions in the same neighborhood as the formula.
- The caveat paragraph prevents over-claiming without derailing the subsection.
- The subsection remains readable to the intended final-paper audience.

## Risks

- **Too many caveats at once.** The fix is one honest paragraph, not a new appendix.
