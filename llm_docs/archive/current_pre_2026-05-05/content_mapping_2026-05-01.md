---
created_at: "2026-05-01T17:18:41-04:00"
updated_at: "2026-05-02T20:33:45-04:00"
generated_by: "codex_gpt5"
timestamp_source: "agent_clock"
---

# Content Mapping for QFT Paper Reorganization

Purpose: active source-to-destination map for the current 7-section Part I / Part II final-paper structure.

Archived previous map: `PROJECTS/QFT/253b_final_paper/llm_docs/archive/content_mapping_2026-05-01_10-section.md`. That file preserves the old 10-section plan and should be treated as provenance, not as active routing guidance.

## Current Structure

Part I builds the mathematical and field-theoretic bridge:

1. `part1_01_introduction.tex`
2. `part1_02_mathematical_toolkit.tex`
3. `part1_03_ordinary_to_chern_simons.tex`
4. `part1_04_tqft_and_observables.tex`

Part II organizes the physics by observable family:

5. `part2_05_response_2plus1d.tex`
6. `part2_06_sectors_3plus1d.tex`
7. `part2_07_defects_caveats_outlook.tex`

## Legend

- **Migrate:** move or adapt existing source prose/calculations into active TeX.
- **Extract:** condense only the useful pieces from a broader source.
- **Write:** produce new connective prose from the source map and citations.
- **Already partial:** active TeX exists and needs completion or audit.
- **Archive only:** keep for provenance, but do not use as an active source unless a missing detail is needed.

## 1. Introduction

Destination: `part1_01_introduction.tex`

Status: write last, after Sections 2-7 stabilize.

Primary inputs:

- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/tqft_observables_literature_review.md`, especially Section 11.
- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/Final QFT Project Overview.md`.
- Finished Sections 2-7, so the introduction promises only what the paper actually delivers.

Content target:

- Frame the paper around topological structures in ordinary QFT, Chern-Simons theory as a bridge, TQFT as the natural formal language, and observables as the physical payoff.
- Preview the Part II observable families: transport/response, CP-sensitive and spectroscopic effects, braiding/nonlocal probes, and defect/global-structure probes.
- Avoid importing old 10-section introduction scaffolding except for useful phrasing.

## 2. Mathematical Toolkit

Destination: `part1_02_mathematical_toolkit.tex`

Status: extract and centralize.

Primary sources:

- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/topology_review.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/differential_forms_csimons_foundations_v2.tex`
- `PROJECTS/QFT/writings/brian_chern_simons_theory.tex`

Source routing:

| Source material | Destination | Action |
|---|---|---|
| Differential forms, orientation, exterior derivative, Stokes' theorem | 2.1 Forms and Conventions | Extract the cleanest definitions from `differential_forms_csimons_foundations_v2.tex`. |
| Lie groups, Lie algebras, SU(2), SO(3), maximal tori | 2.2 Lie Groups and Gauge Groups | Extract from `topology_review.tex`; keep only what later sections use. |
| Principal bundles, connections, curvature | 2.3 Bundles and Connections | Extract from `topology_review.tex`, `differential_forms_csimons_foundations_v2.tex`, and Brian's review. |
| Gauge transformations and characteristic classes | 2.4 Gauge Transformations and Classes | Define here; defer Chern-Simons descent and level quantization to Section 3. |
| Homotopy, winding, `\pi_3(G)` | 2.5 Homotopy and Winding | Extract from `topology_review.tex`; connect directly to large gauge transformations. |
| Holonomy, Wilson loops, flat connections, linking | 2.6 Holonomy and Flat Data | Extract concise definitions; full observable payoff belongs in Section 4. |
| Moduli spaces, symplectic forms, reduction | 2.7 Moduli and Symplectic Structure | Use Brian's clearer exposition plus `topology_review.tex`. |
| Bordism and Atiyah-Segal language | 2.8 TQFT Input Data | State definitions briefly; develop the TQFT interpretation in Section 4. |

Cut or avoid:

- The old just-in-time math distribution plan. The current preference is a centralized mathematical toolkit.
- Pedagogical meta commentary that does not support later calculations.
- Standalone topology-review framing; it should now serve Section 2 and selected later cross-references.

## 3. From Ordinary Gauge Theory to Chern-Simons

Destination: `part1_03_ordinary_to_chern_simons.tex`

Status: reorganize archived derivations into a single bridge section.

Primary sources:

- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/differential_forms_csimons_foundations_v2.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/chern_simons_two_review_synthesis.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/dense_derivation_expansion.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/anomalies_boundaries_topological_response.tex`
- `PROJECTS/QFT/writings/brian_chern_simons_theory.tex`

