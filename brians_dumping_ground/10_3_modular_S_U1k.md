# Task 10.3 — Chapter 10 §10.3 Modular $S$-Matrix for $U(1)_k$ from CS Hilbert Space

- **Status:** pending
- **Owner:** Brian
- **Duration:** 2 hours
- **Stage:** [IV](../stages/stage_IV_partII_A.md)

## Goal

Derive the modular $S$-matrix for $U(1)_k$ Chern–Simons theory directly from the $k$-dimensional torus Hilbert space derived in the CS chapter (Proposition `prop:dimU1k`). The $S$-matrix should diagonalize fusion.

## Content

1. **Setup.** The CS chapter gave $\mathcal{H}_{U(1),k}(T^2)$ with basis $\{\psi_r\}_{r=0}^{k-1}$ and the finite Heisenberg algebra $\hat U \hat V = e^{-2\pi i/k} \hat V \hat U$.
2. **Modular transformation $S$.** The $SL(2, \mathbb{Z})$ action on the torus (swap of cycles) acts on the Hilbert space. In the $\{\psi_r\}$ basis, $S$ is a discrete Fourier transform:
   $$S_{rs} = \frac{1}{\sqrt{k}} e^{2\pi i r s / k}.$$
3. **Derivation.** The $S$ operator must exchange $\hat U \leftrightarrow \hat V$. Use this intertwining property to fix $S_{rs}$ up to a phase; verify by direct computation $S \hat U S^{-1} = \hat V$.
4. **Verlinde formula check.** The fusion rules for $U(1)_k$ anyons are $[r] \times [s] = [r + s \mod k]$; $S$ diagonalizes via
   $$N^t_{rs} = \sum_u \frac{S_{ru} S_{su} S^*_{tu}}{S_{0u}}$$
   Verify this gives $\delta_{t, r+s \mod k}$.

## Acceptance criteria

- $S_{rs} = k^{-1/2}e^{2\pi i rs/k}$ derived, not stated.
- Verlinde formula check succeeds.
- Reference back to CS chapter Proposition `prop:dimU1k`.

## Risks

- **Phase conventions.** Different normalizations for $S$ appear in the literature; fix one and note the convention.
