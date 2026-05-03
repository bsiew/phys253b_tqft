# Task 3.2 — Chapter 3 §3.2 Atiyah–Segal Axioms

- **Status:** pending
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

State the Atiyah–Segal axioms as a symmetric monoidal functor $Z: \mathrm{Cob}_d \to \mathrm{Vect}_{\mathbb{C}}$, and derive immediate consequences (finite dimensionality of $Z(\Sigma)$, duality between $Z(\Sigma)$ and $Z(\bar\Sigma)$, partition function on closed manifolds).

## Content outline

1. **Axiom 1** (Monoidality). $Z(\Sigma_1 \sqcup \Sigma_2) = Z(\Sigma_1) \otimes Z(\Sigma_2)$. $Z(\emptyset^{(d-1)}) = \mathbb{C}$.
2. **Axiom 2** (Functoriality / gluing). $Z(M_2 \circ M_1) = Z(M_2) \circ Z(M_1)$ for composable cobordisms.
3. **Axiom 3** (Orientation). $Z(\bar\Sigma) = Z(\Sigma)^*$.
4. **Consequences:**
   - $Z(\Sigma)$ is finite-dimensional. Argument: $Z(\Sigma) \otimes Z(\bar\Sigma) = Z(\Sigma \sqcup \bar\Sigma)$, and the cylinder-as-identity gives a nondegenerate pairing $Z(\bar\Sigma) \otimes Z(\Sigma) \to \mathbb{C}$; finiteness follows.
   - Closed-manifold partition function $Z(M)$ is a number for closed $d$-manifolds $M$.
5. State explicitly: the axioms do not uniquely determine a TQFT; additional data (like the CS action for CS theory) is needed.

## Acceptance criteria

- All three axioms stated.
- The finite-dimensionality consequence is derived, not just stated.
- Cross-reference the Atiyah 1988 paper for the original.

## References

- Atiyah 1988 (primary).
- Kock 2004 Ch 1 (pedagogical).
