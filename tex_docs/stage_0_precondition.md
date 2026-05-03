# Stage 0 — Precondition (complete)

**Status:** done (as of 2026-04-30).

This stage documents what existed before the plan was created, so that subsequent stages have a clean starting point.

## Artifacts in place

| Artifact | Path | Status |
|---|---|---|
| Chern–Simons chapter | `paper/chern_simons_theory.tex` | Drafted, ~25 pp, matches style references |
| Chern–Simons bibliography | `paper/chern_simons_theory.bib` | Drafted, no orphans, no ghost refs |
| Outline v1 (PS4 submission) | `TQFT_outline (1).pdf` | Submitted for PS4 Problem 1 |
| Outline v2 (revised) | `TQFT_outline_v2.tex` | Working doc with deep/survey/bridge tags |
| Style references | `references/style references/hdr.tex`, `springer.tex` | Brian's past-paper style; all new chapters match these |
| Schwartz textbook | `references/textbook/Matthew_D_Schwartz_Quantum_Field_Theory_And_The_Standard_Model.pdf` | Reader baseline: through Chapter 30 |
| Extra textbooks | `references/textbook/Nakahara_GeometryTopologyandPhysics.pdf`, `Tong_GaugeTheory.pdf`, `Freed_DifferentialGeometryNotes.pdf`, `Freed_ChernSimonsTheoryNotes.pdf` | For targeted lookups, not for cover-to-cover reading |

## Calculations already verified inside the CS chapter

- $d\omega_{CS} = \tr(F \wedge F)$ — expansion matches, signs track.
- $\omega_{CS}(A^g) - \omega_{CS}(A) = -\tfrac{1}{3}\tr(\theta^{\wedge 3}) + d(\cdots)$ — all four steps of the derivation close.
- $\int_{SU(2)} \tr((g^{-1}dg)^{\wedge 3}) = 24\pi^2$ — Euler-angle evaluation, everything matches.
- $\dim \mathcal{H}_{U(1),k}(T^2) = k$ — finite Heisenberg algebra derivation.
- $F^g = g^{-1}Fg$ — template calculation, all mixed terms cancel.
- Abelian Wilson-loop linking phase derivation.

## What Stage I should not re-do

- Do not edit `paper/chern_simons_theory.tex` unless Stage VI proofreading turns up an error.
- Do not re-derive any calculation already in the CS chapter — cite it from the new chapters instead.
- Do not re-extend the bibliography with CS citations — append Stage I new citations to a merged bib.

## Dependencies flowing out of Stage 0

- Chapter 5 (Chern–Simons) is done. Chapters 2, 6, 7, 8, 10, 11 will reuse material from it; each dependency is enumerated in the relevant task file.
- The style preamble (macros, theorem environments, hyperref setup) is the one used in `paper/chern_simons_theory.tex`. Stage I Task 1.6 moves this into a shared file.
