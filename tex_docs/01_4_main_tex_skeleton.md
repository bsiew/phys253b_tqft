# Task 1.4 — Create `paper/main.tex` Skeleton

- **Status:** pending
- **Owner:** Brian
- **Duration:** 45 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)

## Goal

Commit a `paper/main.tex` that uses `\include` to assemble the whole paper. Every chapter file exists (even if it's a one-line placeholder saying "to be written"), and the result compiles cleanly.

## Inputs

- `paper/chern_simons_theory.tex` (reuse as Chapter 5)
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
  chern_simons_theory.tex  # DRAFTED (do not edit in this task)
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

Chapter numbering matches the numbering in outline v3.

## Steps

1. Create the file structure above under `paper/`.
2. Write `main.tex` with `\documentclass{book}` or `\documentclass{article}` (match whatever the CS chapter uses — `article`), `\input{preamble}`, title, author, abstract placeholder, `\tableofcontents`, `\include{chNN_...}` lines.
3. For the existing CS chapter `chern_simons_theory.tex`: it is currently standalone. Create a wrapper version `ch05_chern_simons.tex` that does `\input{chern_simons_theory_body.tex}` where the body is the content between `\begin{document}` and `\end{document}`. Or, simpler, strip the preamble/`\begin{document}` from `chern_simons_theory.tex` when including — run a sed script that extracts body only.
4. Compile with `latexmk -pdf main.tex`. Expect warnings about empty chapters; confirm no errors.

## Acceptance criteria

- `paper/main.tex` compiles with zero errors (warnings about empty chapters are acceptable).
- `main.pdf` has a title page, table of contents with all 14 chapters + 5 appendices, and one placeholder page per empty chapter.
- The CS chapter content appears correctly in place.

## Risks

- **Re-editing the CS chapter by accident.** Don't touch `chern_simons_theory.tex`'s body; only move its preamble out.
- **Preamble conflicts.** The CS chapter's preamble has `\newtheorem` etc.; if `preamble.tex` (Task 1.6) also defines these, we'll get "already defined" errors. Mitigation: Task 1.6 is the single source of truth; delete the preamble from `chern_simons_theory.tex` after Task 1.6 runs.
