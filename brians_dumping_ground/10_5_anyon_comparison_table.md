# Task 10.5 — Chapter 10 §10.5 Anyon Comparison Table

- **Status:** pending
- **Owner:** Brian + Helena
- **Duration:** 45 min
- **Stage:** [IV](../stages/stage_IV_partII_A.md)

## Goal

Produce the paper's comparison table of anyon data for toric code, Laughlin, and Ising anyons.

## Table

| System | Labels | Fusion | Braiding phase (self) | Topological spin |
|---|---|---|---|---|
| Toric code ($\mathbb{Z}_2$) | $1, e, m, \epsilon$ | $e \cdot e = m \cdot m = 1$, $e \cdot m = \epsilon$ | $\theta_e = \theta_m = 1$, $\theta_\epsilon = -1$ | bosons/bosons/fermion |
| Laughlin $\nu = 1/m$ ($\mathbb{Z}_m$) | $0, 1, \ldots, m-1$ | $r \cdot s = r+s \mod m$ | $\theta_r = e^{i\pi r^2 / m}$ | $r^2/(2m)$ |
| Ising | $1, \sigma, \psi$ | $\sigma \cdot \sigma = 1 + \psi$, $\psi \cdot \psi = 1$, $\sigma \cdot \psi = \sigma$ | $\theta_\sigma = e^{i\pi/8}$, $\theta_\psi = -1$ | mixed (non-abelian $\sigma$) |

## Steps

1. Fill in the table.
2. Add a short paragraph contextualizing: abelian (toric code, Laughlin) vs. non-abelian (Ising).
3. Brian owns the toric code and Laughlin columns (derivations in CS chapter and Ch 6/9).
4. Helena owns the Ising column and the physical-interpretation prose.

## Acceptance criteria

- Table renders cleanly.
- Every entry is cited or derived elsewhere in the paper.
