---
created_at: "2026-05-05T17:30:58-04:00"
updated_at: "2026-05-05T17:47:47-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 14.2 — Chapter 14 §14.2 The Eta-Prime Mass and the Witten–Veneziano Formula

- **Status:** pending
- **Owner:** Helena
- **Duration:** 2.5 hr
- **Stage:** new (no BSIEW counterpart)

## Goal

Derive (sketch) the Witten–Veneziano relation and interpret $\chi_t^{YM}$ as a pure-gauge topological observable inferred from hadron spectroscopy.

## Content

1. **Puzzle.** In the large-$N$ limit with $N_f$ massless quarks, $U(N_f)_L \times U(N_f)_R$ is the chiral symmetry. Spontaneous breaking gives $N_f^2$ Goldstones. But the $\eta'$ is heavy ($\sim$958 MeV). Why?
2. **Witten–Veneziano formula.** $m_{\eta'}^2 + m_\eta^2 - 2m_K^2 = (2N_f/F_\pi^2)\,\chi_t^{YM}$. Interpret: the anomaly feeds a gauge-topology contribution into the meson mass matrix.
3. **Large-$N$ derivation sketch.** At leading order in $1/N$, $\chi_t^{YM}$ is the only source for the singlet mass. State the argument; do not reproduce the full Ward-identity chain.
4. **Lattice verification.** Cichy et al. 2015: quenched $\chi_t$ plus measured meson masses satisfy WV to within 10%. This is a topological observable extracted from spectroscopy.
5. **Holographic crosscheck.** Arean et al. 2021: holographic QCD models reproduce $\chi_t$ and the $\eta'$ mass in a framework where topology is encoded geometrically.

## Acceptance criteria

- WV formula stated with all mass terms identified.
- Large-$N$ counting argument (why the anomaly scales as $1/N$) stated in 1–2 paragraphs.
- Lattice and holographic support cited.
- ~4 pages.

## References

- Witten 1979
- Veneziano 1979
- Di Vecchia–Veneziano 1980
- Cichy et al. 2015 (lattice WV)
- Arean et al. 2021 (holographic $\chi_t$)

## Literature summaries (relative to `PROJECTS/QFT/`)

- `literature/1504.07954/codex_paper_summary.md` — Cichy et al. 2015 lattice WV test
- `literature/2105.00923/codex_paper_summary.md` — Arean et al. 2021 holographic U(1)_A / chi_t

## Dependencies

- §14.1 (definition of $\chi_t$, U(1)_A problem statement).

## Risks

- **Formalism creep.** Large-$N$ Ward identities are a rabbit hole. One paragraph of counting, then cite.