Source routing:

| Topic | Destination | Action |
|---|---|---|
| Yang-Mills vacua, pure-gauge sectors, large gauge transformations | 3.1 | Migrate from `topology_review.tex`, `dense_derivation_expansion.tex`, and `chern_simons_two_review_synthesis.tex`. |
| Instantons and theta terms | 3.2 | Write from class notes/literature; use archived derivations only for normalization checks. |
| Anomaly descent and transgression | 3.3 | Extract from `differential_forms_csimons_foundations_v2.tex` and Brian's review. |
| Chern-Simons action and equations of motion | 3.4 | Migrate from v2 foundations and Brian's review. |
| Level quantization under large gauge transformations | 3.5 | Extract the SU(2) winding calculation from `dense_derivation_expansion.tex`; support with `\pi_3(G)` material from Section 2. |
| Why Chern-Simons theory differs from ordinary Yang-Mills theory | 3.6 | Write synthesis: metric independence, no local propagating degrees of freedom in pure CS, boundary sensitivity, and moduli-space dynamics. |

Archive-only source:

- `differential_forms_csimons_foundations.tex` is superseded by the v2 file. Use it only if a missing detail is not present in v2.

## 4. TQFT and Its Observables

Destination: `part1_04_tqft_and_observables.tex`

Status: merge existing CS-observable material with new TQFT framing.

Primary sources:

- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/topology_review.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/chern_simons_two_review_synthesis.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/dense_derivation_expansion.tex`
- `PROJECTS/QFT/writings/brian_chern_simons_theory.tex`
- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/tqft_observables_literature_review.md`, especially Section 2.

Source routing:

| Topic | Destination | Action |
|---|---|---|
| Functorial definition of TQFT | 4.1 | Write from Atiyah-Segal summary material and `topology_review.tex`. |
| Classes of TQFTs | 4.2 | Write a compact taxonomy using Witten/Blau/Birmingham-style references. |
| Chern-Simons as central example | 4.3 | Migrate from `chern_simons_two_review_synthesis.tex` and Brian's review. |
| Wilson loops, linking, and framing | 4.4 | Extract from `dense_derivation_expansion.tex` and `chern_simons_two_review_synthesis.tex`. |
| Hilbert spaces and ground-state degeneracy | 4.5 | Use torus quantization material from `dense_derivation_expansion.tex`, Brian's review, and QHE references. |
| Observable taxonomy | 4.6 | Write from `tqft_observables_literature_review.md` Section 2; make this the transition into Part II. |

## 5. Topological Response in 2+1 Dimensions

Destination: `part2_05_response_2plus1d.tex`

Status: already partial; finish the remaining subsections and audit conventions.

Primary sources:

- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-02_pre_simplification/08_physical_applications.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/chern_simons_theory_FQHE_throughline_v2.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/anomalies_boundaries_topological_response.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/dense_derivation_expansion.tex`
- `PROJECTS/QFT/writings/chern_simons_review.tex`
- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/tqft_observables_literature_review.md`, especially Section 4.

Source routing:

| Topic | Destination | Action |
|---|---|---|
| QHE/FQHE problem setup | 5.1 | Already partial; audit for scope and citations. |
| Hall response | 5.2 | Already drafted; check units, signs, and normalization. |
| Fractional charge and braiding | 5.3 | Already drafted; audit anyon phase conventions. |
| Edge modes, ground-state degeneracy, K-matrix, nonabelian roadmap | 5.4 | Already partial; strengthen links back to Section 4. |
| Maxwell-Chern-Simons contrast | 5.5 | Write from `anomalies_boundaries_topological_response.tex` and `dense_derivation_expansion.tex`. |
| QHE caveats | 5.6 | Write from literature-review caveats and experimental caveat notes. |

