# Task 2.1 — Chapter 2 §2.1 Forms, Wedge, Exterior Derivative

- **Status:** pending
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Introduce differential forms as an economical language for antisymmetric tensors, prove the graded Leibniz rule and nilpotency of $d$ by explicit computation, and establish the wedge-product conventions that will be used throughout the paper.

## Content outline

1. Local definition: $\omega = \frac{1}{p!}\omega_{\mu_1\cdots \mu_p}\,dx^{\mu_1}\wedge\cdots\wedge dx^{\mu_p}$.
2. Wedge product: bilinear, graded-commutative ($\alpha\wedge\beta = (-1)^{pq}\beta\wedge\alpha$).
3. Exterior derivative: $d\omega = \frac{1}{p!}\partial_\nu \omega_{\mu_1\cdots\mu_p}\,dx^\nu\wedge dx^{\mu_1}\wedge\cdots\wedge dx^{\mu_p}$.
4. Lemma (Leibniz + nilpotency): proof by direct component computation.

## Reuse opportunity

`paper/chern_simons_theory.tex` Section 2.1 has exactly this content already, including the Lemma `lem:leibniz-nilpotent` and its proof. Decision: **move** that material into Chapter 2, and have the CS chapter (Chapter 5) cite Chapter 2 §2.1 instead of duplicating.

## Steps

1. Copy Sections 2.1 from `chern_simons_theory.tex` to `paper/ch02_forms.tex` under a new `\section{Forms, wedge, exterior derivative}`.
2. In the CS chapter, replace the current Section 2.1 content with a short paragraph: "We use the conventions of Chapter 2 §2.1 throughout."
3. Verify Lemma 2.1 (Leibniz + nilpotency) still compiles with its proof.

## Acceptance criteria

- Chapter 2 §2.1 compiles inside `main.tex`.
- CS chapter's ex Section 2.1 is a cross-reference, not duplicated content.
- `\label{lem:leibniz-nilpotent}` still resolves from the CS chapter.

## Risks

- **Label collisions.** The CS chapter's label and the new Chapter 2 label must match. Decision: keep the label `lem:leibniz-nilpotent` in Chapter 2 and delete from the CS chapter.
- **Scope creep.** Don't re-prove everything about forms; just Leibniz and nilpotency.

## References

- Nakahara, *Geometry, Topology and Physics* (2003), Chapter 5.
- Already in `paper/chern_simons_theory.tex` Section 2.1.
