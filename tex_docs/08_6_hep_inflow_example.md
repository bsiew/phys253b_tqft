# Task 8.6 — Chapter 8 §8.6 HEP Example: Chiral Anomaly from 5D CS Bulk

- **Status:** pending
- **Owner:** Brian
- **Duration:** 2 hours
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Take Schwartz Chapter 30's chiral anomaly and reframe it as the boundary shadow of a 5D Chern–Simons term in a bulk manifold. This is the high-energy example required by outline v2.

## Content

1. **Starting point.** Schwartz Eq 30.20: $\partial_\mu j^\mu_A = (1/16\pi^2) \epsilon^{\mu\nu\rho\sigma}\tr F_{\mu\nu}F_{\rho\sigma}$.
2. **5D bulk.** Place spacetime $M^4$ as the boundary of a 5-manifold $N^5$. The bulk 5D CS action is
   $$S_{5D} = \frac{1}{24\pi^2}\int_N \tr(A \wedge dA \wedge dA + \cdots)$$
   The full 5D term contains $A \wedge F \wedge F$ expanded with all cyclic combinations; look up the conventions carefully.
3. **Variation.** On a manifold with boundary, varying $S_{5D}$ under $A \to A^g$ picks up a boundary term equal to $-\int_{M^4} \omega_4(A, g)$ where $\omega_4$ is the 4-form anomaly polynomial.
4. **Matching.** This boundary shift is exactly the anomaly of the boundary chiral fermion, so the combined (bulk + fermion) system is gauge-invariant.

## Steps

1. Write down the 5D CS action explicitly.
2. Vary under a large gauge transformation; isolate the boundary term.
3. Compare with Schwartz Eq 30.20.
4. State: "This is the anomaly inflow of Callan–Harvey."

## Acceptance criteria

- Derivation complete, not just stated.
- Explicit tie to Schwartz Ch 30.
- ~2 pages.

## Risks

- **Sign conventions.** 5D CS signs are notoriously tricky; verify against Callan–Harvey 1985.
- **Scope creep.** Resist deriving the full anomaly polynomial via descent equations; leave to a reference.

## References

- Schwartz 2014 Ch 30.
- Callan–Harvey 1985.
