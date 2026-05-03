# Task 1.1 — Produce Outline v3

- **Status:** pending
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)

## Goal

Produce `TQFT_outline_v3.tex` that merges the page budget and through-line of outline v2 with the chapter list and author split agreed in `plan/plan_of_attack.tex` Section 2.

## Inputs

- `TQFT_outline_v2.tex`
- `plan/plan_of_attack.tex` Section 2 (paper structure)
- `plan/plan_of_attack.tex` Section 1.4 (author split)

## Steps

1. Copy `TQFT_outline_v2.tex` to `TQFT_outline_v3.tex`.
2. Replace the 22-section outline with the 14-chapter + appendix structure from `plan_of_attack.tex` Section 2.
3. For each chapter, mark: owner (B/H/B+H), depth tag (Deep/Bridge/Survey), page budget.
4. Add a "Decisions already made" box at the top listing the cuts (no non-invertible symmetry section, SymTFT to one page, no Jones-polynomial derivation, no R-T details).
5. Compile to PDF, verify one page of front matter + roughly three pages of detailed outline.

## Acceptance criteria

- `TQFT_outline_v3.tex` compiles.
- Every chapter has an owner, a tag, and a page budget.
- The "Decisions already made" box is present and matches the decisions in `plan_of_attack.tex`.
- Total page budget sums to 75–100 main + 15–25 appendix.

## Risks

- **Scope creep during editing.** The act of rewriting the outline invites adding "one more section". Resist; this task is reformat + re-scope, not redesign.
