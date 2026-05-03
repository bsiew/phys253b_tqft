# Task 2.6 — Chapter 2 Worked Examples: EM and $S^1 \to S^1$ Winding

- **Status:** pending
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Ground Chapter 2 in two concrete examples before moving on: Maxwell's theory in forms language and the winding number of $S^1 \to S^1$ as an integer-valued integral. Both foreshadow themes in the CS chapter.

## Content

### Example 2.6.1 — Maxwell in forms

- $A = A_\mu dx^\mu$, $F = dA$.
- Bianchi: $dF = d^2 A = 0$ automatically.
- Equation of motion $d\star F = \star J$ is metric-dependent through the Hodge star.
- Takeaway: topological statements use only $d$ and $\wedge$; dynamical statements use $\star$.

### Example 2.6.2 — Winding number of $f: S^1 \to S^1$

- Target parameterized by $\theta \in [0, 2\pi)$; $d\theta$ is globally defined even though $\theta$ is not.
- $\frac{1}{2\pi}\int_{S^1} f^* d\theta = n \in \mathbb{Z}$.
- Depends only on homotopy class of $f$.
- Foreshadows: the CS chapter's level quantization comes from exactly this structure, generalized to $SU(2)$ maps on a 3-manifold.

## Reuse

Both examples are already drafted in CS chapter Section 2.

## Steps

1. Copy Examples 2.2 and 2.5 from CS chapter to Chapter 2.

## Acceptance criteria

- Both examples in place.
- The foreshadowing sentence at the end of Example 2.6.2 points to the CS chapter by `\ref`.
