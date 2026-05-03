# Task 6.3 — Chapter 6 §6.3 BF Wilson/'t Hooft Linking

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Compute $\langle W_q(C) \cdot T_n(\Sigma)\rangle_M$ for compact BF on a closed 3-manifold, and obtain a linking-number phase that parallels the abelian CS Wilson-loop result from the CS chapter.

## Derivation

Insert Wilson-line source $j_C$ (a distributional two-form with $d\eta = j_C$ for Seifert surface $\eta$) and 't Hooft-surface source $j_\Sigma$. The action becomes:

$S[A, B, \text{sources}] = \frac{N}{2\pi}\int B \wedge dA + q \int \eta_C \wedge dA + n \int B \wedge j_\Sigma$

After completing the square in $A$ and $B$, the correlator picks up a phase proportional to the linking number of $C$ and $\Sigma$.

Result: $\langle W_q(C) T_n(\Sigma)\rangle = \exp(2\pi i q n \, \mathrm{Lk}(C, \Sigma) / N)$.

## Steps

1. Write down the sourced action.
2. Integrate out $B$ first: get delta-function constraint relating $A$ and $j_\Sigma$.
3. Plug back into $W_q$ and pick up the linking phase.
4. Parallel this to the CS abelian calculation (Example 6.4 of the CS chapter).

## Acceptance criteria

- Full derivation.
- Explicit statement of the parallel to CS abelian Wilson-loop correlator.
- Forward-pointer to Chapter 9 (toric code braiding).
