# Task 2.5 — Chapter 2 §2.5 Gauge Transformations and $F^g = g^{-1}Fg$

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

State the gauge transformation law $A \mapsto A^g = g^{-1}Ag + g^{-1}dg$ and derive $F^g = g^{-1}Fg$ by explicit computation. This template calculation is reused in the CS chapter's gauge-transformation analysis of $\omega_{CS}$, so it must be clean.

## Content outline

1. Gauge transformation: $g: M \to G$.
2. Formulas for $A^g$ and $F^g$.
3. Derivation of $F^g = g^{-1}Fg$ with every sign tracked, including the four mixed-term cancellations.
4. Maurer–Cartan equation $d\theta + \theta \wedge \theta = 0$ derived as a corollary.

## Reuse opportunity

CS chapter Section 2.5 has the full derivation. Move to Chapter 2.

## Steps

1. Copy Section 2.5 from `chern_simons_theory.tex` to `paper/ch02_forms.tex`.
2. Verify signs against Task 2.3 conventions.

## Acceptance criteria

- Full derivation present; no "after a short calculation".
- Four mixed-term cancellations shown explicitly.
- Maurer–Cartan is stated as a lemma and proved in one line.

## Risks

- **Sign flips when moving from CS chapter.** Careful.
