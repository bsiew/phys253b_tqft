---
created_at: "2026-05-05T17:33:26-04:00"
updated_at: "2026-05-05T18:32:08-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Stage IV-b — Part II Cross-Disciplinary Additions (Ch 14–15)

**Duration:** 2 days (flexible — independent of Ch 9–13 progress).
**Lead:** Helena.

## Objective

Write Chapters 14 and 15: QCD topology / axion physics, and the defects / four-category synthesis. These chapters have NO BSIEW precursor. They extend the paper's scope beyond the condensed-matter core to show the same topological structures governing 3+1d gauge theory.

## Relationship to BSIEW stages

The BSIEW plan originally used "14" and "15" for integration and presentation tasks (Stages VI and VII). Those have been renumbered to **17_*** and **18_*** respectively. The **14_*** and **15_*** task numbers now belong to chapter writing:

- Task 14.x = Chapter 14 section writing (theta, WV, axion, caveats)
- Task 15.x = Chapter 15 section writing (monopoles, taxonomy)
- Task 17.x = Stage VI integration (abstract, cross-refs, bib, etc.)
- Task 18.x = Stage VII presentation (board scripts, rehearsal)

## Tasks

### Chapter 14 — Topological Sectors in 3+1 Dimensions (~15–20 pp, Helena)

| # | Task | File |
|---|---|---|
| 14.1 | Draft §14.1 (theta vacua, $\chi_t$, U(1)_A) | [14_1_theta_chi_u1a.md](../tasks/14_1_theta_chi_u1a.md) |
| 14.2 | Draft §14.2 (eta-prime mass, Witten–Veneziano) | [14_2_eta_prime_wv.md](../tasks/14_2_eta_prime_wv.md) |
| 14.3 | Draft §14.3 (strong CP, nEDM, axion) | [14_3_strong_cp_axion.md](../tasks/14_3_strong_cp_axion.md) |
| 14.4 | Draft §14.4 (caveats / "iffiness" for 3+1d) | [14_4_qcd_caveats.md](../tasks/14_4_qcd_caveats.md) |

### Chapter 15 — Defects, Global Structure, and Synthesis (~10–12 pp, Helena)

| # | Task | File |
|---|---|---|
| 15.1 | Draft §15.1 (monopoles, line operators, global structure) | [15_1_monopoles_line_operators.md](../tasks/15_1_monopoles_line_operators.md) |
| 15.2 | Draft §15.2 (four-category "when topological" taxonomy) | [15_2_when_topological.md](../tasks/15_2_when_topological.md) |

## Acceptance criteria

- Chapter 14 derives $\chi_t$, states Witten–Veneziano, derives the axion mass from $\chi_t$, and cites the nEDM bound numerically.
- Chapter 14 §14.4 and Chapter 15 §15.2 explicitly address when observables are "clean" vs "iffy."
- Chapter 15 §15.2 contains the four-category table with cross-references to all earlier chapters.
- Both chapters compile as part of `tex_docs_main_wrapper_20260501.tex`.
- No instanton derivation from scratch — state results and cite.
- No generalized-symmetries formalism beyond a one-paragraph bridge.

## Dependencies

- **Independent of** Ch 9–13 (Stages IV–V). Can be written in parallel.
- **Depends on** Part I Sec. 2 (homotopy groups) and Sec. 3 (instanton number) for notation.
- **Feeds into** Stage VI integration (cross-refs, through-line, must-include audit).
- Ch 15 §15.2 depends on Ch 11 §11.7 and Ch 14 §14.4 being at least outlined.

## Writing order

1. ch14.1 → ch14.2 → ch14.3 → ch14.4 (linear narrative chain)
2. ch15.1 (independent of Ch 14 content, but benefits from §14.4 being at least outlined)
3. ch15.2 (depends on both §14.4 and §15.1 being drafted)

## Risks

- **Scope creep from QCD.** The instanton, theta-vacuum, and axion literatures are enormous. Each subsection should cite one TASI review and move on.
- **Monopole monograph.** One worked example (SU(2) → U(1)) only.
- **Category (c)/(d) conflation.** The boundary between "theory-side topological" and "model-dependent" is subtle. State it clearly with examples and don't oversimplify.
- **Numbering collision resolved.** BSIEW integration tasks renumbered to `17_*`, presentation tasks to `18_*`. Chapter writing tasks now own the `14_*` / `15_*` / `16_*` namespace.
