# Task 6.3 — Chapter 6 §6.3 BF Wilson/'t Hooft Linking

- **Status:** done
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Compute the mixed line-operator correlator $\langle W_q(C)\, T_n(C')\rangle_M$ for compact BF in $3$ dimensions, and obtain a linking-number phase that parallels the abelian CS Wilson-loop result from the CS chapter.

## Derivation

Insert the Wilson-line source $\delta_C$ and the dual BF line source $\delta_{C'}$, with $d\eta_C=\delta_C$ and $d\eta_{C'}=\delta_{C'}$ for chosen Seifert surfaces. The sourced action is

$S[A, B;C,C'] = \frac{N}{2\pi}\int B \wedge dA + q \int A \wedge \delta_C + n \int B \wedge \delta_{C'}.$

Shift $A \mapsto A + \frac{2\pi n}{N}\eta_{C'}$, integrate over $B$, and identify the remaining current pairing with the linking number.

With the sign convention of Chapter 6, the result is
$\langle W_q(C) T_n(C')\rangle = \exp(-2\pi i q n \, \mathrm{Lk}(C, C') / N)$.

## Steps

1. Write down the sourced action.
2. Shift $A$ to absorb the $B$-source.
3. Integrate out $B$ to impose flatness of the shifted field.
4. Evaluate the residual current pairing as a linking number.
5. Parallel this to the CS abelian calculation (Example 6.4 of the CS chapter).

## Acceptance criteria

- Full derivation.
- Explicit statement of the parallel to CS abelian Wilson-loop correlator.
- Forward-pointer to Chapter 9 (toric code braiding).
