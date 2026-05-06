---
created_at: "2026-05-05T17:31:55-04:00"
updated_at: "2026-05-05T17:48:40-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 15.1 — Chapter 15 §15.1 Monopoles, Line Operators, and Global Structure

- **Status:** pending
- **Owner:** Helena
- **Duration:** 3 hr
- **Stage:** new (no BSIEW counterpart)

## Goal

Treat the "defect / global-structure" observable family in one place: Dirac and 't Hooft–Polyakov monopoles, Wilson and 't Hooft lines, and how line-operator spectra probe the global form of the gauge group.

## Content

1. **Dirac monopoles.** Charge quantization as a topological consistency condition ($eg = n/2$). Singular string, Dirac's argument, connection to $\pi_1(U(1))$.
2. **'t Hooft–Polyakov monopoles.** Finite-energy solitons with maps $S^2_\infty \to G/H$; classified by $\pi_2(G/H)$. Use notation from Part I Sec. 2.5. Contrast: Dirac singular vs 't Hooft–Polyakov smooth.
3. **Magnetic charge sector is NOT a topological theory.** The soliton exists in a full Yang–Mills–Higgs theory with local propagating modes. The topological sector number (magnetic charge) is robust, but the embedding theory is metric-dependent.
4. **Wilson and 't Hooft lines.** Define Wilson loop $W_R(\gamma) = \tr_R\,\mathcal{P}\exp\oint A$. 't Hooft line as the magnetic dual. Mutual locality condition: which lines can coexist determines the global form ($SU(N)$ vs $SU(N)/\mathbb{Z}_N$).
5. **Preview of generalized symmetries.** One paragraph: line operators generate 1-form symmetries in the sense of Gaiotto–Kapustin–Seiberg–Willett 2015. This is how the "defect family" of observables connects to the modern language. Do NOT develop the full formalism — only the bridge sentence.

## Acceptance criteria

- Dirac quantization stated with derivation sketch (patching argument from Sec. 2).
- 't Hooft–Polyakov: existence from $\pi_2(G/H) \neq 0$, one worked example (SU(2) $\to$ U(1)).
- Wilson/'t Hooft line mutual locality stated; example: $SU(2)$ vs $SO(3)$ gauge theory.
- Clear statement: magnetic charge is topological, but the theory hosting it is not a TQFT.
- ~6 pages.

## References

- Dirac 1931
- 't Hooft 1974
- Polyakov 1974
- Manton–Sutcliffe (Topological Solitons)
- Shnir (Magnetic Monopoles)
- Weinberg (Classical Solutions in QFT)
- Rajantie 2024 (review)
- Fairbairn et al. 2021
- PDG Monopoles
- GKSW 2015 (generalized symmetries)
- Kapustin–Saulina (line operators)

## Literature summaries (relative to `PROJECTS/QFT/`)

- `literature/2411.05753/codex_paper_summary.md` — Rajantie 2024 monopole theory overview
- `literature/2005.05100/codex_paper_summary.md` — Fairbairn et al. 2021 Magnetic Monopoles Revisited
- `literature/1412.5148/codex_paper_summary.md` — GKSW 2015 Generalized Global Symmetries
- `literature/hep-th_0604151/codex_paper_summary.md` — Kapustin–Witten 2007 Electric-Magnetic Duality / Langlands

## Dependencies

- Part I Sec. 2 (homotopy groups, fiber bundles, patching).
- Ch 14 (establishes the 3+1d gauge-theory context).

## Risks

- **Overweight.** Monopoles are a monograph topic. Keep to one example per construction. The worked example is SU(2) $\to$ U(1); do not also do SU(5) $\to$ SM.
- **Generalized-symmetries rabbit hole.** One bridge paragraph, max. The formalism is deferred to Part I Ch 8 (when written).
