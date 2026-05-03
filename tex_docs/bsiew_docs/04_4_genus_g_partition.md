# Task 4.4 — Chapter 4 §4.4 Partition Function on $\Sigma_g$

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Derive the formula $Z(\Sigma_g) = \sum_i \lambda_i^{2-2g}$ where $\lambda_i$ are eigenvalues of the "handle operator" (multiplication by the idempotent dual element), by explicit decomposition of $\Sigma_g$ into pairs of pants.

## Derivation sketch

1. Decompose $\Sigma_g$ into $2g$ pairs of pants (and $2g-2$ or so cylinders, depending on conventions).
2. Express $Z(\Sigma_g)$ as a contraction of $2g$ copies of $m$ against $2g$ copies of its dual $\Delta = m^*$.
3. Handle operator $H = m \circ \Delta$ is diagonalizable in a suitable basis of $V$; let $\lambda_i$ be its eigenvalues.
4. Derive $Z(\Sigma_g) = \mathrm{tr}(H^g) = \sum_i \lambda_i^g$ — with the $2-2g$ exponent coming from a more careful accounting of caps, cups, and cylinders.

(The exact exponent is $Z(\Sigma_g) = \sum \lambda_i^{2-2g}$ or $\sum \lambda_i^{g-1}$ depending on convention. Verify before committing.)

## Steps

1. Work through the decomposition carefully on paper.
2. Verify the formula on small cases: $g = 0$ (sphere), $g = 1$ (torus).
3. Match against Example 4.3.2: for the center-of-group-algebra example, the torus partition function is $|G|$, which forces $\sum \lambda_i = |G|$, check.

## Acceptance criteria

- Formula derived, not stated.
- Small-genus sanity checks pass.

## Risks

- **Getting the exponent wrong.** The $2-2g$ convention is correct only with specific cap/cup/pop normalizations. Verify against Kock §2.
