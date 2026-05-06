---
created_at: "2026-05-05T19:01:40-04:00"
updated_at: "2026-05-05T22:03:47-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.11 — Prose Pass and AI-Tell Purge

- **Status:** pending
- **Owner:** Brian + Helena
- **Duration:** 2.5 hours (expanded scope)
- **Stage:** [VI](../stages/stage_VI_integration.md)
- **Reference:** [`llm_docs/CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md`](../../llm_docs/CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md) — see "Cross-Cutting Problems §3: Missing Through-Line"

## Goal

Strip AI-sounding phrases from the whole paper. Get transitions and sentence rhythms in Brian's style (see `references/style references/hdr.tex`, `springer.tex`). Upgrade generic chapter-glue sentences to specific Part-2-payoff pointers (per Critical Evaluation §3).

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

## Through-line upgrade (from Critical Evaluation)

Task 17.6 provides generic chapter-ending glue sentences. During this pass, upgrade each to a **specific** Part-2-payoff pointer. Examples of the required specificity:

| Current (generic) | Target (specific) |
|---|---|
| "We now turn to the physical realization..." | "The linking-number computation of §5.6 predicts the $2\pi/3$ braiding phase measured in the Nakamura experiment of Chapter 12." |
| "Part II turns to..." | "The anomaly inflow mechanism of §8.7 will reappear as the origin of chiral edge modes in the FQHE (Chapter 11, Eq. 11.X)." |

Every Part 1 chapter ending must name a specific equation, observable, or experiment from Part 2.

## Acceptance criteria

- Zero instances of the genuinely AI-sounding banned phrases.
- No leftover `\begin{upshot}` etc.
- Transitions read smoothly on a full-paper re-read.
- Every Part 1 chapter-ending glue sentence names a specific Part 2 payoff (equation, experiment, or observable).

## Dependencies

- Run AFTER Task 17.12 (LLM decontamination pass — kills structural AI tells and contrived framing).
- Run AFTER Task 17.13 (full style overhaul — rewrites section openings, transitions, and rhythm against Tong/GGS references).
- This task is then the final mechanical cleanup: banned-phrase grep, glue-sentence upgrade, environment removal.

## Risks

- **Fatigue.** This task is mechanical. Don't skimp on it — prose pass is where the paper's AI-ness is hidden or exposed.
