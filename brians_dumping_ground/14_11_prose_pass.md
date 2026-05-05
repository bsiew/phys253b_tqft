# Task 14.11 — Prose Pass and AI-Tell Purge

- **Status:** pending
- **Owner:** Brian + Helena
- **Duration:** 2 hours
- **Stage:** [VI](../stages/stage_VI_integration.md)

## Goal

Strip AI-sounding phrases from the whole paper. Get transitions and sentence rhythms in Brian's style (see `references/style references/hdr.tex`, `springer.tex`).

## Banned phrases

Run a find on the whole paper for each and replace when they read as AI filler rather than natural mathematical prose:

- "we shall see"
- "in this chapter we have proved"
- "the key statement is"
- "an upshot of all this is"
- "it can be seen"
- "it is easy to see"
- "it is easy to verify"
- "it can be verified"
- "an important observation"
- "as we shall see"

## Style reference checks

- Brian uses `\medskip` liberally for paragraph breaks inside proofs — ensure this is preserved.
- Brian's `\textbf{Theorem/Lemma/Proposition 1.2.3}` referencing style — cross-check.
- No `upshot`, `note`, `slogan`, `motivation` etc. environments anywhere — grep and remove.

## Acceptance criteria

- Zero instances of the genuinely AI-sounding banned phrases.
- No leftover `\begin{upshot}` etc.
- Transitions read smoothly on a full-paper re-read.

## Risks

- **Fatigue.** This task is mechanical. Don't skimp on it — prose pass is where the paper's AI-ness is hidden or exposed.
