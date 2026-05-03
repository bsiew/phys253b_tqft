# Task 2.3 — Chapter 2 §2.3 Lie-Algebra-Valued Forms and Conventions

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Set up the conventions for anti-Hermitian Lie-algebra-valued one-forms as used throughout the TQFT literature, and give the explicit translation to Schwartz's Hermitian convention. Everything downstream — Chapters 5, 6, 7, 8, 10 — uses these conventions.

## Content outline

1. Translation from Schwartz's Hermitian generators $T^a$ with $[T^a,T^b]=if^{abc}T^c$, $\tr(T^aT^b) = \tfrac{1}{2}\delta^{ab}$ to anti-Hermitian $t^a = -iT^a$ with $[t^a,t^b] = f^{abc}t^c$, $\tr(t^at^b) = -\tfrac{1}{2}\delta^{ab}$.
2. Connection one-form $A = A_\mu^a t^a\, dx^\mu$, translation $A_{\text{here}} = -iA_{\text{Schwartz}}$.
3. Field strength $F = dA + A\wedge A$; verify $A \wedge A \neq 0$ using $[t^a,t^b]$; express in components and show it equals the component formula $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu + [A_\mu, A_\nu]$.
4. Abelian case: $A \wedge A = 0$.

## Reuse opportunity

CS chapter Section 2.3 already has this. Move to Chapter 2.

## Steps

1. Copy Section 2.3 from `chern_simons_theory.tex` to `paper/ch02_forms.tex`.
2. Add an up-front "Convention" box stating clearly: "Throughout Chapters 2–8 we use the anti-Hermitian convention. To translate to Schwartz's Hermitian convention, send $A \to -iA$ and $F \to -iF$."
3. Include the graded-commutator remark (factor of 2 between $[A,A]$ and $A\wedge A$).

## Acceptance criteria

- Conventions are stated explicitly and unambiguously up front.
- Every sign in the $F = dA + A \wedge A$ derivation is checked.
- The translation to Schwartz appears in a box or clearly marked paragraph.

## Risks

- **Sign confusion downstream.** If this chapter gets the conventions wrong, every chapter that uses connections breaks. Mitigation: when editing, verify against the already-debugged CS chapter.
