# Task 2.5 — Chapter 2 §2.5 Gauge Transformations and $F^g = g^{-1}Fg$

- **Status:** done (2026-05-04)
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)
- **Priority:** core

## Result

`paper/ch02_forms.tex` §2.5 ``Gauge transformations and the transformation of $F$'' drafted and appended. Chapter 2 is now complete at **677 lines** and five sections.

### Content delivered

1. **Definition~\ref{def:gauge-transf}** of gauge transformation $A^g = g^{-1}Ag + g^{-1}dg$, motivated as change of local section (from §2.4).
2. **Remark~\ref{rem:theta-tildeA}** introducing $\theta = g^{-1}dg$ (Maurer-Cartan) and $\tilde A = g^{-1}Ag$ notation.
3. **Lemma~\ref{lem:dginv}** deriving $dg^{-1} = -g^{-1}(dg)g^{-1}$ from $d(g^{-1}g) = 0$.
4. **Lemma~\ref{lem:maurer-cartan}** (Maurer-Cartan equation $d\theta + \theta\wedge\theta = 0$) proved in four lines using $d^2 = 0$ and Lemma~\ref{lem:dginv}.
5. **Remark~\ref{rem:mc-on-group}** flagging that Maurer-Cartan is really a statement about $G$ itself, to be used extensively in Chapter 5's Wess-Zumino three-form.
6. **Theorem~\ref{thm:F-transformation}** ($F^g = g^{-1}Fg$) proved in four explicit steps:
   - Step 1: compute $d\tilde A$ using Leibniz and Lemma~\ref{lem:dginv}, arriving at $d\tilde A = -\theta\wedge\tilde A + g^{-1}(dA)g - \tilde A\wedge\theta$.
   - Step 2: compute $dA^g = d\tilde A - \theta\wedge\theta$ using Maurer-Cartan.
   - Step 3: compute $A^g\wedge A^g = g^{-1}(A\wedge A)g + \tilde A\wedge\theta + \theta\wedge\tilde A + \theta\wedge\theta$.
   - Step 4: add; **three pairs of mixed terms** cancel explicitly.
7. **Remark~\ref{rem:four-mixed-terms}** naming the cancellation pattern and flagging it as the template for the $\omega_{\CS}$ computation in Ch 5.
8. **Proposition~\ref{prop:nonabelian-bianchi}** (non-abelian Bianchi $dF + A\wedge F - F\wedge A = 0$) with full proof using Leibniz, $d^2 = 0$, and cancellation of cubic $A\wedge A\wedge A$ terms.
9. **Remark~\ref{rem:infinitesimal-gauge}** giving the infinitesimal form $\delta A = d\varepsilon + [A, \varepsilon] = D\varepsilon$ and $\delta F = [F, \varepsilon]$.
10. **Closing paragraph** synthesizing the chapter and pointing forward to Ch 3 (axiomatic TQFT).

### What I verified by hand before drafting

| Claim | Check | ✓ |
|---|---|---|
| $dg^{-1} = -g^{-1}(dg)g^{-1}$ | $d(g^{-1}g) = (dg^{-1})g + g^{-1}dg = 0$ | ✓ |
| Maurer-Cartan: $d\theta = -\theta\wedge\theta$ | $d(g^{-1}dg) = (dg^{-1})\wedge(dg) + g^{-1}d^2g = -g^{-1}(dg)g^{-1}\wedge(dg) = -\theta\wedge\theta$ | ✓ |
| $d\tilde A = -\theta\wedge\tilde A + g^{-1}(dA)g - \tilde A\wedge\theta$ | Leibniz on $d(g^{-1}Ag)$ + $dg^{-1}$ substitution + matrix factor absorption | ✓ |
| $A^g\wedge A^g$ mixed expansion | Bilinearity + $\tilde A\wedge\tilde A = g^{-1}(A\wedge A)g$ via $gg^{-1} = \mathbf{1}$ | ✓ |
| Three-pair cancellation | $(-\theta\wedge\tilde A) + (+\theta\wedge\tilde A) = 0$; $(-\tilde A\wedge\theta) + (+\tilde A\wedge\theta) = 0$; $(-\theta\wedge\theta) + (+\theta\wedge\theta) = 0$ | ✓ |
| Bianchi: $A\wedge F - F\wedge A = A\wedge dA - dA\wedge A$ | Cubic $A\wedge A\wedge A$ appears on both sides and cancels | ✓ |
| Bianchi sum to zero | $dF = dA\wedge A - A\wedge dA$ cancels $A\wedge F - F\wedge A = A\wedge dA - dA\wedge A$ | ✓ |
| Infinitesimal $\delta A$ | $(\mathbf{1}-\varepsilon)A(\mathbf{1}+\varepsilon) + (\mathbf{1}-\varepsilon)d\varepsilon = A + [A,\varepsilon] + d\varepsilon + O(\varepsilon^2)$ | ✓ |

### Label collisions

None. Ch 2 uses `eq:gauge-A-2`, `eq:F-transformation`, `eq:dginv-lemma`, `lem:maurer-cartan` — all distinct from CS body's `eq:gauge-A`, `eq:gauge-F`, `eq:dginv`, `lem:MC`. Integration plan recorded in `plan/notes/stage_III_trim_log.md`.

### Content duplication flagged

The CS body §2.5 now has identical content. Trim-log entry says: replace CS body §2.5 with a pointer to `\ref{sec:gauge-transf}` during Task 14.11, saving ~40 lines.

### Verification-matrix rows added

C.2.24 through C.2.28.

### Chapter 2 is complete

All five sections drafted. The chapter is the geometric language foundation for Chapters 5, 6, 7, 8. Ready to move to Chapter 3 (axiomatic TQFT) or (more appropriately per Task 2.6) pick up the worked-examples task.

## Goal

State the gauge transformation law $A \mapsto A^g = g^{-1}Ag + g^{-1}dg$ and derive $F^g = g^{-1}Fg$ by explicit computation. This template calculation is reused in the CS chapter's gauge-transformation analysis of $\omega_{CS}$, so it must be clean.

## Content outline

1. Gauge transformation: $g: M \to G$.
2. Formulas for $A^g$ and $F^g$.
3. Derivation of $F^g = g^{-1}Fg$ with every sign tracked, including the four mixed-term cancellations.
4. Maurer–Cartan equation $d\theta + \theta \wedge \theta = 0$ derived as a corollary.

## Reuse opportunity

CS chapter Section 2.5 has the full derivation. Use it as the verified template for Chapter 2 without changing the standalone file during drafting.

## Steps

1. Adapt Section 2.5 from `chern_simons_theory.tex` into `paper/ch02_forms.tex`.
2. Verify signs against Task 2.3 conventions.

## Acceptance criteria

- Full derivation present; no "after a short calculation".
- Four mixed-term cancellations shown explicitly.
- Maurer–Cartan is stated as a lemma and proved in one line.

## Risks

- **Sign flips when moving from CS chapter.** Careful.
