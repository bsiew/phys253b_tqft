# Verification Matrix

Living ledger of every non-trivial mathematical claim in the paper. This is the operational implementation of the professor's rubric line "You are responsible for the correctness of the results in the review."

Task 1.12 seeds this file; each chapter drafting task appends new claims as it goes; Task 14.9 (math proofreading pass) reads down this matrix and flips `unverified` rows to `verified` or escalates problems.

## Status tags

- `derived-here`: full derivation in the paper body.
- `derived-elsewhere`: derived in another chapter or appendix with explicit cross-reference.
- `moved-to-appendix`: full derivation in an appendix; main text has the statement.
- `cited`: stated with a primary-source citation and not re-derived.
- `unverified`: claim exists in the draft but no verification step has been run. Must disappear before Task 14.9 closes.
- `cut`: considered and dropped; keep the row so we don't re-derive by accident.

## Claims (seeded from Chapter 5 `paper/chern_simons_theory.tex`)

| ID | Claim | Chapter/§ | Status | Source / location |
|---|---|---|---|---|
| C.5.1 | $\tr(F \wedge F) = d\,\omega_{\CS}(A)$ | Ch 5 §3 | `derived-here` | Proposition~\ref{prop:CS-form} in `chern_simons_body.tex` |
| C.5.2 | $F^g = g^{-1} F g$ under $A \to A^g$ | Ch 5 §2 | `derived-here` | §2.5 of `chern_simons_body.tex` |
| C.5.3 | $\omega_{\CS}(A^g) - \omega_{\CS}(A) = -\tfrac{1}{3}\tr(\theta^{\wedge 3}) + d\tr(g(dg^{-1})\wedge A)$ | Ch 5 §3 | `derived-here` | Proposition~\ref{prop:CS-gauge} |
| C.5.4 | Maurer-Cartan: $d\theta = -\theta \wedge \theta$ | Ch 5 §3 | `derived-here` | Lemma~\ref{lem:MC} |
| C.5.5 | $\int_{SU(2)} \tr((g^{-1}dg)^{\wedge 3}) = 24\pi^2$ | Ch 5 §5 | `derived-here` | Euler-angle calculation, Eqs. 5.5.26--30 |
| C.5.6 | Level quantization $k \in \mathbb{Z}$ for $G = SU(2)$ | Ch 5 §5 | `derived-here` | Theorem~\ref{thm:level-quantization-su2} |
| C.5.7 | Level quantization $k \in \mathbb{Z}$ for general compact simple simply connected $G$ | Ch 5 §5 | `cited` | Remark~\ref{rmk:general-group}; not re-derived |
| C.5.8 | Abelian CS two-loop correlator $\langle W_{q_1}(C_1) W_{q_2}(C_2) \rangle = e^{-2\pi i q_1 q_2 \mathrm{Lk}/k}$ | Ch 5 §6 | `derived-here` | Example~\ref{ex:abelian-wilson}, completing-the-square argument |
| C.5.9 | $\dim \mathcal{H}_{U(1),k}(T^2) = k$ | Ch 5 §7 | `derived-here` | Finite Heisenberg algebra, Proposition~\ref{prop:dimU1k} |
| C.5.10 | Atiyah-Segal axioms force $\dim Z(\Sigma) < \infty$ | Ch 5 §8 | `cited` | Cited to Atiyah 1988; Chapter 3 will re-derive via cylinder trace |
| C.2.1 | Graded commutativity $\alpha\wedge\beta = (-1)^{pq}\beta\wedge\alpha$ | Ch 2 §2.1 | `derived-here` | Proposition~\ref{prop:graded-comm} in `ch02_forms.tex`; proof by counting adjacent transpositions |
| C.2.2 | Leibniz rule $d(\alpha\wedge\beta) = (d\alpha)\wedge\beta + (-1)^p\,\alpha\wedge(d\beta)$ | Ch 2 §2.1 | `derived-here` | Lemma~\ref{lem:ch2-leibniz-nilpotent} in `ch02_forms.tex`; direct index computation |
| C.2.3 | $d^2 = 0$ on smooth forms | Ch 2 §2.1 | `derived-here` | Lemma~\ref{lem:ch2-leibniz-nilpotent}; symmetric-antisymmetric contraction argument |
| C.2.4 | Bianchi identity $dF = 0$ for $F = dA$ | Ch 2 §2.1, Example~\ref{ex:maxwell-forms} | `derived-here` | Immediate consequence of $d^2 = 0$ |
| C.2.5 | $U(1)$ gauge invariance of $F$ | Ch 2 §2.1, Example~\ref{ex:gauge-invariance-F} | `derived-here` | Immediate consequence of $d^2 = 0$ |
| C.2.6 | de Rham--singular cohomology isomorphism | Ch 2 §2.2 | `cited` | Theorem~\ref{thm:deRham-iso} in `ch02_forms.tex`; cited to Nakahara 2003 |
| C.2.7 | Stokes's theorem $\int_M d\omega = \int_{\partial M}\omega$ | Ch 2 §2.2 | `cited` | Theorem~\ref{thm:ch2-stokes}; cited to Nakahara 2003 |
| C.2.8 | Exact forms integrate to zero on closed manifolds | Ch 2 §2.2 | `derived-here` | Corollary~\ref{cor:exact-to-zero}; immediate from Stokes |
| C.2.9 | Closed-form integrals depend only on homology class | Ch 2 §2.2 | `derived-here` | Corollary~\ref{cor:homology-dependence}; Stokes + $d\omega = 0$ |
| C.2.10 | Homotopy invariance for closed forms: $\int_N f_0^*\omega = \int_N f_1^*\omega$ | Ch 2 §2.2 | `cited` | Corollary~\ref{cor:homotopy-invariance}; proof via Cartan's magic formula cited to Nakahara |
| C.2.11 | Winding number $n(f) = \tfrac{1}{2\pi}\int_{S^1} f^*d\theta \in \Z$ for $f:S^1\to S^1$, homotopy-invariant | Ch 2 §2.2 | `derived-here` | Example~\ref{ex:ch2-winding}; explicit lift $\tilde f$ + FTC |
| C.2.12 | Poincar\'e lemma: closed forms on star-shaped $U \subseteq \R^n$ are exact | Ch 2 §2.2 | `cited` | Proposition~\ref{prop:poincare-lemma}; cited to Nakahara 2003 |
| C.2.13 | Anti-Hermitian bracket: $[t^a, t^b] = f^{abc} t^c$ given Schwartz's Hermitian $[T^a, T^b] = if^{abc}T^c$ and $t^a = -iT^a$ | Ch 2 §2.3 | `derived-here` | Proposition~\ref{prop:anti-herm-identities}; two-line direct computation |
| C.2.14 | Anti-Hermitian trace: $\tr(t^a t^b) = -\tfrac{1}{2}\delta^{ab}$ | Ch 2 §2.3 | `derived-here` | Proposition~\ref{prop:anti-herm-identities} |
| C.2.15 | $A\wedge A = \tfrac{1}{2}[A_\mu, A_\nu]\, dx^\mu\wedge dx^\nu$ for Lie-algebra-valued connection one-form | Ch 2 §2.3 | `derived-here` | Proposition~\ref{prop:AwedgeA}; symmetric/antisymmetric decomposition of $A_\mu^a A_\nu^b\, t^a t^b$ |
| C.2.16 | Non-abelian field strength $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu + [A_\mu, A_\nu]$ | Ch 2 §2.3 | `derived-here` | Proposition~\ref{prop:F-components}; combines Prop.~\ref{prop:AwedgeA} with $dA$ component formula |
| C.2.17 | Convention translation $F_{\text{here}} = -i\, F_{\text{Schwartz}}$ | Ch 2 §2.3 | `derived-here` | Remark~\ref{rem:schwartz-comparison}; explicit substitution $A_\mu = -i A_\mu^{\text{Sch}}$ |
| C.2.18 | Graded-commutator factor: $[A, A] = 2\, A\wedge A$ for one-forms | Ch 2 §2.3 | `derived-here` | Remark~\ref{rem:AwedgeA-factor}; specialization of Definition~\ref{def:graded-commutator} |
| C.2.19 | Abelian case: $A\wedge A = 0$, so $F = dA$ | Ch 2 §2.3 | `derived-here` | Remark~\ref{rem:abelian-case}; $f^{abc} = 0$ kills the cubic correction |
| C.2.20 | Curvature on the total space, $\Omega = d\omega + \omega\wedge\omega$, descends to $F = s^*\Omega = dA + A\wedge A$ on the base | Ch 2 §2.4 | `cited` | Eq.~\ref{eq:F-as-pullback}; horizontality and equivariance of $\Omega$ cited to Nakahara |
| C.2.21 | Trivial-bundle hypothesis: every principal $G$-bundle over a closed oriented 3-manifold $M$ is trivial, for $G$ compact simple simply connected | Ch 2 §2.4 | `cited` | Proposition~\ref{prop:trivial-bundle-3-manifold}; obstruction-theory argument using $\pi_0(G) = \pi_1(G) = \pi_2(G) = 0$ cited to Nakahara |
| C.2.22 | $U(1)$-bundles over $S^2$ classified by $\pi_1(U(1)) = \Z$ $\Rightarrow$ Dirac monopole charge | Ch 2 §2.4 | `cited` | Remark~\ref{rem:when-triviality-fails}; referenced forward to Ch 8 |
| C.2.23 | $SU(N)$-bundles over $S^4$ classified by $\pi_3(G) = \Z$ $\Rightarrow$ instanton number $\tfrac{1}{8\pi^2}\int_{S^4}\tr(F\wedge F)$ | Ch 2 §2.4 | `cited` | Remark~\ref{rem:when-triviality-fails}; connects to Schwartz Ch 30 and Ch 5 level quantization |
| C.2.24 | $dg^{-1} = -g^{-1}(dg)g^{-1}$ | Ch 2 §2.5 | `derived-here` | Lemma~\ref{lem:dginv}; differentiate $g^{-1}g = \mathbf{1}$ |
| C.2.25 | Maurer-Cartan equation: $d\theta + \theta\wedge\theta = 0$ for $\theta = g^{-1}dg$ | Ch 2 §2.5 | `derived-here` | Lemma~\ref{lem:maurer-cartan}; uses $d^2 = 0$ and Lemma~\ref{lem:dginv} |
| C.2.26 | Gauge transformation of field strength: $F^g = g^{-1}Fg$ for $A^g = g^{-1}Ag + g^{-1}dg$ | Ch 2 §2.5 | `derived-elsewhere` | Theorem~\ref{thm:F-transformation}; only a sketch in Ch 2. The fully explicit three-pair cancellation is executed in Chapter~\ref{ch:chern-simons} where the same argument runs for $\omega_{\CS}$. |
| C.2.27 | Non-abelian Bianchi identity $dF + [A, F] = 0$ | Ch 2 §2.3 eq.~\ref{eq:nonabelian-bianchi} | `cut` | Stated without derivation in §2.3 as \eqref{eq:nonabelian-bianchi}; no downstream `\ref` by any chapter, so no proof given. If it becomes load-bearing in some later chapter, re-derive there. |
| C.2.28 | Infinitesimal gauge transformation: $\delta A = d\varepsilon + [A, \varepsilon] = D\varepsilon$, $\delta F = [F, \varepsilon]$ | Ch 2 §2.5 | `derived-here` | Remark~\ref{rem:infinitesimal-gauge}; first-order expansion of $A^g = g^{-1}Ag + g^{-1}dg$ |
| C.2.29 | Topological/dynamical dichotomy: $dF=0$ (Bianchi) needs only $d,\wedge$; $d\star F = \star J$ (inhomogeneous) is metric-dependent via Hodge star | Ch 2 §2.1, Example~\ref{ex:maxwell-forms} | `derived-here` (Bianchi) + `cited` (Hodge construction) | Dichotomy is the organizing principle of Schwartz vs Chern-Simons; Hodge star construction cited to Nakahara |

