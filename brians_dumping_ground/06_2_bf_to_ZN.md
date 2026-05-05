# Task 6.2 — Chapter 6 §6.2 Compact BF at Level $N$ ↔ $\mathbb{Z}_N$ Gauge Theory

- **Status:** done
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Derive the equivalence between compact $U(1)$ BF theory at level $N$ and $\mathbb{Z}_N$ gauge theory, by integrating out $B$ as a Lagrange multiplier on the lattice or by summing over its periodic values on the continuum.

## Derivation strategy

Compact BF partition function: $Z_{BF}(M) = \int \mathcal{D}A \mathcal{D}B\, e^{i(N/2\pi) \int B \wedge dA}$ with $B$ taking values in $\mathbb{R}/2\pi\mathbb{Z}$ (compactness).

Summing over the compact $B$ at each point:
- The integral over $B \in [0, 2\pi)$ of $e^{i N \phi \cdot B/(2\pi)}$ for $\phi = dA$ produces a delta function enforcing $N\phi \in 2\pi\mathbb{Z}$, i.e. $\phi$ lands in $(2\pi/N)\mathbb{Z}$-valued one-form $\to$ the residual gauge field takes values in $\mathbb{Z}_N$.
- Equivalently: the path integral localizes on connections with holonomies in $\mathbb{Z}_N$.

Result: $Z_{BF, k=N}(M) = Z_{\mathbb{Z}_N}(M)$.

## Steps

1. Start from the continuum action.
2. Discretize if helpful (lattice BF on a 3-cell complex).
3. Perform the $B$ integration cell by cell.
4. Show the residual sum is over $\mathbb{Z}_N$-valued connections.
5. State: this is the untwisted 3D Dijkgraaf–Witten theory at gauge group $\mathbb{Z}_N$ (forward-pointer to Chapter 7).

## Acceptance criteria

- Derivation is explicit, not "it is well-known that".
- Forward-pointer to Chapter 7 §7.3 (DW at $\mathbb{Z}_2$ = toric code).

## Risks

- **Rigor ambiguity.** The $B$-integration argument is cleanest on the lattice; in the continuum it involves delta-function manipulations. Choose one (lattice) and stick with it.

## References

- Tong *Gauge Theory* notes.
