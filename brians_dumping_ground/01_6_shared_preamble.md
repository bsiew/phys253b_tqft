# Task 1.6 — Shared `paper/preamble.tex`

- **Status:** done (2026-05-03)
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)
- **Priority:** core

## Result

`paper/preamble.tex` rewritten as the chapter-aware shared preamble. Changes from the Task 1.4 seed:

| Change | Reason |
|---|---|
| Fixed `\theHequation` to `\thechapter.\thesection.\arabic{equation}` | Prevents hyperref anchor collisions between chapters (report class); Task 1.4 seed still had the article-class form |
| Added `\theHconstruction`, `\theHexercise`, `\theHquestion` anchor aliases | Completes the alias table for every environment in `\defthms{}` |
| Deduplicated double `\usepackage{amsmath,amssymb,...}` | The CS standalone pulled amsmath/amssymb twice; consolidated into one ordered block |
| Reorganized packages into labeled groups | Core typesetting → math → figures/tables → diagrams → bibliography → hyperref |
| Added the "what does NOT live here" comment block | Documents that title/author/bibliography live in `main.tex`, and flags banned environments |

## Verification

1. **Environments used in the CS body** (`assumption, corollary, definition, example, lemma, proof, proposition, remark, setup, theorem`) are all defined by `\defthms{...}` or by `amsthm` directly.
2. **Environments used in chapter placeholders** — same 14 environments; all covered.
3. **Banned environments** (`upshot`, `note`, `slogan`, `motivation`, `warning`, `idea`, `intuition`, `terminology`) appear nowhere in the preamble. A stray `\begin{upshot}` in a chapter will error at compile time; this is the intended enforcement mechanism for `plan/README.md` rule #2.

## Kept despite minor deprecation concern

- `subfigure` is deprecated in favor of `subcaption`, but the CS body uses `subfigure` conventions. Keep for parity until integration; consider migrating in Task 14.7 along with figure work.
- `calligra` was dropped (was in the CS preamble but unused by any section of the CS body).

## Standalone source preserved

`paper/chern_simons_theory.tex` is unchanged. It compiles on its own with its own (article-class) preamble. `paper/preamble.tex` is for `main.tex` only.

## Goal

Factor the common preamble material into a shared `paper/preamble.tex` file that every chapter file can `\input`, while preserving the standalone compileability of `paper/chern_simons_theory.tex` until the integration architecture is stable.

## Inputs

- `paper/chern_simons_theory.tex` lines 1–84 (current preamble)
- `references/style references/hdr.tex` lines 1–250 (style reference)
- `references/style references/springer.tex` lines 1–250 (style reference)

## Steps

1. Copy the reusable preamble material from `chern_simons_theory.tex` into `paper/preamble.tex`.
2. Replace the `\title{...}`, `\author{...}`, `\date{...}` block with a comment (those live in `main.tex`).
3. Remove `\begin{document}` (it lives in `main.tex`).
4. Cross-check against `hdr.tex`/`springer.tex`: the `\defthms{}` list in preamble should match the environments Brian actually uses in past papers. Current CS chapter list after Codex+our edits: `assumption, claim, construction, corollary, definition, example, exercise, fact, lemma, notation, proposition, question, remark, setup`. Confirm this is consistent with hdr/springer.
5. Do not strip the CS chapter's standalone preamble in this task. Instead, make sure the wrapper/body split from Task 1.4 can consume `paper/preamble.tex` without breaking the archival source.

## Acceptance criteria

- `paper/preamble.tex` exists.
- `main.tex` compiles in the chosen build route with just `\input{preamble}` at the top.
- Chapter files that are `\include`d need no `\usepackage{}` lines.
- Environments `\begin{upshot}`, `\begin{note}`, `\begin{slogan}`, `\begin{motivation}`, `\begin{warning}`, `\begin{idea}`, `\begin{intuition}`, `\begin{terminology}` are NOT defined in the shared preamble. If any chapter file accidentally uses them, it errors loudly — this is the desired behavior.

## Risks

- **Macro collisions with TikZ.** If we later want `\newcommand{\delta}{...}` style redefinitions, they may collide with TikZ. Mitigation: introduce TikZ in Task 14.7, not here, so we don't fight both at once.
- **`numberwithin{theorem}{section}` vs `{chapter}`.** `main.tex` should use `report`-style chaptering, so theorem numbering must be checked deliberately rather than inherited from the standalone CS file.
