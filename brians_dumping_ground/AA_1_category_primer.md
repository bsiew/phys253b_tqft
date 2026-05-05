# Task A.1 — Appendix A: Category Theory Minimum

- **Status:** pending
- **Priority:** important
- **Owner:** Brian
- **Duration:** 3 hours
- **Stage:** [VI](../stages/stage_VI_integration.md) (or earlier if Stage II slack permits)

## Goal

Provide a 4–6 page primer on the bare minimum of category theory used in the paper: category, functor, natural transformation, symmetric monoidal structure, and dualizable objects. This is an escape hatch so Chapter 3 (Atiyah–Segal) and Chapter 4 (Frobenius classification) can use the words without pausing to define them.

## Content

1. **Definition of a category.** Objects, morphisms, composition, identity. One physics example (Hilbert spaces as a category) and one pure-math example (sets as a category).
2. **Functors.** Covariant and contravariant. Example: the functor assigning to each spacetime manifold its de Rham cohomology.
3. **Natural transformations.** State the definition; defer examples to "we will see one when we define a TQFT as a functor out of the cobordism category."
4. **Symmetric monoidal categories.** $\otimes$, unit object, braiding, symmetry. Examples: $(\mathrm{Vect}_\C, \otimes)$ and $(\mathrm{Cob}_d, \sqcup)$.
5. **Dualizable objects.** $V^*$ and the evaluation/coevaluation. This is what makes $\dim Z(\Sigma) < \infty$ work in Chapter 3.

## What to leave out

- Higher categories, 2-functors, cobordism hypothesis (cited in outlook only).
- Limits, colimits, adjoints.
- Abelian categories, derived functors.

## Acceptance criteria

- 4–6 pp total.
- Every term used in Chapters 3 and 4 is defined here, with a one-line cross-reference back to the appendix.
- No theorems beyond the Yoneda lemma stated in passing.

## References

- Mac Lane, *Categories for the Working Mathematician* (cited once, not followed in detail).
- Kock 2004 Ch 0 (a physicist-friendly minimalism).
