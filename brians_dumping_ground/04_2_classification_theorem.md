# Task 4.2 — Chapter 4 §4.2 The Classification Theorem (Showpiece)

- **Status:** done
- **Owner:** Brian
- **Duration:** 3 hours
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Prove the theorem: 2D oriented TQFTs are equivalent to commutative Frobenius algebras over $\mathbb{C}$. This is Brian's mathematical showpiece in Part I.

## Content outline

### The correspondence

Given a 2D TQFT $Z$:
- $V := Z(S^1)$ is a finite-dimensional vector space.
- $m := Z(\text{pair of pants}): V \otimes V \to V$ is the multiplication.
- $\eta := Z(\text{cap}): \mathbb{C} \to V$ defines the unit $\eta(1) \in V$.
- $\epsilon := Z(\text{cup}): V \to \mathbb{C}$ is the counit / trace.
- The pairing $V \otimes V \to \mathbb{C}$ via $(a,b) \mapsto \epsilon(m(a,b))$ is nondegenerate.
- Frobenius condition: $\epsilon(m(a,b)) = \epsilon(m(b,a))$ (from commutativity of multiplication in $\mathrm{Cob}_2$) and the cocycle/associativity conditions.

Conversely, given a commutative Frobenius algebra $(V, m, \eta, \epsilon)$:
- $Z(S^1) = V$.
- $Z(\text{POP}) = m$, etc.
- $Z$ extends to the whole category because the generators and relations of $\mathrm{Cob}_2$ are matched by the Frobenius axioms.

### Proof structure

1. **$Z \Rightarrow$ Frobenius**: apply the axioms to the generators; the relations among generators force the Frobenius axioms on $V$.
2. **Frobenius $\Rightarrow Z$**: define $Z$ on generators and check that relations are preserved. Kock's argument proceeds by Morse theory / handlebody decomposition; cite for the details and sketch the key step.
3. **Finite dimensionality**: follows from the cylinder giving $\dim V < \infty$.

## Steps

1. State the theorem clearly (definition of commutative Frobenius algebra, then the bijection).
2. Prove one direction in detail ($Z \Rightarrow$ Frobenius, because it's the easier direction).
3. Sketch the other direction and cite Kock §2 for details.
4. Appendix B (Task 4.5) will carry the full proof.

## Acceptance criteria

- Theorem stated precisely.
- At least one direction proved in full, the other sketched with citation.
- 4–5 pages, not more.

## Risks

- **Getting stuck in Morse theory.** Don't. State the Morse/handlebody step and cite Kock.
- **Category theory creep.** If you find yourself writing "adjunctions" or "2-functors", stop.

## References

- Kock 2004, *Frobenius Algebras and 2D TQFTs*, Chapters 1–3.
- Atiyah 1988 for axioms.
