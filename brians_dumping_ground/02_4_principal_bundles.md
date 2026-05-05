# Task 2.4 — Chapter 2 §2.4 Principal Bundles (Minimum Viable)

- **Status:** done (2026-05-04)
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)
- **Priority:** core

## Result

`paper/ch02_forms.tex` §2.4 ``Principal bundles, connections, and global issues'' drafted and appended. File is now 516 lines. §2.4 is deliberately ~2 pages, state-level, with no Čech cocycles or reconstruction theorems.

### Content delivered

1. **§2.4.1 Informal definition:** principal $G$-bundle $P \to M$ with free right $G$-action and local trivializations. Transition functions $g_{UV}$ and local sections. One paragraph each.
2. **§2.4.2 Connection one-form on $P$:** the two axioms (vertical condition and equivariance under the right action) stated via \eqref{eq:vertical-axiom} and \eqref{eq:equivariance-axiom}, not derived.
3. **Definition~\ref{def:local-connection}:** local connection $A = s^* \omega$ via pullback along a section. Reconciles with the component notation of Definition~\ref{def:connection-one-form}.
4. **§2.4.3 Curvature:** total-space $\Omega = d\omega + \omega\wedge\omega$; statement that it is horizontal and equivariant; descent to base gives $F = s^*\Omega = dA + A\wedge A$ of \eqref{eq:F-as-pullback}.
5. **Proposition~\ref{prop:trivial-bundle-3-manifold}:** for $G$ compact simple simply connected and $M$ closed oriented 3-manifold, every principal $G$-bundle is trivial. Sketched via obstruction theory using $\pi_0(G) = \pi_1(G) = \pi_2(G) = 0$; full proof cited to Nakahara.
6. **Remark~\ref{rem:when-triviality-fails}:** the two canonical nontrivial-bundle examples — Dirac monopole ($U(1)$ over $S^2$, $\pi_1(U(1)) = \Z$) and Yang--Mills instanton ($SU(N)$ over $S^4$, $\pi_3(G) = \Z$). Both forward-pointed to Chapter 8.
7. **Remark~\ref{rem:nakahara-pointer}:** pointer to Nakahara for readers who want the full bundle story; flags that the full Chern--Simons machinery also has a bundle-theoretic version via Dijkgraaf--Witten's 4-manifold extension trick (forward to Chapter 7).

### What I verified by hand

| Claim | Check | ✓ |
|---|---|---|
| Principal $G$-bundles over $M$ classified by $[M, BG]$ | Standard algebraic-topology fact; cited | ✓ |
| $\pi_k(BG) = \pi_{k-1}(G)$ | Long exact sequence of $G \to EG \to BG$ | ✓ |
| For $G$ compact simple simply connected, $\pi_2(G) = 0$ | Classical theorem (Bott–Samelson) | ✓ |
| Obstruction theory: a map $M^3 \to X$ with $\pi_1(X) = \pi_2(X) = \pi_3(X) = 0$ wait— | Actually Proposition 2.4.6 uses $\pi_1(BG) = \pi_2(BG) = \pi_3(BG) = 0$, which requires $\pi_0(G) = \pi_1(G) = \pi_2(G) = 0$. For $G$ simply connected we get the first two; the third is the classical $\pi_2$ fact. Obstruction theory applied to a 3-dimensional CW complex needs vanishing $\pi_k(BG)$ for $k \leq 3$, which we have. Any such map is null-homotopic, so bundle is trivial. ✓ |
| Dirac monopole class = $\tfrac{1}{2\pi}\int_{S^2} F \in \Z$ | First Chern class integrality | ✓ |
| Instanton number = $\tfrac{1}{8\pi^2}\int_{S^4} \tr(F\wedge F) \in \Z$ | Second Chern class integrality | ✓ |

### Label collisions

None.

### Verification-matrix rows added

C.2.20 through C.2.23.

### Length check

§2.4 is 50 lines of LaTeX, well under the ~2-page cap. The forward-pointer strategy (Ch 5 cites §2.4 for triviality; Ch 8 cites §2.4 for the nontrivial-bundle examples) works cleanly.

## Goal

Introduce the minimum principal-bundle vocabulary that Chapter 5 (Chern–Simons) already assumes: connection, curvature on the total space vs. the base, trivial bundle over a simply-connected 3-manifold. Don't write a full principal-bundle theory.

## Content outline

1. Principal $G$-bundle $P \to M$ informally: at each point of $M$, a copy of $G$; transitions respect right $G$-action.
2. Connection one-form on $P$: a Lie-algebra-valued one-form satisfying equivariance + vertical-condition axioms (stated, not derived).
3. Local expression: pulling back to a section gives the $A = A_\mu^a t^a \, dx^\mu$ we already have.
4. Trivial bundle: if $G$ is simply connected and $M$ is any manifold, or if $\pi_1(M) = 0$, the principal $G$-bundle over $M$ is trivial. Cite Nakahara.
5. Why this matters: in Chapter 5 we work with $A \in \Omega^1(M, \mathfrak{g})$ globally; in Chapter 8 we need to know when this globality fails (nontrivial bundles ↔ instantons and magnetic monopoles).

## Steps

1. Write the section at ~2 pages.
2. Every claim either has a citation or is stated "we state without proof".
3. No principal-bundle reconstruction theorems, no Čech cocycles.

## Acceptance criteria

- 2 pages or less.
- Chapter 5 can cite Section 2.4 cleanly for "trivial bundle over simply connected $M$".
- Chapter 8's discussion of monopoles and nontrivial bundles has a hook to cite.

## Risks

- **Over-teaching bundles.** The temptation is to write a real bundle theory chapter. Resist. If the reader wants more, refer them to Nakahara Chapter 10.

## References

- Nakahara 2003, Chapter 10.
