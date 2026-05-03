# Task 1.7 — `paper/figures/` Directory with README

- **Status:** pending
- **Owner:** Brian
- **Duration:** 10 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)

## Goal

Create the figures directory with a README that catalogues every image the paper will contain, its status, and its author.

## Steps

1. `mkdir paper/figures/`.
2. Create `paper/figures/README.md` with a table listing every planned figure:

```markdown
| # | Figure | Chapter | Type | Status | Owner |
|---|---|---|---|---|---|
| 1 | Cobordism generators (cap, cup, cyl, POP) | 4 | TikZ | TODO | B |
| 2 | Pair-of-pants multiplication diagram | 4 | TikZ | TODO | B |
| 3 | Hopf link for Wilson-loop discussion | 5 | TikZ | TODO | B |
| 4 | Higher-form symmetry defect insertion | 8 | TikZ | TODO | B |
| 5 | Bulk-boundary anomaly inflow schematic | 8 | TikZ | TODO | B |
| 6 | Anyon braiding worldlines | 10 | TikZ | TODO | H |
| 7 | FQH interferometer (Nakamura 2020) | 12 | extract + cite | TODO | H |
| 8 | Ising fusion tree | 13 | TikZ | TODO | H |
```

3. Commit empty `paper/figures/fig01_cobordism.tex` etc. as placeholder stubs so the LaTeX `\includegraphics` or `\input{figures/fig01_cobordism}` references resolve.

## Acceptance criteria

- Directory exists with README.
- Table in README matches the "Figure checklist" from `plan_of_attack.tex` Task 1.8.
- Each planned figure has a stub file.
