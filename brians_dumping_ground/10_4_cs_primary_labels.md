# Task 10.4 — Chapter 10 §10.4 CS Primary Labels and Wilson-Loop Correlators

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [IV](../stages/stage_IV_partII_A.md)

## Goal

Tabulate the primary anyon labels for $U(1)_k$ and $SU(2)_k$ Chern–Simons theories, and state the correspondence between them and Wilson-loop correlators computed in the CS chapter.

## Content

### $U(1)_k$

- Labels $r = 0, 1, \ldots, k-1$.
- Fusion $r \times s = r + s \mod k$.
- Braiding phase $\theta_r = e^{i\pi r^2/k}$.
- $S_{rs} = k^{-1/2} e^{2\pi i rs / k}$ (from §10.3).

### $SU(2)_k$

- Labels $j = 0, 1/2, 1, \ldots, k/2$.
- Fusion via truncated $SU(2)$ tensor products (level-$k$ fusion).
- Primary labels count = $k + 1$, matching $\dim \mathcal{H}_{SU(2), k}(T^2) = k + 1$.

### Connection to CS

- Each anyon label corresponds to a representation of $SU(2)$ (or $U(1)$ charge) at level $k$.
- Wilson-loop expectation values in the CS chapter's Proposition `prop:topological` compute fusion/braiding data.

## Acceptance criteria

- Both tables present.
- Connection between labels and CS Wilson loops stated, with cross-reference to CS chapter.

## References

- Witten 1989 Jones.
- Any modular-tensor-category reference (e.g., Bakalov–Kirillov).
