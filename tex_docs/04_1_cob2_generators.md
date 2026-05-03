# Task 4.1 — Chapter 4 §4.1 Generators and Relations of $\mathrm{Cob}_2$

- **Status:** pending
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Identify the generators of the 2-dimensional oriented cobordism category and the relations among them. The generators are the cap, the cup, the cylinder, and the pair of pants (and its reverse). The relations are: commutativity of multiplication, associativity, unitality, and the Frobenius condition.

## Content outline

1. **The generators**. Four basic building blocks:
   - Cap $D^2$: morphism $\emptyset \to S^1$, picture of a disk with boundary up.
   - Cup $\bar D^2$: morphism $S^1 \to \emptyset$.
   - Cylinder $S^1 \times [0,1]$: identity $S^1 \to S^1$.
   - Pair of pants: $S^1 \sqcup S^1 \to S^1$ (multiplication) and $S^1 \to S^1 \sqcup S^1$ (comultiplication).
2. **The relations**. Every closed oriented surface decomposes into pairs of pants glued along cylinders (Morse-theoretic / handlebody decomposition). The relations that determine when two decompositions of the same surface must give the same TQFT amplitudes include:
   - Associativity (different ways of joining 3 circles into 1).
   - Commutativity (swap of inputs).
   - Unitality (cap + cylinder = cylinder).
   - The Frobenius relation (equating two different decompositions of the four-holed sphere).
3. **Figure 1**: the pair of pants as a cobordism picture. See also `paper/figures/fig02_pop.tex`.

## Acceptance criteria

- All four generators identified.
- All relations stated with a one-line justification ("because the corresponding surfaces are diffeomorphic").
- Figure 1 (POP) present.

## References

- Kock 2004 §1.3 for the full generator-relation presentation.
