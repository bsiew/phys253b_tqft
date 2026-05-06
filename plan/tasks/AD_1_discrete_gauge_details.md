# Task D.1 — Appendix D: Discrete Gauge Theory Details (BF ↔ $\mathbb{Z}_N$ and $H^3$ Bar Resolution)

- **Status:** pending
- **Priority:** core
- **Owner:** Brian
- **Duration:** 3 hours
- **Stage:** [VI](../stages/stage_VI_integration.md) (earlier if Stage III sends material here)

## Goal

Carry the mathematical heavy lifting that Chapter 6 (BF theory) and Chapter 7 (Dijkgraaf–Witten) explicitly defer. Currently two items are flagged for this appendix:

1. Full derivation of the compact-BF ↔ $\mathbb{Z}_N$ gauge theory equivalence via lattice $B$-integration.
2. Full bar-resolution computation of $H^3(\mathbb{Z}_N, U(1)) = \mathbb{Z}_N$.

## Content

### D.1 BF ↔ $\mathbb{Z}_N$ on the lattice

- Discretize the 3-manifold $M$ as a cell complex.
- Write compact-$U(1)$ BF partition function as a product over cells, with $B$-integration on each 2-cell producing a $\delta$-function enforcing $dA \in (2\pi/N)\mathbb{Z}$.
- Sum over residual $\mathbb{Z}_N$ holonomies gives the untwisted DW partition function.
- Full with all signs; ~1.5 pp.

### D.2 $H^3(\mathbb{Z}_N, U(1))$ via bar resolution

Follow Task 7.2's plan:
- State the bar complex $B_n = \mathbb{Z}[G^{n+1}]$ with boundary $\partial(g_0, \ldots, g_n) = \sum (-1)^i (g_0, \ldots, \hat g_i, \ldots, g_n)$.
- Dualize to cochains $f: G^n \to U(1)$.
- Write 3-cocycle condition in full.
- Canonical representative $\omega_p(a, b, c) = \exp(2\pi i p\, a \lfloor (b+c)/N \rfloor / N)$.
- Verify $\omega_p$ is a cocycle by direct substitution.
- Verify $\omega_p \sim \omega_q$ iff $p \equiv q \pmod N$ by exhibiting a coboundary $\beta$ witnessing the equivalence.
- Conclude $H^3(\mathbb{Z}_N, U(1)) = \mathbb{Z}_N$.
- ~3 pp.

## Acceptance criteria

- ~5 pp total.
- Every step has all signs.
- Main chapters 6, 7 point here explicitly via `\ref`.
- Sanity check: for $N=2$, the two classes correspond to untwisted toric code and the "double semion" twist; name-check both.

## Risks

- **Sign conventions in bar resolution.** Pick one convention (Brown's *Cohomology of Groups*) and cite it. Verify every sign against a single source to avoid combining conventions.
