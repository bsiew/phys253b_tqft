# Task 2.2 — Chapter 2 §2.2 Integration, Stokes, de Rham Cohomology

- **Status:** done (2026-05-04)
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)
- **Priority:** core

## Result

`paper/ch02_forms.tex` §2.2 drafted and appended. The de Rham cohomology material that had provisionally landed in §2.1 during Task 2.1 was relocated to §2.2 where it fits structurally alongside Stokes.

### Content delivered

1. **Orientation and integration of top forms:** local definition, partition-of-unity extension to general manifolds, linearity, restriction-to-submanifold integration.
2. **Remark on orientation reversal** as the source of the Chern--Simons action's parity-odd character.
3. **Stokes's theorem** (Theorem~\ref{thm:ch2-stokes}) stated, with three immediate corollaries: exact forms integrate to zero on closed manifolds (Corollary~\ref{cor:exact-to-zero}); closed-form integrals depend only on homology class (Corollary~\ref{cor:homology-dependence}); homotopy invariance (Corollary~\ref{cor:homotopy-invariance}).
4. **Worked example** of the winding number $f: S^1 \to S^1$ (Example~\ref{ex:ch2-winding}) with the integrality derivation fully spelled out: lift $\tilde f : [0, 2\pi] \to \R$, FTC, evaluate. Homotopy invariance follows immediately from Corollary~\ref{cor:homotopy-invariance}.
5. **Remark on the structural lesson** explicitly flagging that Chapter 5's level-quantization calculation is structurally identical.
6. **De Rham cohomology** (Definition~\ref{def:deRham}) and the de Rham--singular isomorphism (Theorem~\ref{thm:deRham-iso}, cited to Nakahara).
7. **Poincar\'e lemma** (Proposition~\ref{prop:poincare-lemma}, cited).
8. **Closing remark** explaining why de Rham cohomology underlies every integer-valued topological invariant in the paper (second Chern number, CS level, higher-form symmetry obstructions).

### Verification performed by hand

- Winding number integrality: $f^* d\theta = \tilde f'(t)\, dt$, $\int_0^{2\pi} \tilde f'(t)\, dt = \tilde f(2\pi) - \tilde f(0) = 2\pi n$. ✓
- Corollary 2.2.5 derivation: $\int_\Sigma \omega - \int_{\Sigma'}\omega = \int_{\partial\Omega}\omega = \int_\Omega d\omega = 0$ because $d\omega = 0$. ✓
- Degree-$n$ map $f(t) = e^{int}$ lifts to $\tilde f(t) = nt$ and contributes $n$ to the winding integer. ✓

### Citation hygiene

All Nakahara references in `ch02_forms.tex` are chapter-agnostic (`\cite{Nakahara2003GTP}` only), per the no-ghost-references rule. A tightening opportunity is recorded in `plan/notes/stage_III_trim_log.md` for Task 14.10: verify the actual chapter numbers in the 2003 second edition and add `[Ch.~X]` qualifiers.

### Verification-matrix rows added

C.2.7 through C.2.12.

### No new label collisions with `chern_simons_body.tex`.

## Goal

Introduce integration of top forms on oriented manifolds, state Stokes's theorem (without full proof, with specific page reference to Nakahara), and define de Rham cohomology as the quotient $H^p = \ker d / \mathrm{im}\, d$.

## Content outline

1. Integration of top forms: $\int_M \omega = \int f(x)\, d^n x$ in local coordinates, with partition of unity for general manifolds.
2. Stokes: $\int_M d\omega = \int_{\partial M}\omega$.
3. Corollaries on closed manifolds.
4. Worked example: winding number of $f: S^1 \to S^1$.
5. de Rham cohomology and its topological meaning; cite de Rham's theorem (isomorphism with singular cohomology) without proof.

## Reuse opportunity

CS chapter Section 2.2 has most of this. Use it as source material for Chapter 2 without forcing an early rewrite of Chapter 5.

## Steps

1. Adapt Section 2.2 from `chern_simons_theory.tex` into `paper/ch02_forms.tex`.
2. Verify the Stokes citation. Nakahara's Stokes theorem: check that it's in the 2003 2nd edition near Chapter 6. **Do not** cite a specific theorem number unless verified.
3. Verify the de Rham theorem citation similarly.

## Acceptance criteria

- Chapter 2 §2.2 exists with all content above.
- Every cross-reference to Nakahara is either page-verified or stated generically as "see Nakahara Chapter 6".
- The winding-number example is present as Example 2.4 or similar.

## Risks

- **Ghost citations.** This section is where we have historically introduced "Theorem X.Y of Nakahara" ghost references. **Before citing any specific theorem number, open the Nakahara PDF at `references/textbook/Nakahara_GeometryTopologyandPhysics.pdf` and verify.**

## References

- Nakahara 2003, Chapter 6 (Stokes, de Rham).
