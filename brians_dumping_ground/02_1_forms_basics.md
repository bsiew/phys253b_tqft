# Task 2.1 — Chapter 2 §2.1 Forms, Wedge, Exterior Derivative

- **Status:** done (2026-05-03)
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [II](../stages/stage_II_partI_A.md)
- **Priority:** core

## Result

`paper/ch02_forms.tex` now contains a fully drafted §2.1 (``Forms, wedge, exterior derivative''). The section is self-contained: a physics reader of \cite{Schwartz2014QFT} through Chapter 30 can follow every step without prior exposure to differential forms.

### Content delivered

1. **Local definition of a $p$-form**, with an explicit remark on the $1/p!$ prefactor and its relation to the ordered-multi-index convention.
2. **The wedge product**, defined on basis one-forms and extended bilinearly, with the explicit component formula \eqref{eq:wedge-components}.
3. **Graded commutativity** $\alpha\wedge\beta = (-1)^{pq}\beta\wedge\alpha$, proved by counting $p\cdot q$ adjacent transpositions (Proposition~\ref{prop:graded-comm}).
4. **Two specializations** of graded commutativity: odd-degree forms square to zero; even-degree forms commute with everything.
5. **The exterior derivative** defined by \eqref{eq:d-def}, with the Maxwell-style calculation of $dA = \tfrac{1}{2}F_{\mu\nu}dx^\mu\wedge dx^\nu$ spelled out via symmetric/antisymmetric decomposition plus dummy-index relabeling.
6. **Worked example** computing $d$ of a 2-form on $\mathbb{R}^3$ and recovering the divergence of a vector field $(P, Q, R)$.
7. **Lemma~\ref{lem:ch2-leibniz-nilpotent}** with full proofs of the Leibniz rule and $d^2 = 0$. Every sign and every factor is tracked; no ``it can be seen''.
8. **Remark on the symmetric-antisymmetric contraction principle** that drives nilpotency.
9. **Maxwell example** (Bianchi identity as $d^2 A = 0$) and $U(1)$-gauge-invariance-of-$F$ example, both as one-line consequences of Lemma~\ref{lem:ch2-leibniz-nilpotent}.
10. **De Rham cohomology** defined, with the de Rham--singular isomorphism stated and cited forward to Chapter 3.

### Verification performed by hand

- Graded commutativity: $p\cdot q$ adjacent transpositions, sign $(-1)^{pq}$. ✓
- $dA$ component computation: symmetric part vanishes against antisymmetric wedge, dummy-index rename gives the conventional $\tfrac{1}{2}F_{\mu\nu}dx^\mu\wedge dx^\nu$. ✓
- Leibniz: the $(-1)^p$ comes from moving $dx^\rho$ past $p$ basis one-forms of $\alpha$. ✓
- Nilpotency: $\partial_\sigma\partial_\rho = \partial_\rho\partial_\sigma$ (Clairaut) paired with $dx^\sigma\wedge dx^\rho = -dx^\rho\wedge dx^\sigma$; symmetric $\times$ antisymmetric $= 0$. Explicit pair-by-pair summation written out. ✓
- $\mathbb{R}^3$ divergence example: every cancellation from $dx^\mu\wedge dx^\mu = 0$ spelled out; the two adjacent transpositions that cycle $dy\wedge dz\wedge dx \to dx\wedge dy\wedge dz$ counted. ✓

### Label collisions resolved

Four labels (`eq:graded-comm`, `lem:leibniz-nilpotent`, `eq:leibniz`, `eq:nilpotent`) collided with identical labels in `chern_simons_body.tex`. Ch 2 versions renamed with `ch2-` prefix; resolution plan recorded in `plan/notes/stage_III_trim_log.md` for the integration pass (Task 14.11 or 14.4).

### Verification-matrix rows added

C.2.1 through C.2.6 added to `plan/notes/verification_matrix.md`.

## Goal

Introduce differential forms as an economical language for antisymmetric tensors, prove the graded Leibniz rule and nilpotency of $d$ by explicit computation, and establish the wedge-product conventions that will be used throughout the paper.

## Content outline

1. Local definition: $\omega = \frac{1}{p!}\omega_{\mu_1\cdots \mu_p}\,dx^{\mu_1}\wedge\cdots\wedge dx^{\mu_p}$.
2. Wedge product: bilinear, graded-commutative ($\alpha\wedge\beta = (-1)^{pq}\beta\wedge\alpha$).
3. Exterior derivative: $d\omega = \frac{1}{p!}\partial_\nu \omega_{\mu_1\cdots\mu_p}\,dx^\nu\wedge dx^{\mu_1}\wedge\cdots\wedge dx^{\mu_p}$.
4. Lemma (Leibniz + nilpotency): proof by direct component computation.

## Reuse opportunity

`paper/chern_simons_theory.tex` Section 2.1 has exactly this content already, including the Lemma `lem:leibniz-nilpotent` and its proof. Use it as the verified source text, but do not destabilize the standalone CS file while drafting Chapter 2.

## Steps

1. Adapt Section 2.1 from `chern_simons_theory.tex` into `paper/ch02_forms.tex` under a new `\section{Forms, wedge, exterior derivative}`.
2. Leave the standalone CS chapter unchanged during the drafting pass.
3. During integration, decide whether Chapter 5 keeps a short self-contained recap or cross-refers back to Chapter 2.

## Acceptance criteria

- Chapter 2 §2.1 compiles inside `main.tex`.
- The Chapter 2 version is drafted cleanly without breaking the standalone CS chapter.
- Label strategy is recorded so the final integration pass can remove duplication without orphaning references.

## Risks

- **Label collisions.** Do not force label migration until the integration pass.
- **Scope creep.** Don't re-prove everything about forms; just Leibniz and nilpotency.

## References

- Nakahara, *Geometry, Topology and Physics* (2003), Chapter 5.
- Already in `paper/chern_simons_theory.tex` Section 2.1.
