# Task 8.6 - Chapter 8 Sec. 8.6 HEP Example: Chiral Anomaly from 5D CS Bulk

- **Status:** done
- **Owner:** Brian
- **Duration:** 2 hours
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Take Schwartz Chapter 30's chiral anomaly and reframe it as the boundary shadow of a 5D Chern--Simons-type term in a bulk manifold. This is the main high-energy anomaly-inflow example for the paper.

## Content

1. **Starting point.** Schwartz Eq. 30.20:
   \[
   \partial_\mu j^\mu_A
   =
   \frac{1}{16\pi^2}\epsilon^{\mu\nu\rho\sigma}\tr(F_{\mu\nu}F_{\rho\sigma}).
   \]
2. **5D bulk.** Place spacetime $X^4$ as the boundary of a 5-manifold $N^5$. For the direct Schwartz match, use the mixed 5D term
   \[
   S_{\mathrm{bulk}}[a,A]
   =
   -\frac{1}{4\pi^2}\int_N a\wedge \tr(F\wedge F),
   \]
   where $a$ is the axial background field and $A$ is the vector gauge field.
3. **Variation.** On a manifold with boundary, varying under the axial background gauge transformation $a\to a+d\lambda$ produces the boundary term
   \[
   \delta_\lambda S_{\mathrm{bulk}}
   =
   -\frac{1}{4\pi^2}\int_X \lambda\,\tr(F\wedge F).
   \]
4. **Matching.** This boundary shift is exactly minus the boundary axial anomaly written in forms, so the combined bulk-plus-boundary system is gauge-invariant.

## Acceptance criteria

- Derivation complete, not just stated.
- Explicit tie to Schwartz Ch. 30.
- About 2 pages.

## Result

- `paper/ch08_gensym.tex` now contains a real `\S8.6` at `sec:hep-inflow`.
- The section rewrites the Schwartz anomaly equation in differential-form notation and fixes the coefficient explicitly.
- It derives the boundary variation of the mixed five-dimensional inflow term and proves that it cancels the boundary axial anomaly.
- It states explicitly that this is the Callan--Harvey inflow mechanism in the present notation.
- A separate remark records the full nonabelian $CS_5$ form and explains that it belongs to the broader consistent-gauge-anomaly descent story, while the mixed term is the right choice for the direct Schwartz match.
