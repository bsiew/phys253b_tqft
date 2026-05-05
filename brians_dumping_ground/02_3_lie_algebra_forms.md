# Task 2.3 — Chapter 2 §2.3 Lie-Algebra-Valued Forms and Conventions

- **Status:** done (2026-05-04)
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)
- **Priority:** core

## Result

`paper/ch02_forms.tex` §2.3 ``Lie-algebra-valued forms and the non-abelian field strength'' drafted and appended. File is now 466 lines with four sections (§2.1 forms basics, §2.2 integration/Stokes/de Rham, §2.3 Lie-algebra-valued/field-strength, and pointers to §2.4-2.5 still to come).

### Content delivered

1. **Anti-Hermitian-convention up-front block** (Remark~\ref{rem:translation-box}) with the one-line translation rule $A \to -iA$, $F \to -iF$, $t^a \to -iT^a$ between Schwartz's Hermitian convention and the geometry-literature anti-Hermitian convention.
2. **Proposition~\ref{prop:anti-herm-identities}** with full proof: $[t^a, t^b] = f^{abc} t^c$ (absence of $i$) and $\tr(t^at^b) = -\tfrac{1}{2}\delta^{ab}$, derived directly from Schwartz's Hermitian identities.
3. **Definition~\ref{def:connection-one-form}** of the connection one-form $A = A_\mu^a t^a\, dx^\mu$ with the translation rule.
4. **Wedge product of Lie-algebra-valued forms** defined via \eqref{eq:lie-wedge-def}, and the graded commutator (Definition~\ref{def:graded-commutator}) introduced to handle the noncommutative generator product.
5. **Proposition~\ref{prop:AwedgeA}** with a full proof that $A \wedge A = \tfrac{1}{2}[A_\mu, A_\nu] dx^\mu\wedge dx^\nu = \tfrac{1}{2} f^{abc} A_\mu^a A_\nu^b t^c\, dx^\mu \wedge dx^\nu$. The proof uses the symmetric-antisymmetric decomposition of $A_\mu^a A_\nu^b t^a t^b$ and cites the principle of Remark~\ref{rem:sym-anti} from §2.1.
6. **Remark~\ref{rem:AwedgeA-factor}** on the factor of 2 between $[A, A]$ (graded commutator) and $A \wedge A$.
7. **Abelian-case remarks** (Remark~\ref{rem:abelian-case}, Remark~\ref{rem:abelian-trace}) explaining why $A \wedge A = 0$ for $U(1)$ and setting the $\tr \to 1$ convention for Laughlin-action calculations in Chapter 5.
8. **Definition~\ref{def:F-nonabelian}** and **Proposition~\ref{prop:F-components}** with full derivation of $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu + [A_\mu, A_\nu]$.
9. **Remark~\ref{rem:schwartz-comparison}** with explicit line-by-line verification that $F_{\text{here}} = -i\, F_{\text{Schwartz}}$ under $A_\mu = -i A_\mu^{\text{Sch}}$.
10. **Example~\ref{ex:abelian-F-check}** as a sanity check that the abelian Maxwell formula is recovered.
11. **Forward pointer** to §2.5 for the non-abelian Bianchi identity and the gauge transformation law.

### Verification performed by hand before drafting

- **Anti-Hermitian bracket**: $[-iT^a, -iT^b] = -[T^a, T^b] = -if^{abc}T^c = -if^{abc}(it^c) = f^{abc}t^c$. ✓
- **Anti-Hermitian trace**: $\tr((-iT^a)(-iT^b)) = -\tr(T^aT^b) = -\tfrac{1}{2}\delta^{ab}$. ✓
- **$A \wedge A$**: relabeling $(\mu, a) \leftrightarrow (\nu, b)$ in the rename-dummies step gives $A_\nu^b A_\mu^a t^b t^a dx^\nu\wedge dx^\mu = -A_\mu^a A_\nu^b t^b t^a dx^\mu\wedge dx^\nu$; average to get the commutator. ✓
- **$dA$ component formula**: same symmetric-antisymmetric decomposition as scalar case. ✓
- **Schwartz comparison**: $F_{\mu\nu} = -i(\partial_\mu A_\nu^{\text{Sch}} - \partial_\nu A_\mu^{\text{Sch}}) - [A_\mu^{\text{Sch}}, A_\nu^{\text{Sch}}]$ from substitution; rearrange as $-i(\partial_\mu A_\nu^{\text{Sch}} - \partial_\nu A_\mu^{\text{Sch}} - i[A_\mu^{\text{Sch}}, A_\nu^{\text{Sch}}]) = -i F_{\mu\nu}^{\text{Sch}}$ using $-1 = -i\cdot i$ on the commutator. ✓

### Label collisions

None. The Ch 2 labels (`eq:A-components`, `eq:F-nonabelian-components`, `prop:anti-herm-identities`, `prop:AwedgeA`, `prop:F-components`) were chosen deliberately to avoid CS-body counterparts (`eq:A-def`, `eq:F-components`). Integration-pass merger documented in `plan/notes/stage_III_trim_log.md`.

### Verification-matrix rows added

C.2.13 through C.2.19.

## Goal

Set up the conventions for anti-Hermitian Lie-algebra-valued one-forms as used throughout the TQFT literature, and give the explicit translation to Schwartz's Hermitian convention. Everything downstream — Chapters 5, 6, 7, 8, 10 — uses these conventions.

## Content outline

1. Translation from Schwartz's Hermitian generators $T^a$ with $[T^a,T^b]=if^{abc}T^c$, $\tr(T^aT^b) = \tfrac{1}{2}\delta^{ab}$ to anti-Hermitian $t^a = -iT^a$ with $[t^a,t^b] = f^{abc}t^c$, $\tr(t^at^b) = -\tfrac{1}{2}\delta^{ab}$.
2. Connection one-form $A = A_\mu^a t^a\, dx^\mu$, translation $A_{\text{here}} = -iA_{\text{Schwartz}}$.
3. Field strength $F = dA + A\wedge A$; verify $A \wedge A \neq 0$ using $[t^a,t^b]$; express in components and show it equals the component formula $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu + [A_\mu, A_\nu]$.
4. Abelian case: $A \wedge A = 0$.

## Reuse opportunity

CS chapter Section 2.3 already has this. Use it as the verified template for Chapter 2.

## Steps

1. Adapt Section 2.3 from `chern_simons_theory.tex` into `paper/ch02_forms.tex`.
2. Add an up-front "Convention" box stating clearly: "Throughout Chapters 2–8 we use the anti-Hermitian convention. To translate to Schwartz's Hermitian convention, send $A \to -iA$ and $F \to -iF$."
3. Include the graded-commutator remark (factor of 2 between $[A,A]$ and $A\wedge A$).

## Acceptance criteria

- Conventions are stated explicitly and unambiguously up front.
- Every sign in the $F = dA + A \wedge A$ derivation is checked.
- The translation to Schwartz appears in a box or clearly marked paragraph.

## Risks

- **Sign confusion downstream.** If this chapter gets the conventions wrong, every chapter that uses connections breaks. Mitigation: when editing, verify against the already-debugged CS chapter.
