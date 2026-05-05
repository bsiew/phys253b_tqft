# Task 1.5 — Merged `paper/tqft_review.bib`

- **Status:** done (2026-05-03)
- **Owner:** Brian
- **Duration:** 45 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)
- **Priority:** core

## Result

`paper/tqft_review.bib` now contains 26 entries (grew from 14 at Task 1.4 seed). New entries added:

- `DijkgraafWitten1990` (restored, was dropped by the earlier revision)
- `Kock2004Frobenius` (Ch 4, App B main source)
- `Bhardwaj2023Lectures`, `FreedMooreTeleman2024` (Ch 8, outlook pointers)
- `Kitaev2003`, `NayakSimonSternFreedmanDasSarma2008` (anyons, TQC)
- `KitaevPreskill2006`, `LevinWen2006` (TEE, App E)
- `Werkmeister2025`, `Andersen2023` (experimental papers for Ch 12)
- `Ghosh2025`, `Ruelle2025` (optional 2025 follow-ups; author lists flagged for verification)

## Verification performed

1. **No duplicate keys.** 26 entries, 26 unique keys.
2. **Every non-book entry has a DOI, arXiv number, or URL** (via the bib-hygiene audit).
3. **Every `\cite{KEY}` in every included `.tex` still resolves** (14 keys cited by the CS body, all 14 defined; orphan count 0).
4. **12 "defined but not yet cited" entries** are the ones added in this task; they will be consumed by Chapters 6/7/8/9/10/11/12/13 when drafted. Expected state, not an error.

## Shopping list for external PDFs

Produced in `plan/notes/bibliography_pdf_shopping_list.md`. 8 "essential" arXiv PDFs to drop into `references/experiments/` and `references/textbook/`; 2 optional 2025 follow-ups; 2 journal-only papers worth grabbing if easy.

## Goal

Consolidate all bibliography entries the full paper will need into a single file, with verified DOIs/arXiv numbers.

## Inputs

- `paper/chern_simons_theory.bib` (existing, verified)
- `TQFT_outline (1).pdf` References section
- Additional sources flagged in `plan_of_attack.tex` Task 1.5 item list

## Expected entries beyond the CS bib

- **Atiyah 1988** — already in CS bib; keep.
- **Schwartz 2014** — already in CS bib; keep.
- **Witten 1989 Jones** — already in CS bib; keep.
- **Dijkgraaf–Witten 1990** — add back (was dropped from CS bib). Needed for Chapter 7.
- **Nakahara 2003 GTP** — already in CS bib; keep.
- **Tong QHE 2016** — already in CS bib; keep.
- **Freed CS notes 1995** — already in CS bib; keep.
- **Gaiotto–Kapustin–Seiberg–Willett 2015** (generalized symmetries) — already in CS bib; keep.
- **Callan–Harvey 1985** — already in CS bib; keep.
- **Nakamura et al 2020** (FQH interferometer) — already in CS bib; keep.
- **Kitaev 2003** (fault-tolerant quantum computation by anyons) — **add.**
- **Nayak–Simon–Stern–Freedman–Das Sarma 2008** (non-abelian anyons RMP) — **add.**
- **Kitaev–Preskill 2006** (topological entanglement entropy) — **add.**
- **Levin–Wen 2006** (detecting TO in ground state wavefunction) — **add.**
- **Werkmeister et al 2025** (graphene interferometer) — **add.**
- **Andersen et al 2023** (non-abelian braiding on superconducting processor) — **add.**
- **Ghosh et al 2025** and **Ruelle et al 2025** — optional follow-up experimental entries if used in Chapter 12.
- **Freed–Moore–Teleman 2024** (topological symmetry) — **add.** Used in outlook + Ch 8 SymTFT pointer.
- **Bhardwaj et al 2023** (lectures on generalized symmetries) — **add.** Pedagogical citation in Ch 8.
- **Kock, "Frobenius Algebras and 2D TQFTs" 2004** — **add.** Used in Ch 4 and Appendix B.
- **Nayak et al RMP 2008** — **add.** Used in Ch 13.

## Steps

1. Copy `chern_simons_theory.bib` → `paper/tqft_review.bib`.
2. Append the new entries above. For each, verify the DOI by searching the DOI system, and include an `arXiv:` note where applicable.
3. Run `biber --validate-datamodel paper/tqft_review.bib` if the chosen build route supports it, and fix any errors.
4. Keep `chern_simons_theory.bib` until the CS wrapper/body architecture is stable. Only then switch the integrated paper to `tqft_review.bib`.

## Acceptance criteria

- `paper/tqft_review.bib` exists with all ~20 entries.
- `biber --validate-datamodel` passes, or an equivalent bib validation check is performed in the chosen build route.
- DOIs verified for at least the experimental entries (Nakamura, Werkmeister, Andersen) and the review entries actually used in the paper.

## Risks

- **Wrong DOIs.** Verify by clicking through the resolver, not by trusting ArXiv listings alone.
- **Andersen 2023 citation.** Prefer the journal version; keep the arXiv only as a secondary note if useful.
- **Kock book vs. notes.** There's a short 2004 book ("A Short Introduction to 2-Dimensional Topological Quantum Field Theories") and earlier lecture notes. Cite the book.
