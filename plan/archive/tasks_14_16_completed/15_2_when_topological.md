---
created_at: "2026-05-05T17:31:56-04:00"
updated_at: "2026-05-05T17:48:41-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 15.2 — Chapter 15 §15.2 When the Observables Are Really Topological, and When They Are Only Effective

- **Status:** pending
- **Owner:** Helena
- **Duration:** 2.5 hr
- **Stage:** new (no BSIEW counterpart)

## Goal

Unify the per-chapter "iffiness" discussions (Ch 11 §11.7, Ch 14 §14.4, §15.1) into a four-category organizing table. This is the structural climax of the paper's critical-assessment theme.

## Content

The four-category taxonomy (from tqft_observables_literature_review.md Sec. 9):

| Category | Definition | Example chapters |
|----------|-----------|-----------------|
| (a) Strict TQFT | Metric-independent in the exact theory; computed from the partition function of a TQFT. | Part I Sec. 4 (Wilson-line linking, Hilbert spaces on closed surfaces) |
| (b) IR topological response | Universal below the gap and after decoupling assumptions; computed from a CS effective action. | Ch 11 §11.2–11.4 (Hall conductance, edge anomaly coefficient, GSD) |
| (c) Theory-side topological | Defined cleanly in Euclidean QFT / lattice; enter observables only indirectly through hadronization or analytic continuation. | Ch 14 §14.1–14.2 (instanton number, $\chi_t$, $\eta'$ mass) |
| (d) Topology-inspired but model-dependent | The underlying topological sector is real, but the observable coupling to it depends on the UV completion or mesoscopic details. | Ch 14 §14.3 (axion couplings), Ch 15 §15.1 (monopole production rates), Ch 11 §11.7 (interferometric signatures) |

### Structure

1. **State the table.** Present as a 4-row table with definition + examples.
2. **Sharpen each category.** One paragraph per category: what makes it "clean" or "iffy," and what would upgrade or downgrade a given observable.
3. **Cross-references.** Each example points back to the relevant section with `\ref`.
4. **Closing paragraph.** TQFT reorganizes gauge theory around global data; the four-category table is the honest answer to "how topological is this observable?"

## Acceptance criteria

- Four-category table present and filled.
- Each category has one paragraph of prose.
- All examples cross-reference earlier sections with `\ref`.
- Closing paragraph connects to Ch 16 (outlook) and the through-line.
- ~4–6 pages.

## References

- Witten 2016 (Three Lectures on Topological Phases)
- Stern 2008 (Anyons and QHE review)
- Wen 1995 (Topological orders)
- Birmingham et al. 1991 (Topological field theory review)

## Literature summaries (relative to `PROJECTS/QFT/`)

- `literature/1510.07698/codex_paper_summary.md` — Witten 2016 Three Lectures on Topological Phases
- `literature/0711.4697/codex_paper_summary.md` — Stern 2008 Anyons and QHE pedagogical review
- `literature/cond-mat_9506066/codex_paper_summary.md` — Wen 1995 Topological orders and edge excitations

## Dependencies

- Ch 11 §11.7 (2+1d caveats — must be written first so the taxonomy can cite it).
- Ch 14 §14.4 (3+1d caveats).
- §15.1 (monopoles — category (d) example).
