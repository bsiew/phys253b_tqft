---
created_at: "2026-05-05T17:30:59-04:00"
updated_at: "2026-05-05T17:47:48-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 14.3 — Chapter 14 §14.3 Strong CP, the Neutron EDM, and the Axion

- **Status:** pending
- **Owner:** Helena
- **Duration:** 3 hr
- **Stage:** new (no BSIEW counterpart)

## Goal

Connect bar-theta to the neutron EDM bound, introduce the PQ mechanism, and survey axion phenomenology at the level of experimental observables.

## Content

1. **Bar-theta.** $\bar\theta = \theta + \arg\det M_q$. Physical because it cannot be rotated away when quarks are massive.
2. **Neutron EDM.** $d_n \propto \bar\theta\, e\, m_*/(4\pi^2 F_\pi^2)$ (chiral estimate). Abel et al. 2020: $|d_n| < 1.8 \times 10^{-26}\,e\,\text{cm}$ implies $|\bar\theta| \lesssim 10^{-10}$.
3. **The fine-tuning problem.** Why is $\bar\theta$ so small? No SM mechanism sets it to zero.
4. **Peccei–Quinn mechanism.** Promote $\bar\theta \to a(x)/f_a$. The axion potential $V(a) = \chi_t(1 - \cos(a/f_a))$ has a minimum at $a = 0$; CP is dynamically restored.
5. **Axion mass.** $m_a^2 f_a^2 = \chi_t$. This is the same topological susceptibility from §14.1.
6. **Experimental landscape.** Mass–coupling plane: haloscopes (ADMX), helioscopes (CAST/IAXO), NMR (CASPEr), dielectric (MADMAX). State which region each probes; cite placeholders.
7. **KSVZ vs DFSZ.** Two benchmark UV completions differ in axion–photon and axion–electron couplings. The mass from $\chi_t$ is model-independent; the couplings are not.

## Acceptance criteria

- Bar-theta defined and nEDM bound stated numerically.
- PQ mechanism explained in 1 page (not a full symmetry-breaking derivation).
- Axion mass related back to $\chi_t$.
- Experimental landscape described by observable class (not individual experiment histories).
- ~5 pages.

## References

- Dine 2000 (TASI strong CP)
- Hook 2018 (TASI strong CP + axions)
- Marsh 2016 (axion cosmology)
- Abel et al. 2020 (nEDM)
- ADMX, CAST/IAXO, CASPEr, MADMAX placeholders

## Literature summaries (relative to `PROJECTS/QFT/`)

- `literature/hep-ph_0011376/codex_paper_summary.md` — Dine 2000 TASI Strong CP
- `literature/1812.02669/codex_paper_summary.md` — Hook 2018 TASI Strong CP + Axions
- `literature/1510.07633/codex_paper_summary.md` — Marsh 2016 Axion Cosmology
- `literature/2001.11966/codex_paper_summary.md` — Abel et al. 2020 nEDM measurement
- `literature/1804.05750/codex_paper_summary.md` — ADMX Gen 2 axion search (haloscope)
- `literature/2010.12076/codex_paper_summary.md` — BabyIAXO design (helioscope)
- `literature/1306.6089/codex_paper_summary.md` — CASPEr proposal
- `literature/1511.02867/codex_paper_summary.md` — NLO axion properties from ChPT
- `literature/1606.07494/codex_paper_summary.md` — Borsanyi et al. 2016 lattice axion mass

## Dependencies

- §14.1 ($\chi_t$ definition).
- §14.2 (WV establishes $\chi_t \neq 0$).

## Risks

- **Axion-cosmology tangent.** This is not a cosmology paper. State the misalignment mechanism in one sentence and cite Marsh 2016.
- **Model zoo.** Do not survey all axion models. KSVZ/DFSZ as benchmarks only.
