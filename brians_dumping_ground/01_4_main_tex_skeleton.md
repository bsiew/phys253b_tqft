# Task 1.4 — Create `paper/main.tex` Skeleton

- **Status:** done (2026-05-03)
- **Owner:** Brian
- **Duration:** 45 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)
- **Priority:** core

## Result

Repository skeleton in place under `paper/`. Files committed:

| File | Purpose |
|---|---|
| `paper/main.tex` | `\documentclass{report}` master; `\includes` all 14 chapters + 5 appendices; `\bibliography{tqft_review}` |
| `paper/preamble.tex` | Shared preamble (macros + theorem environments mirroring the CS standalone source) |
| `paper/tqft_review.bib` | Bibliography seed (copied from `chern_simons_theory.bib`); Task 1.5 will extend |
| `paper/chern_simons_body.tex` | Auto-extracted content body of `chern_simons_theory.tex` (lines 95–1707, 1429 lines), preserves every proof unchanged |
| `paper/ch05_chern_simons.tex` | Wrapper: `\chapter{Chern--Simons theory}` + `\input{chern_simons_body}` |
| `paper/chern_simons_theory.tex` | **Untouched.** Standalone archival source remains compilable on its own |
| `paper/chNN_*.tex` × 13 | Chapter placeholders (Chs 1–4, 6–14) |
| `paper/appA-E_*.tex` × 5 | Appendix placeholders |
| `paper/figures/README.md` | Figure directory stub with policy and target file list |

## Verification performed

1. **Every `\include{}` in `main.tex` resolves** to a file on disk (all 19 targets present).
2. **Every `\cite{KEY}` in the CS body resolves** to a bib entry in `tqft_review.bib` (14 keys cited, 14 keys defined, zero missing).
3. **Label `prop:dimU1k`** referenced by the Ch 10 placeholder exists at line 1565 of `chern_simons_body.tex`; cross-reference will resolve after a two-pass compile.
4. **CS standalone source preserved.** `chern_simons_theory.tex` unchanged on disk (88,444 bytes, verified against the pre-task state).

## Not verified (deferred to Task 1.10)

- Actual `pdflatex` run. The workspace has no LaTeX toolchain yet; Task 1.10 settles the canonical build route, at which point `main.tex` should compile cleanly with warnings only for empty chapters.

## Goal

Commit a `paper/main.tex` that uses `\include` to assemble the whole paper. Every chapter file exists (even if it's a one-line placeholder saying "to be written"), and the result compiles cleanly in the chosen build route.

## Inputs

- `paper/chern_simons_theory.tex` (preserve as standalone archival compile target)
- Chapter list from `plan_of_attack.tex` Section 2

## File layout

```
paper/
  main.tex                 # master file, \includes everything
  preamble.tex             # Task 1.6 output
  tqft_review.bib          # Task 1.5 output
  figures/                 # Task 1.7 output
  ch01_intro.tex           # placeholder
  ch02_forms.tex           # placeholder
  ch03_axiomatic.tex       # placeholder
  ch04_frobenius.tex       # placeholder
  ch05_chern_simons.tex    # include-able wrapper
  chern_simons_theory.tex  # standalone archival source, preserved
  chern_simons_body.tex    # extracted body used by wrapper
  ch06_bf.tex              # placeholder
  ch07_dw.tex              # placeholder
  ch08_gensym.tex          # placeholder
  ch09_toporder.tex        # placeholder
  ch10_anyons.tex          # placeholder
  ch11_fqh.tex             # placeholder
  ch12_experiments.tex     # placeholder
  ch13_tqc.tex             # placeholder
  ch14_outlook.tex         # placeholder
  appA_category.tex        # placeholder
  appB_frobenius.tex       # placeholder
  appC_cs_level.tex        # placeholder
  appD_bf_zn.tex           # placeholder
  appE_tee.tex             # placeholder
```

## Placeholder content per chapter file

```latex
\chapter{...}
\label{ch:...}

\emph{To be drafted in Stage [II/III/IV/V] (Task [ref]).}
```

Use `report`-style chaptering in `main.tex`. The standalone CS file may remain `article`-style until the wrapper/body split is stable.

## Steps

1. Create the file structure above under `paper/`.
2. Write `main.tex` with `\documentclass{report}`, `\input{preamble}`, title, author, abstract placeholder, `\tableofcontents`, `\include{chNN_...}` lines.
3. For the existing CS chapter `chern_simons_theory.tex`: do not strip it destructively. Create a wrapper `ch05_chern_simons.tex` and an extracted body file `chern_simons_body.tex`, leaving the standalone file untouched until final integration.
4. Compile with the route chosen in Task 1.10. Expect warnings about empty chapters; confirm no hard errors.

## Acceptance criteria

- `paper/main.tex` compiles with zero hard errors in the chosen build route (warnings about empty chapters are acceptable).
- `main.pdf` has a title page, table of contents with all 14 chapters + 5 appendices, and one placeholder page per empty chapter.
- The CS chapter content appears correctly in place.

## Risks

- **Re-editing the CS chapter by accident.** Do not destructively rewrite `chern_simons_theory.tex` in this task.
- **Preamble conflicts.** The CS chapter's standalone preamble and the shared preamble will temporarily coexist. Mitigation: wrapper/body architecture first, final unification only after the multi-file paper compiles.
