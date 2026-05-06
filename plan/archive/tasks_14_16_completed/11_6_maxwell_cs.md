# Task 11.6 — Chapter 11 §11.6 Maxwell–Chern–Simons: When a CS Term Is Not a TQFT

- **Status:** pending
- **Owner:** Helena
- **Duration:** 90 min
- **Stage:** [IV](../../llm_docs/bsiew_plan/stage_IV_partII_A.md)

## Goal

Explain why adding a Chern–Simons term to a dynamical gauge theory does NOT produce a TQFT. The Hodge star reintroduces metric dependence, the propagator acquires a topologically massive pole, and observables depend on distances. This subsection is the contrast that makes the purity of the pure CS action conceptually sharp.

## Content

1. **Maxwell-CS action.** $S = -(1/4e^2) \int F \wedge \star F + (k/4\pi) \int A \wedge dA$.
2. **Topologically massive pole.** The propagator has mass $m_{\text{CS}} = k e^2 / (2\pi)$. At distances $\gg 1/m_{\text{CS}}$ the theory looks topological; at shorter scales it looks like electrodynamics with a gap.
3. **NOT a TQFT.** The Hodge star $\star$ depends on the metric. Observables depend on the metric. Local propagating modes exist. Contrast with pure CS where $F = 0$ on-shell.
4. **Physical use.** Finite-thickness edge model, finite-temperature regularization of pure CS, realistic condensed-matter effective theories.
5. **Lesson.** The purity of the CS action is what makes the observables topological. Adding dynamics destroys that.

## Acceptance criteria

- Maxwell-CS action written and contrasted with pure CS.
- Topological mass scale identified.
- Statement: this is NOT a TQFT, and why.
- ~2 pages.

## References

- Dunne 1999 (MCS treatment).
- Wen 1995 (edge theory as MCS limit).
- Birmingham et al. 1991 (TQFT classification).

## Source material

- `archive_2026-05-01/anomalies_boundaries_topological_response.tex` lines ~500–600.

## Risks

- **Over-derivation.** Don't derive the full propagator from scratch. State the pole and cite Dunne.
