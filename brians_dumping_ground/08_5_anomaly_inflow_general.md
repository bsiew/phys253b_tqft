# Task 8.5 --- Chapter 8 Sec. 8.5 Anomaly Inflow: General Statement

- **Status:** done
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

State the anomaly-inflow mechanism: a $d$-dimensional theory with an anomaly can be realized as the boundary of a $(d+1)$-dimensional invertible TQFT, whose bulk partition function, on a manifold with boundary, picks up exactly the anomalous phase needed to cancel the boundary's anomaly.

## Content

1. **Setup.** $M$ is $(d+1)$-dimensional with boundary $\partial M$; the bulk is a $(d+1)$-dimensional invertible TQFT with action $S_{\text{inv}}[A]$. Its partition function $\exp(iS_{\text{inv}})$ can vary on manifolds with boundary by a local functional of $A|_{\partial M}$ under background gauge transformations.
2. **Claim.** Pair the bulk with a $d$-dimensional theory on $\partial M$ whose anomaly is exactly minus this bulk shift: the combined system is gauge-invariant.
3. **Example template.** A five-dimensional bulk Chern--Simons-type term $\int A \wedge F \wedge F$ cancels the four-dimensional chiral anomaly; this is derived explicitly in Sec. 8.6.

## Acceptance criteria

- General statement present.
- The fact that the bulk must be invertible is explained.
- Forward-pointer to Sec. 8.6 and Sec. 8.7.

## References

- Callan--Harvey 1985.
- Freed 1995 classical Chern--Simons notes.
- Freed--Moore--Teleman 2024.

## Result

- `paper/ch08_gensym.tex` now contains a real `\S8.5` at `sec:anomaly-inflow-general`.
- The section defines the bulk-boundary setup, explains why the inflow bulk should be invertible, and states the general cancellation formula as Proposition `prop:general-inflow`.
- It ties the continuum statement back to the discrete Dijkgraaf--Witten inflow story from Chapter 7.
- It points forward explicitly to the four-dimensional chiral-anomaly derivation in Sec. 8.6 and the fractional-quantum-Hall inflow story in Sec. 8.7.
