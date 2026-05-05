# Task 8.4 --- Chapter 8 Sec. 8.4 Anomalies as Obstructions to Gauging

- **Status:** done
- **Owner:** Brian
- **Duration:** 45 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Define 't Hooft anomaly: a theory has an anomaly for symmetry $G$ if the partition function in a nontrivial $G$-background field is not gauge-invariant but shifts by a local functional.

## Content

1. **'t Hooft anomaly, operational definition.** Put the theory on a manifold $M$ with a $G$-background field $A$. Under a background gauge transformation $A \to A^g$, the partition function shifts by $Z[A^g] = Z[A] \cdot e^{i\alpha[A, g]}$ where $\alpha[A, g]$ is a local functional of $A$ and $g$.
2. **Consequence.** The anomaly prevents gauging $G$ entirely; any attempt to sum over $A$-configurations fails because the phase is not gauge-invariant.
3. **Example, warmup.** The chiral fermion in 2D has an anomaly in $U(1)_{\text{vector}} \times U(1)_{\text{axial}}$; gauging both simultaneously is forbidden.

## Acceptance criteria

- Definition stated precisely.
- Short example (chiral fermion in 2D) illustrating.
- About one page of main-text content.

## Result

- `paper/ch08_gensym.tex` now contains a real `\S8.4` at `sec:anomaly-definition`.
- The section gives the operational definition of an 't Hooft anomaly, including the role of local counterterms.
- It proves explicitly that an anomaly obstructs gauging.
- It includes a short two-dimensional chiral-fermion warmup, while deferring the fuller inflow treatment to the later Chapter 8 sections.
