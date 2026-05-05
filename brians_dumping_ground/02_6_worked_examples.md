# Task 2.6 — Chapter 2 Worked Examples: EM and $S^1 \to S^1$ Winding

- **Status:** done (2026-05-04)
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [II](../stages/stage_II_partI_A.md)
- **Priority:** core

## Result

Both worked examples were already present in Ch 2 after Tasks 2.1 and 2.2 drafted them. Task 2.6 was a **verification-and-cleanup** task rather than new drafting. Two tightening edits applied to meet the full acceptance criteria:

### Edit 1: Sharpened the Maxwell example (Example~\ref{ex:maxwell-forms}, §2.1)

Added an explicit display of the inhomogeneous equation
\[
d \star F = \star J
\]
and a tightened topological-vs-dynamical punchline:

> \emph{Identities involving only $d$ and $\wedge$ are topological and metric-free, while equations involving $\star$ are dynamical and metric-dependent. The Chern--Simons action of Chapter~\ref{ch:chern-simons} uses only $d$ and $\wedge$ and is therefore a topological field theory; the Yang--Mills action $\int \tr(F \wedge \star F)$ uses the Hodge star and is metric-dependent, which is what makes it dynamical.}

This is the explicit formulation the task spec demanded (`Topological statements use only $d$ and $\wedge$; dynamical statements use $\star$`).

### Edit 2: Merged structural-lesson remark into the winding example

Spec acceptance criterion 2 required the forward pointer to Chapter 5 to live inside Example 2.2.7, not in a separate remark. Absorbed the former Remark~\ref{rem:ch2-winding-lesson} as the closing paragraph of `\begin{example}[Winding number]` under the label "Forward pointer." Zero dangling references to the deleted label.

### What Ch 2 now delivers for Task 2.6

1. **Maxwell in forms** — Example~\ref{ex:maxwell-forms} with:
   - $F = dA$ definition
   - Bianchi $dF = d^2 A = 0$ automatic from $d^2 = 0$
   - Inhomogeneous $d\star F = \star J$ explicitly displayed
   - Topological-vs-dynamical principle stated as the organizing dichotomy for the paper
2. **Winding number of $f:S^1 \to S^1$** — Example~\ref{ex:ch2-winding} with:
   - $d\theta$ globally defined though $\theta$ is not
   - Full derivation of $n(f) = \tfrac{1}{2\pi}\int f^*d\theta \in \Z$ via lift + FTC
   - Homotopy invariance via Corollary~\ref{cor:homotopy-invariance}
   - Explicit computation $f(t) = e^{int}$, $\tilde f(t) = nt$, $n(f) = n$
   - Forward pointer to CS level quantization (Chapter~\ref{ch:chern-simons}) now lives inside the example

### Verification matrix

Added row C.2.29 (topological/dynamical dichotomy). Other claims already covered by C.2.4, C.2.5, C.2.11.

### Label count

99 labels in `ch02_forms.tex`, zero collisions with `chern_simons_body.tex`.

### Chapter 2 status

All six numbered tasks (2.1 through 2.6) complete. Task 2.7 (scope-check to ~10 pp) remains.

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
