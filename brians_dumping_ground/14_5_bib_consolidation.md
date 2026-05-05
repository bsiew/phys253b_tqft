# Task 14.5 — Bibliography Consolidation

- **Status:** pending
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [VI](../stages/stage_VI_integration.md)

## Goal

Ensure every `\cite{}` resolves to an entry in `tqft_review.bib`, and every bib entry is actually cited somewhere.

## Steps

1. Grep every `\cite{KEY}` in `paper/*.tex`. Produce a list of unique keys.
2. Compare against `tqft_review.bib` entries.
3. Missing entries: add them (verify DOI first).
4. Orphan entries (present in bib, never cited): delete unless they're meant as "further reading".
5. Bib validation clean in the chosen build route (see [`plan/notes/build_route.md`](../notes/build_route.md)).
6. Cross-check: every entry has a year and either a DOI, an arXiv number, or a URL.

## Acceptance criteria

- No `\cite{}` produces `[?]` in the PDF.
- No orphan bib entries.
- Bib validation clean in the chosen build route (see [`plan/notes/build_route.md`](../notes/build_route.md)).
