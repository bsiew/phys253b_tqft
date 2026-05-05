# Task 1.1 — Produce Outline v3

- **Status:** done (2026-05-03)
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)
- **Priority:** core

## Result

`TQFT_outline_v3.tex` committed at the project root. Main-text target 113–117 pp,
appendices 21 pp (compressible to 16 pp), grand total 134–138 pp.

Key differences from v2:
- 14-chapter + 5-appendix structure replacing the old Part-based numbering
- Chapter 5 (CS) marked as the anchor chapter, not one of three equally-weighted deep dives
- Witten–Jones bridge restored as Chapter 5 subsection (Task 5.1)
- Chapter 8 CM inflow example changed from 3D TI $\theta=\pi$ to FQH edge
- Werkmeister 2025 replaces Werkmeister 2024 as the primary graphene interferometer citation
- Appendices A/C/D/E each have dedicated task files
- Explicit trim ladder attached

File-path references removed that pointed at phantom sections; all surviving
references resolve to the current plan tree or to `paper/chern_simons_theory.tex`.

## Goal

Produce `TQFT_outline_v3.tex` that uses `TQFT_outline_v2.tex` as raw input but updates the chapter list, page budget, and author split to match the current `plan/plan_of_attack.tex`.

## Inputs

- `TQFT_outline_v2.tex`
- `plan/plan_of_attack.tex` Section 2 (paper structure)
- `plan/plan_of_attack.tex` Section 1.4 (author split)

## Steps

1. Copy `TQFT_outline_v2.tex` to `TQFT_outline_v3.tex`.
2. Replace the older section structure with the current 14-chapter + appendix structure from `plan_of_attack.tex` Section 2.
3. For each chapter, mark: owner (B/H/B+H), depth tag (Deep/Bridge/Survey), page budget.
4. Add a "Decisions already made" box at the top listing the cuts (no non-invertible symmetry section, SymTFT compressed, no standalone Jones-polynomial chapter, no R-T details).
5. Compile to PDF, verify one page of front matter + roughly three pages of detailed outline.

## Acceptance criteria

- `TQFT_outline_v3.tex` compiles.
- Every chapter has an owner, a tag, and a page budget.
- The "Decisions already made" box is present and matches the decisions in `plan_of_attack.tex`.
- Total page budget sums to roughly 110-120 main + 10-15 appendix.

## Risks

- **Scope creep during editing.** The act of rewriting the outline invites adding "one more section". Resist; this task is reformat + re-scope, not redesign.
