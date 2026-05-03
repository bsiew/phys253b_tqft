# Stage II — Part I Mathematical Buildup A

**Duration:** 2 days (target: Day 1 afternoon through Day 3).
**Lead:** Brian.
**Parallel work for Helena:** first-pass drafts of Chapters 9 and 11 so Stage IV is revision rather than blank-page work.

## Objective

Write Chapters 2, 3, and 4: the differential-geometry primer, the Atiyah–Segal axiomatic framework, and the 2D TQFT / Frobenius-algebra showpiece.

## Tasks

### Chapter 2 — Differential Geometry Primer (~10 pp)

| # | Task | File |
|---|---|---|
| 2.1 | Draft §2.1 (forms, wedge, exterior derivative) | [02_1_forms_basics.md](../tasks/02_1_forms_basics.md) |
| 2.2 | Draft §2.2 (integration, Stokes, de Rham) | [02_2_integration_stokes.md](../tasks/02_2_integration_stokes.md) |
| 2.3 | Draft §2.3 (Lie-algebra-valued forms and conventions) | [02_3_lie_algebra_forms.md](../tasks/02_3_lie_algebra_forms.md) |
| 2.4 | Draft §2.4 (principal bundles at minimum level) | [02_4_principal_bundles.md](../tasks/02_4_principal_bundles.md) |
| 2.5 | Draft §2.5 (gauge transformations and $F^g = g^{-1}Fg$) | [02_5_gauge_transformations.md](../tasks/02_5_gauge_transformations.md) |
| 2.6 | Two worked examples (EM, $S^1 \to S^1$ winding) | [02_6_worked_examples.md](../tasks/02_6_worked_examples.md) |
| 2.7 | Scope-check to ~10 pp | [02_7_scope_check.md](../tasks/02_7_scope_check.md) |

### Chapter 3 — Axiomatic TQFT (~10 pp)

| # | Task | File |
|---|---|---|
| 3.1 | Draft §3.1 (cobordism category) | [03_1_cobordism_category.md](../tasks/03_1_cobordism_category.md) |
| 3.2 | Draft §3.2 (Atiyah–Segal axioms) | [03_2_atiyah_segal_axioms.md](../tasks/03_2_atiyah_segal_axioms.md) |
| 3.3 | Draft §3.3 (one worked gluing: two disks → sphere) | [03_3_gluing_example.md](../tasks/03_3_gluing_example.md) |
| 3.4 | Draft §3.4 (Schwarz vs Witten vs invertible, one paragraph each) | [03_4_taxonomy.md](../tasks/03_4_taxonomy.md) |
| 3.5 | Cross-check every claim has a source or is derived | [03_5_citation_audit.md](../tasks/03_5_citation_audit.md) |

### Chapter 4 — 2D TQFT and Frobenius Algebras — showpiece (~12 pp)

| # | Task | File |
|---|---|---|
| 4.1 | Draft §4.1 (generators and relations of $\mathrm{Cob}_2$, Figure 1: pair of pants) | [04_1_cob2_generators.md](../tasks/04_1_cob2_generators.md) |
| 4.2 | Draft §4.2 (the classification theorem with full argument) | [04_2_classification_theorem.md](../tasks/04_2_classification_theorem.md) |
| 4.3 | Draft §4.3 (worked examples: group algebras, foreshadowing DW) | [04_3_worked_examples.md](../tasks/04_3_worked_examples.md) |
| 4.4 | Derive $Z(\Sigma_g) = \sum_i \lambda_i^{2-2g}$ in full | [04_4_genus_g_partition.md](../tasks/04_4_genus_g_partition.md) |
| 4.5 | Confirm Appendix B carries the technical details | [04_5_appendix_B_handoff.md](../tasks/04_5_appendix_B_handoff.md) |

## Acceptance criteria

- All three chapters compile as part of `paper/main.tex` without errors.
- Chapter 4's proof of the Frobenius-algebra correspondence is complete at review level (technical details pushed to Appendix B).
- Chapter 2 reuses Lemma content from `paper/chern_simons_theory.tex` by cross-reference, not by duplication.
- Every claim in Chapter 3 is either a definition, a worked example, or cited to Atiyah 1988.
- Page count: Chapter 2 ~10 pp, Chapter 3 ~10 pp, Chapter 4 ~12 pp.

## Dependencies

- Blocks: Stage III (Chapter 6 BF theory needs the gauge-transformation machinery of §2.5).
- Depends on: Stage I (skeleton and preamble).

## Risks

- **Chapter 4 bloat.** The Frobenius classification is beautiful and can attract expansion. Mitigation: strict 12-page cap, push to Appendix B when in doubt.
- **Chapter 2 over-general.** It's tempting to write a mini-textbook on forms. Stick to what Chapters 3–8 actually use. Anything else is cut.
- **Duplication with CS chapter.** Chapter 2 and the CS chapter both introduce forms. Resolve by: Chapter 2 is the formal introduction, the CS chapter says "we use the conventions of Chapter 2".
