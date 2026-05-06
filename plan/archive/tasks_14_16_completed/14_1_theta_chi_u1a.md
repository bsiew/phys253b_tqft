---
created_at: "2026-05-05T17:30:57-04:00"
updated_at: "2026-05-05T17:47:46-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 14.1 — Chapter 14 §14.1 Theta Vacua, Topological Susceptibility, and U(1)_A

- **Status:** pending
- **Owner:** Helena
- **Duration:** 3 hr
- **Stage:** new (no BSIEW counterpart)

## Goal

Open the 3+1d chapter by deriving topological susceptibility as the curvature of the vacuum energy and explaining why U(1)_A fails as a Goldstone symmetry.

## Content

1. **Instanton number recap.** Remind reader that Part I Sec. 3 introduced $\nu = (1/32\pi^2)\int \tr(F \wedge F)$. Here we follow the chain from topology to measurable observables.
2. **Topological charge density.** Define $q(x) = (g^2/32\pi^2)\tr(F_{\mu\nu}\tilde{F}^{\mu\nu})$ and the topological susceptibility $\chi_t = \int d^4x\,\langle q(x)\,q(0)\rangle$.
3. **Vacuum energy curvature.** $E(\theta) = E(0) + \tfrac{1}{2}\chi_t\,\theta^2 + O(\theta^4)$ at small $\theta$.
4. **U(1)_A problem.** Anomaly kills the naive ninth Goldstone; without instantons the $\eta'$ would be as light as the pion. Large-$N$ expansion saves the story: $\chi_t^{YM} \neq 0$ at $N_f = 0$ ensures the mass gap.
5. **Theta vacua.** $|\theta\rangle = \sum_\nu e^{i\nu\theta}|\nu\rangle$; cluster decomposition selects one $\theta$.

## Acceptance criteria

- $\chi_t$ defined operationally and related to $E(\theta)$.
- U(1)_A anomaly stated (not derived from scratch — cite 't Hooft).
- Large-$N$ counting argument stated at the level of Witten 1979.
- ~5 pages.

## References

- 't Hooft 1976 (Bell–Jackiw; Pseudoparticle)
- Witten 1979 (U(1) Goldstone boson)
- Veneziano 1979 (U(1) without instantons)
- Di Vecchia–Veneziano 1980 (chiral dynamics with theta)
- Teper 2000 (lattice topology review)

## Literature summaries (relative to `PROJECTS/QFT/`)

- `literature/hep-ph_0011376/codex_paper_summary.md` — Dine 2000 TASI Strong CP
- `literature/hep-lat_9909124/codex_paper_summary.md` — Teper 2000 Topology in QCD
- `literature/1812.02669/codex_paper_summary.md` — Hook 2018 TASI Strong CP + Axions

## Dependencies

- Part I Sec. 3 (instanton number definition, Chern–Weil).

## Risks

- **Over-deriving instantons.** This is a review paper, not a QCD textbook. State the semiclassical formula and cite; do not re-derive the instanton action.
- **Conflating YM and full-QCD chi_t.** Be explicit about quenched vs unquenched.
