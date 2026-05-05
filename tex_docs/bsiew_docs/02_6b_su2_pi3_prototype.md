# Task 2.6b — Chapter 2 §2.5/2.6 The $SU(2)\simeq S^3$ Prototype for $\pi_3(G)$

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Bridge the existing $S^1 \to S^1$ winding example to the nonabelian case actually used later in Chern-Simons theory: maps $g : S^3 \to SU(2)\simeq S^3$ classified by degree, and then the Bott corollary that for compact simple simply connected $G$, $\pi_3(G)\cong \mathbb{Z}$.

## Content

1. **Prototype map.** Explain why $SU(2)\cong S^3$ as a manifold, so a map $g:S^3\to SU(2)$ has an integer degree.
2. **Integral formula.** State the standard normalized winding-number integral
   $$
   \frac{1}{24\pi^2}\int_{S^3}\mathrm{tr}\bigl((g^{-1}dg)^3\bigr)\in\mathbb{Z}.
   $$
3. **Generalization.** State, without reproving in detail, Bott's corollary that for compact connected simply connected simple Lie groups one has $\pi_3(G)\cong\mathbb{Z}$.
4. **Semisimple caveat.** One sentence that for several simple factors the result becomes $\mathbb{Z}^r$.
5. **Forward pointer.** End by saying this is exactly the topological input used in Chapter 3 large-gauge transformations and level quantization.

## Source bundle

- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/homotopy_group_literature_intake_2026-05-04.md`
- `PROJECTS/QFT/literature/manual_homotopy_group_sources/Bott1956_An_application_of_the_Morse_theory_to_the_topology_of_Lie-groups.pdf`
- `PROJECTS/QFT/literature/manual_homotopy_group_sources/Milnor_MorseTheory.pdf`
- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/tqft_algebraic_topology_review.md`

## Acceptance criteria

- The reader sees one explicit nonabelian winding-number formula before Chapter 3.
- The statement `\pi_3(G)\cong \mathbb{Z}` is not written without assumptions.
- The final sentence points to Chapter 3 by role, not just by citation.

## Risks

- **Too much topology too early.** Keep the proof light; this is a toolkit bridge, not a full algebraic-topology detour.
