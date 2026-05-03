# Task 1.5 — Merged `paper/tqft_review.bib`

- **Status:** pending
- **Owner:** Brian
- **Duration:** 45 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)

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
- **Werkmeister et al 2024** (graphene interferometer) — **add.**
- **Andersen et al 2023** (non-abelian braiding on superconducting processor) — **add.**
- **Freed–Moore–Teleman 2024** (topological symmetry) — **add.** Used in outlook + Ch 8 SymTFT pointer.
- **Bhardwaj et al 2023** (lectures on generalized symmetries) — **add.** Pedagogical citation in Ch 8.
- **Kock, "Frobenius Algebras and 2D TQFTs" 2004** — **add.** Used in Ch 4 and Appendix B.
- **Nayak et al RMP 2008** — **add.** Used in Ch 13.

## Steps

1. Copy `chern_simons_theory.bib` → `paper/tqft_review.bib`.
2. Append the new entries above. For each, verify the DOI by searching the DOI system, and include an `arXiv:` note where applicable.
3. Run `biber --validate-datamodel paper/tqft_review.bib` and fix any errors.
4. Delete `chern_simons_theory.bib` and update the CS chapter's `\bibliography{}` line to point to `tqft_review` (when the CS chapter is absorbed into `main.tex`).

## Acceptance criteria

- `paper/tqft_review.bib` exists with all ~20 entries.
- `biber --validate-datamodel` passes.
- DOIs verified for at least the experimental entries (Nakamura, Werkmeister, Andersen) and the review entries (GKSW, Bhardwaj, FMT).

## Risks

- **Wrong DOIs.** Verify by clicking through the resolver, not by trusting ArXiv listings alone.
- **Andersen 2023 citation.** This is preprint vintage; include `arXiv:2210.10255` or equivalent and a journal version if one exists.
- **Kock book vs. notes.** There's a short 2004 book ("A Short Introduction to 2-Dimensional Topological Quantum Field Theories") and earlier lecture notes. Cite the book.
