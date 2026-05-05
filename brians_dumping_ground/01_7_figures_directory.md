# Task 1.7 — `paper/figures/` Directory with README

- **Status:** done (2026-05-03)
- **Owner:** Brian
- **Duration:** 10 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)
- **Priority:** core

## Result

`paper/figures/README.md` committed as the figure register for the paper. Thirteen figures planned: seven hand-drawn topological (cobordism, pair of pants, Hopf link, defect insertion, inflow schematic, anyon braiding, fusion tree, Kitaev–Preskill geometry) and six TikZ block schematics (Hall bar, toric-code lattice, three experiment schematics). Each row has status (❌/⏳/✅), owner (B/H), drafting-task link, and a short description.

## Deviation from original spec

Original spec said: "commit empty `paper/figures/fig01_cobordism.tex` etc. as placeholder stubs so `\includegraphics` references resolve." We did not commit those stubs. Two reasons:

1. **Policy.** [Task 1.11](01_11_figure_policy.md) requires hand-drawn scans for the topological figures, i.e. PDFs not TeX. An empty `.pdf` stub is meaningless.
2. **Signal clarity.** A missing file is a clearer TODO signal than an empty stub, and it matches the "status = ❌" column in the register. When the figure lands, update the README from ❌ to ✅ in the same commit.

Chapters that forward-reference an unwritten figure will get a missing-file warning at compile time, which is the intended prompt to go draw it.

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
