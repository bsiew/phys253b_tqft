# Task 4.4 — Chapter 4 §4.4 Partition Function on $\Sigma_g$

- **Status:** done
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Derive the genus formula in the normalization actually used in Chapter 4:
\[
Z(\Sigma_g)=\epsilon(e^g)=\Tr(H^{g-1}) \quad (g\ge 1),
\]
where $H=m\circ \Delta$ is the handle operator and $e=H(1)$ is the handle element. In a semisimple idempotent basis this becomes
\[
Z(\Sigma_g)=\sum_i \lambda_i^{g-1},
\]
with $\lambda_i$ the eigenvalues of $H$.

## Derivation sketch

1. Decompose $\Sigma_g$ as cap + $g$ copies of the once-punctured torus + cup.
2. Identify the once-punctured torus operator as $H = m \circ \Delta$.
3. Prove $H$ is multiplication by the handle element $e = m(\Delta(1))$.
4. Derive $Z(\Sigma_g) = \epsilon(e^g)$ and then the trace form $Z(\Sigma_g)=\Tr(H^{g-1})$ for $g\ge 1$.
5. In the semisimple idempotent basis, derive $Z(\Sigma_g)=\sum_i \lambda_i^{g-1}$.

## Steps

1. Work through the decomposition carefully on paper.
2. Verify the formula on small cases: $g = 0$ (sphere), $g = 1$ (torus).
3. Match against Example 4.3.2: for the center-of-group-algebra example, the torus partition function is the number of conjugacy classes of $G$, and for the cyclic example $A_n$ one gets $Z(\Sigma_g)=n^g$ with the present counit normalization.

## Acceptance criteria

- Formula derived, not stated.
- Small-genus sanity checks pass.

## Risks

- **Normalization confusion.** The exponent depends on how the counit is normalized. The chapter should state its convention explicitly and record the finite-gauge-theory rescaling separately.