## 6. Topological Sectors in 3+1 Dimensions

Destination: `part2_06_sectors_3plus1d.tex`

Status: new writing.

Primary sources:

- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/tqft_observables_literature_review.md`, especially Section 5.
- Section 3 source material for theta terms, instantons, and topological charge.
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/dense_derivation_expansion.tex`, only for component or normalization checks.

Source routing:

| Topic | Destination | Action |
|---|---|---|
| Theta vacua, topological susceptibility, and U(1)A | 6.1 | Write from literature review plus QCD/topological-susceptibility references. |
| Eta-prime mass and Witten-Veneziano logic | 6.2 | Write from Witten/Veneziano/Di Vecchia/lattice references. |
| Strong CP, neutron EDM, and axions | 6.3 | Write from Dine/Hook/Marsh/Abel-style references; resolve experimental placeholders before final citation pass. |
| Caveats and limits of the analogy with 2+1D response | 6.4 | Use literature-review caveats and cross-reference Sections 3 and 5. |

## 7. Defects, Caveats, and Outlook

Destination: `part2_07_defects_caveats_outlook.tex`

Status: new writing with selected extraction.

Primary sources:

- `PROJECTS/QFT/253b_final_paper/llm_docs/reference/tqft_observables_literature_review.md`, especially Sections 6-9.
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/topology_review.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/archive_2026-05-01/anomalies_boundaries_topological_response.tex`
- Section 3 material for monopole and global-structure motivation.

Source routing:

| Topic | Destination | Action |
|---|---|---|
| Monopoles, line operators, and global form of the gauge group | 7.1 | Write from literature-review Sections 6-7 plus homotopy/bundle material in `topology_review.tex`. |
| Strict topology versus effective topological behavior | 7.2 | Write from literature-review Section 9 and anomaly/response caveats. |
| Guide du routard and outlook | 7.3 | Fold the old standalone outlook idea into the final section; use completed paper claims to avoid overpromising. |

## Superseded 10-Section Routing

The old active map used destinations I-X. Those destinations are no longer live, but the mapping below is useful when reading older notes:

| Old destination | New destination |
|---|---|
| I. Introduction | 1. Introduction |
| II. Physical motivation and ordinary QFT | 3. From Ordinary Gauge Theory to Chern-Simons, with basic definitions moved to 2 |
| III. Mathematical toolkit | 2. Mathematical Toolkit |
| IV. From Yang-Mills to Chern-Simons | 3. From Ordinary Gauge Theory to Chern-Simons |
| V. Chern-Simons theory | 3 and 4 |
| VI. Wilson loops and observables | 4. TQFT and Its Observables |
| VII. TQFT formalism | 2.8 and 4 |
| VIII. Physical applications | 5. Topological Response in 2+1 Dimensions |
| IX. Subtleties and caveats | 5.6 and 7.2 |
| X. Conclusion and outlook | 1 and 7.3 |

## Duplicate and Cut Decisions

- `differential_forms_csimons_foundations.tex`: archive only; prefer `differential_forms_csimons_foundations_v2.tex`.
- `topology_review.tex`: no longer a standalone active section; extract into Section 2 and selected cross-references.
- `dense_derivation_expansion.tex`: source reference for calculations, not a standalone active section.
- Old 10-section stubs and plans: archive/provenance only unless a precise paragraph is still useful.
- Figure wishlist material: use the combined active figure inventory instead of separate wishlist routing.
- Project/session logs: do not treat as evidence sources for the paper body.

## Migration Priorities

1. Finish Section 5.5 and 5.6 while the partial 2+1D response draft is already open.
2. Migrate the centralized mathematical toolkit into Section 2.
3. Migrate the ordinary-QFT-to-CS bridge into Section 3.
4. Draft the TQFT and observable-taxonomy bridge in Section 4.
5. Draft the 3+1D topological-sectors material in Section 6.
6. Draft defects, caveats, and outlook in Section 7.
7. Resolve bibliography placeholders and normalization audits.
8. Write Section 1 last.
