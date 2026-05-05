# Task 3.1 — Chapter 3 §3.1 Cobordism Category

- **Status:** done
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Introduce the cobordism category $\mathrm{Cob}_d$: objects are closed oriented $(d-1)$-manifolds; morphisms are $d$-dimensional cobordisms up to orientation-preserving diffeomorphism; composition is gluing along boundaries; the category is symmetric monoidal under disjoint union.

## Content outline

1. Informal motivation: spacetime with in/out boundaries is a cobordism; a QFT assigns amplitudes.
2. Definition of $\mathrm{Cob}_d$:
   - Objects: closed oriented $(d-1)$-manifolds.
   - Morphisms $\Sigma_0 \to \Sigma_1$: equivalence classes of cobordisms $M$ with $\partial M = \bar\Sigma_0 \sqcup \Sigma_1$ (overline is orientation reversal).
   - Composition: gluing along the common boundary; well-defined because diffeomorphisms of the boundary extend to collar neighborhoods.
   - Identity on $\Sigma$: the cylinder $\Sigma \times [0,1]$.
3. Symmetric monoidal structure: $(\Sigma_1, \Sigma_2) \mapsto \Sigma_1 \sqcup \Sigma_2$, unit is empty manifold $\emptyset^{(d-1)}$, braiding is the obvious swap.

## Pedagogy notes

- Do not introduce category theory formally; the reader is a physicist, so phrases like "composition" should be motivated by path integrals gluing along time slices.
- Include one picture: a pair of pants as a cobordism from $S^1 \sqcup S^1$ to $S^1$.

## Acceptance criteria

- Definition of $\mathrm{Cob}_d$ is stated clearly.
- Symmetric monoidal structure is stated.
- Pair-of-pants picture is included.
- No heavy category theory — any mention is parenthetical and cited to Appendix A.

## Risks

- **Category theory creep.** Resist adding "(this is a 2-category because …)" sidebars. Not helpful to the audience.

## References

- Atiyah 1988 for the original formulation.
- Kock, *Frobenius Algebras and 2D TQFTs* Ch 1 for a friendly physicist-accessible discussion.
