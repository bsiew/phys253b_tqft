# Task 6.4 — Chapter 6 §6.4 BF Ground-State Degeneracy $N^{2g}$ on $\Sigma_g$

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Derive that the Hilbert space of compact BF theory at level $N$ on a spatial slice $\Sigma_g$ of genus $g$ has dimension $N^{2g}$. Use the same flat-connection moduli space / Wilson-line algebra technology as in the CS chapter's $U(1)_k$ torus derivation.

## Derivation strategy

1. Flat $U(1)$ connections on $\Sigma_g$ are classified by $\mathrm{Hom}(\pi_1(\Sigma_g), U(1)) = U(1)^{2g}$ (the $2g$ holonomies around generators of $\pi_1$).
2. Compactness + level $N$ produces, after quantization, a Hilbert space of dimension $N^{2g}$.
3. For $g = 1$: $N^2$ states, matching the toric code's $4 = 2^2$ for $N = 2$.

## Reuse from CS chapter

The CS chapter Section 7 has essentially this derivation for $U(1)_k$ on $T^2$, giving $\dim \mathcal{H} = k$. Adapt: for BF with level $N$, the analogous result is $\dim \mathcal{H} = N^{2g}$, not $N^g$, because the BF Hilbert space structure is different ($A$ and $B$ both contribute holonomies).

## Steps

1. Parametrize flat connections on $\Sigma_g$.
2. Quantize the reduced phase space using the finite Heisenberg algebra.
3. Check: $g = 0$ (sphere) gives 1 state; $g = 1$ (torus) gives $N^2$; and $N = 2, g = 1$ gives 4 (toric code GSD).

## Acceptance criteria

- $N^{2g}$ derived.
- Sanity checks pass.
- Forward-pointer to Chapter 9 (toric code) and Chapter 7 (DW).
