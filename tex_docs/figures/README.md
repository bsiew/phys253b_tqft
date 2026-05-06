# paper/figures/

This directory holds every figure used by `paper/main.tex`.

Register frozen 2026-05-03 (Task 1.8). Policy is set by [Task 1.11](../../plan/tasks/01_11_figure_policy.md) and the global editorial rules in [plan/README.md](../../plan/README.md).

## Policy (non-negotiable)

1. **No LLM-generated TikZ for complex topology.** Knots, braid traces, fusion trees, cobordism generators, and anyon worldlines are **hand-drawn and scanned**. TikZ is allowed for simple block schematics (lattice diagrams, interferometer comparison, subtraction geometries with no knotting) because those are low topological content.
2. **Redraw schematics with citation** rather than reproducing journal figures directly. Caption pattern: "Schematic based on [citation]."
3. **Only reproduce a figure directly** if the license is open or the author-reproduction right is explicit. Caption pattern: "Reproduced from [citation], Fig. N, under [license]."
4. **File format:** commit `.pdf` for scans and `.tex` for TikZ source. Scans at 300 dpi or higher; crop to content before scanning.
5. **No raster files (`.png`, `.jpg`, `.svg`) in the repo.** Convert to PDF via ImageMagick or print-to-PDF before committing.

## Figure register (frozen)

Status legend: ❌ TODO, ⏳ in progress, ✅ committed.

| # | Filename | Chapter/§ | Type | Status | Owner | Drafting task | Notes |
|---|---|---|---|---|---|---|---|
| 1 | `cobordism_generators.pdf` | Ch 3 §3.3, Ch 4 §4.1 | hand-drawn scan | ❌ | B | [4.1](../../plan/tasks/04_1_cob2_generators.md) | cap, cup, cylinder, pair of pants side by side |
| 2 | `pair_of_pants.pdf` | Ch 4 §4.2 | hand-drawn scan | ❌ | B | [4.1](../../plan/tasks/04_1_cob2_generators.md) | multiplication ⊗ comultiplication diagram |
| 3 | `hopf_link.pdf` | Ch 5 §Witten–Jones | hand-drawn scan | ❌ | B | [5.1](../../plan/tasks/05_1_witten_jones_bridge.md) | two linked circles with crossing info |
| 4 | `defect_insertion.pdf` | Ch 8 §8.2 | hand-drawn scan | ❌ | B | [8.2](../../plan/tasks/08_2_q_form_dictionary.md) | codimension-$(q+1)$ defect on a spacetime slice |
| 5 | `anomaly_inflow.pdf` | Ch 8 §8.5, §8.6 | hand-drawn scan | ❌ | B | [8.5, 8.6](../../plan/tasks/08_6_hep_inflow_example.md) | bulk-boundary cylinder schematic |
| 6 | `toric_code_lattice.pdf` | Ch 9 §9.2 | TikZ block schematic | ❌ | H | 9.2 | square lattice with $A_v$, $B_p$ stabilizers and a $W_1$ string operator |
| 7 | `anyon_braiding.pdf` | Ch 10 §10.2 | hand-drawn scan | ❌ | H | 10.2 | two worldlines exchanging in 2+1D |
| 8 | `interferometer_comparison.pdf` | Ch 12 (all three experiments) | TikZ block schematic | ❌ | H | [12.4](../../plan/tasks/12_4_experiment_figures.md) | single composite comparing Nakamura 2020, Werkmeister 2025, Andersen 2023 geometries |
| 9 | `ising_fusion_tree.pdf` | Ch 10 §10.5, Ch 13 §13.2 | hand-drawn scan | ❌ | H | 10.5, 13.2 | $\sigma \times \sigma = 1 + \psi$ fusion tree |
| 10 | `kitaev_preskill_geometry.pdf` | App E | hand-drawn scan | ❌ | B | [E.1](../../plan/tasks/AE_1_tee_derivation.md) | four-region disk partition for $\gamma = \log \mathcal{D}$ |

Total: **10 figures**. 7 hand-drawn topological, 3 TikZ block schematics. Upper-bound page cost: ~1.5 pp of figure real estate spread across the paper.

## Deliberate cuts (do not re-add without a scope conversation)

