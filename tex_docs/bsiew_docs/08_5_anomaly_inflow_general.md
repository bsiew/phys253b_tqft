# Task 8.5 — Chapter 8 §8.5 Anomaly Inflow: General Statement

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

State the anomaly-inflow mechanism: a $d$-dimensional theory with an anomaly can be realized as the boundary of a $(d+1)$-dimensional invertible TQFT, whose bulk partition function, on a manifold with boundary, picks up exactly the anomalous phase needed to cancel the boundary's anomaly.

## Content

1. **Setup.** $M$ is $(d+1)$-dim with boundary $\partial M$; the bulk is a $(d+1)$-dim invertible TQFT with action $S_{\text{inv}}[A]$. Its partition function $\exp(iS_{\text{inv}})$ is anomalous on manifolds with boundary — it shifts by a local functional of $A|_{\partial M}$ under background gauge transformations.
2. **Claim.** Pair the bulk with a $d$-dim theory on $\partial M$ whose anomaly is exactly minus this bulk shift: the combined system is gauge-invariant.
3. **Example.** $(d+1) = 5$ dim bulk Chern–Simons term $\int A \wedge F \wedge F$ cancels the 4D chiral anomaly; derived explicitly in §8.6.

## Acceptance criteria

- General statement present.
- The fact that the bulk must be invertible is explained (otherwise there are bulk local degrees of freedom).
- Forward-pointer to §8.6 and §8.7.

## References

- Callan–Harvey 1985 for the original inflow mechanism.
- Freed 1995 classical CS notes.
