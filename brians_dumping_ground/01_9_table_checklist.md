# Task 1.9 — Table Checklist

- **Status:** done (2026-05-03)
- **Owner:** Brian
- **Duration:** 10 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)
- **Priority:** core

## Result

Table register committed to `paper/figures/README.md` under a new "Tables" heading. **2 tables total**:

| # | Table | Chapter | Owner |
|---|---|---|---|
| T1 | Generalized-symmetry dictionary | Ch 8 §8.2 | B |
| T2 | Anyon comparison (toric code / Laughlin / Ising) | Ch 10 §10.5 | B+H |

### Change from the earlier spec

The earlier spec listed 3 tables. I dropped **Table 3 (Page budget by part)** because:

- The Chapter 1 introduction task (Task 14.2) explicitly says "Do not summarize every chapter; just say which part covers what," which conflicts with a chapter-by-chapter budget table.
- `TQFT_outline_v3.tex` already carries the budget breakdown for the authors' own planning, and that's not the paper's audience.
- Keeping the intro in prose is cleaner editorial judgment.

### Deliberate cuts (recorded in the register to prevent re-addition)

- Bibliography summary table.
- "What we cover vs. cut" editorial table.
- Page-budget-by-part table.

## Goal

Enumerate the tables the paper will contain.

## The list

1. **Generalized-symmetry dictionary** (Ch 8 §8.2). Columns: object, dimension, charged operator, symmetry defect, conserved current/background field. Rows: ordinary 0-form $G$, 1-form $U(1)_{\text{electric}}$, 1-form $U(1)_{\text{magnetic}}$, $\mathbb{Z}_N$ 1-form center.
2. **Anyon comparison** (Ch 10 §10.5). Columns: labels, fusion rules, braiding phases, topological spin. Rows: toric code ($\{1, e, m, \epsilon\}$), Laughlin $\nu = 1/3$, Ising ($\{1, \sigma, \psi\}$).
3. **Page budget by part** (Ch 1 intro). Columns: Part, topic, target pages. Rows: Part I, Part II, appendices.

## Cuts

- No bibliography summary table. The `\bibliography` section suffices.
- No "what we cover vs. cut" table. That's what the abstract and outlook do.

## Acceptance criteria

- This list is committed to `paper/figures/README.md` under a "Tables" heading.

## Risks

- Low. Tables are cheap to produce in LaTeX.