- **Hall-bar geometry for Ch 11.** Ch 11 derives $\sigma_{xy} = e^2/(mh)$ symbolically from the CS Lagrangian; a Hall-bar schematic would be cosmetic. Cut.
- **Separate figures per experiment** (Nakamura, Werkmeister, Andersen). Merged into the single composite figure #8 which compares the three geometries side-by-side. This makes the editorial judgment about synthetic vs.\ natural platforms visible.
- **BF-theory phase diagram.** Not needed — the BF → $\mathbb{Z}_N$ reduction in Ch 6 §6.2 is algebraic.
- **Landau-level energy diagram** for Ch 11. Helena to decide during drafting; default is to skip.
- **MCG action diagrams** for App B. Text and equation suffice for the Morse-decomposition direction.

## How to include a figure

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.6\linewidth]{figures/cobordism_generators}
    \caption{Generators of $\mathrm{Cob}_2$: cap, cup, cylinder, pair of pants. Each 2-manifold-with-boundary acts on the single-circle state space $V = Z(S^1)$ in a way that assembles into the data of a commutative Frobenius algebra.}
    \label{fig:cobordism-generators}
\end{figure}
```

For TikZ, keep the source in this directory as `<name>.tex` and either `\input{figures/<name>}` inside a `figure` environment or compile to PDF separately and `\includegraphics` the result.

## Attribution checklist

For every figure tagged "schematic based on [citation]" or "reproduced from [citation]" in its caption:

1. Caption must include the primary citation, whose bib entry has a DOI.
2. If reproducing directly (not redrawing), capture the license or reproduction-rights basis alongside the figure file.
3. The bib entry for the source must already exist in `paper/tqft_review.bib`.

All three experimental references used in figure #8 (`Nakamura2020`, `Werkmeister2025`, `Andersen2023`) are in the bib (Task 1.5).

## No figure stubs are committed

An absent file is a clear TODO signal. Once a figure PDF lands, flip status from ❌ to ✅ in the register and commit both the PDF and the README change in the same commit.

---

## Tables

Register frozen 2026-05-03 (Task 1.9). Tables live inline inside the chapter files as `\begin{table} \begin{tabular}{...} \end{tabular} \end{table}` — there is no separate `tables/` directory. The register below exists so we don't add or drop tables mid-stream.

Status legend: ❌ TODO, ⏳ in progress, ✅ committed.

| # | Table | Chapter/§ | Status | Owner | Drafting task | Notes |
|---|---|---|---|---|---|---|
| T1 | Generalized-symmetry dictionary | Ch 8 §8.2 | ❌ | B | [8.2](../../plan/tasks/08_2_q_form_dictionary.md) | Columns: object, dimension, charged operator, symmetry defect, conserved current / background field. Rows: ordinary 0-form $G$, 1-form $U(1)_e$, 1-form $U(1)_m$, $\mathbb{Z}_N$ center. Mandatory per Task 8.2 acceptance criteria. |
| T2 | Anyon comparison | Ch 10 §10.5 | ❌ | B+H | [10.5](../../plan/tasks/10_5_anyon_comparison_table.md) | Columns: labels, fusion rules, braiding phase (self), topological spin. Rows: toric code $\mathbb{Z}_2$, Laughlin $\nu = 1/m$, Ising. Mandatory per Task 10.5 acceptance criteria. |

Total: **2 tables**.

### Deliberate cuts (do not re-add without a scope conversation)

- **Page budget / part breakdown table** (was Table 3 in the Task 1.9 spec). The introduction is explicitly instructed to "say which part covers what" in prose rather than via a breakdown table; `TQFT_outline_v3.tex` already carries the detailed breakdown for the authors' own use.
- **Bibliography summary table.** `\bibliography` already does this.
- **"What we cover vs. cut" table.** The abstract and outlook carry this editorial signal in prose.

### How to include a table

Follow Brian's style (see `references/style references/hdr.tex`):

```latex
\begin{table}[h]
    \centering
    \begin{tabular}{@{}lllll@{}}
        \toprule
        Object & Dimension & Charged operator & Symmetry defect & Background field \\
        \midrule
        $G$ (0-form) & 0 & local operator $\mathcal{O}(x)$ & codim-1 $U_g(\Sigma^{d-1})$ & $A \in \Omega^1(M, \mathfrak{g})$ \\
        % ...
        \bottomrule
    \end{tabular}
    \caption{Dictionary for $q$-form symmetries.}
    \label{tab:gen-sym-dictionary}
\end{table}
```

Use `booktabs` rules (`\toprule`, `\midrule`, `\bottomrule`) — not `\hline`. `booktabs` is already loaded by `paper/preamble.tex`.

