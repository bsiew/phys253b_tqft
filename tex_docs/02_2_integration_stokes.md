# Task 2.2 — Chapter 2 §2.2 Integration, Stokes, de Rham Cohomology

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Introduce integration of top forms on oriented manifolds, state Stokes's theorem (without full proof, with specific page reference to Nakahara), and define de Rham cohomology as the quotient $H^p = \ker d / \mathrm{im}\, d$.

## Content outline

1. Integration of top forms: $\int_M \omega = \int f(x)\, d^n x$ in local coordinates, with partition of unity for general manifolds.
2. Stokes: $\int_M d\omega = \int_{\partial M}\omega$.
3. Corollaries on closed manifolds.
4. Worked example: winding number of $f: S^1 \to S^1$.
5. de Rham cohomology and its topological meaning; cite de Rham's theorem (isomorphism with singular cohomology) without proof.

## Reuse opportunity

CS chapter Section 2.2 has most of this. Move it to Chapter 2.

## Steps

1. Copy Section 2.2 from `chern_simons_theory.tex` to `paper/ch02_forms.tex`.
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
