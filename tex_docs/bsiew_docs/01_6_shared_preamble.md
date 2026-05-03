# Task 1.6 — Shared `paper/preamble.tex`

- **Status:** pending
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)

## Goal

Factor the preamble from `paper/chern_simons_theory.tex` into a shared `paper/preamble.tex` file that every chapter file can `\input`, so that macros, theorem environments, hyperref setup, and custom commands live in exactly one place.

## Inputs

- `paper/chern_simons_theory.tex` lines 1–84 (current preamble)
- `references/style references/hdr.tex` lines 1–250 (style reference)
- `references/style references/springer.tex` lines 1–250 (style reference)

## Steps

1. Copy lines 1–84 of `chern_simons_theory.tex` into `paper/preamble.tex`.
2. Replace the `\title{...}`, `\author{...}`, `\date{...}` block with a comment (those live in `main.tex`).
3. Remove `\begin{document}` (it lives in `main.tex`).
4. Cross-check against `hdr.tex`/`springer.tex`: the `\defthms{}` list in preamble should match the environments Brian actually uses in past papers. Current CS chapter list after Codex+our edits: `assumption, claim, construction, corollary, definition, example, exercise, fact, lemma, notation, proposition, question, remark, setup`. Confirm this is consistent with hdr/springer.
5. After Task 1.4 strips the CS chapter's preamble, ensure `chern_simons_theory.tex` starts directly with `\section{...}`.

## Acceptance criteria

- `paper/preamble.tex` exists.
- `main.tex` compiles with just `\input{preamble}` at the top.
- Chapter files that are `\include`d need no `\usepackage{}` lines.
- Environments `\begin{upshot}`, `\begin{note}`, `\begin{slogan}`, `\begin{motivation}`, `\begin{warning}`, `\begin{idea}`, `\begin{intuition}`, `\begin{terminology}` are NOT defined in the shared preamble. If any chapter file accidentally uses them, it errors loudly — this is the desired behavior.

## Risks

- **Macro collisions with TikZ.** If we later want `\newcommand{\delta}{...}` style redefinitions, they may collide with TikZ. Mitigation: introduce TikZ in Task 14.7, not here, so we don't fight both at once.
- **`numberwithin{theorem}{section}` vs `{chapter}`.** If `main.tex` uses `\documentclass{article}`, sections are top-level and numbering works. If `\documentclass{book}`, we'd need `\numberwithin{theorem}{chapter}`. Default to `article` to match Brian's past paper style.