## Claims to be added

As Chapters 2, 3, 4, 6--14 and Appendices A--E are drafted, each chapter's drafting task MUST append its non-trivial claims here before marking itself complete. Expected seeds by chapter:

- **Ch 2:** Leibniz rule, $d^2 = 0$, Stokes, de Rham--singular isomorphism (`cited`)
- **Ch 3:** Atiyah-Segal axioms; cylinder = identity ⟹ $\dim Z(\Sigma) < \infty$
- **Ch 4:** 2D classification theorem (Frobenius), $Z(\Sigma_g) = \sum \lambda_i^{2-2g}$
- **Ch 6:** Compact $U(1)$ BF at level $N$ equals $\mathbb{Z}_N$ gauge theory; GSD $= N^{2g}$
- **Ch 7:** $H^3(\mathbb{Z}_N, U(1)) = \mathbb{Z}_N$
- **Ch 8:** Chiral anomaly as boundary of 5D CS bulk; FQH edge anomaly inflow
- **Ch 9:** Toric code GSD $=4$ on the torus
- **Ch 10:** $S$-matrix for $U(1)_k$ is a discrete Fourier transform; Verlinde $\dim \mathcal{H}_{SU(2),k}(T^2) = k+1$ (`cited`, not derived)
- **Ch 11:** $\sigma_{xy} = e^2/(mh)$ from $U(1)_m$ CS; quasi-particle braiding phase $= 2\pi/m$
- **App D:** Full $H^3(\mathbb{Z}_N, U(1)) = \mathbb{Z}_N$ via bar resolution
- **App E:** Kitaev-Preskill subtraction ⟹ $\gamma = \log \mathcal{D}$; $\mathcal{D}$ values for toric code, Laughlin $\nu = 1/m$, Ising

## Rules

1. **Append, do not overwrite.** If a claim is revised, add a new row and tag the old row `cut`.
2. **Every `derived-here` row cites its equation or theorem label.** The label must be resolvable in the compiled PDF.
3. **Every `cited` row names the primary source.** Secondary citations are not sufficient.
4. **Task 14.9 (math proof pass) is gated on this matrix reaching zero `unverified` rows.** No row is removed at 14.9; only status flips.
