---
created_at: "2026-05-05T18:27:51-04:00"
updated_at: "2026-05-05T22:04:18-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Stage VI — Integration and Polish

**Duration:** 1 day (target: Day 7 afternoon through Day 8).
**Lead:** joint.

## Objective

Draft front matter, back matter, and all appendices. Propagate cross-references. Install figures. Proofread three times. Consolidate the bibliography.

## Tasks

### Front and back matter

| # | Task | Owner | File |
|---|---|---|---|
| 17.1 | Draft abstract (<250 words) | B+H | [17_1_abstract.md](../tasks/17_1_abstract.md) |
| 17.2 | Draft Chapter 1 introduction | B+H | [17_2_introduction.md](../tasks/17_2_introduction.md) |
| 17.3 | Draft Chapter 16 outlook | B+H | [17_3_outlook.md](../tasks/17_3_outlook.md) |

### Integration

| # | Task | Owner | File |
|---|---|---|---|
| 17.4 | Propagate `\ref`s across chapters using the chosen build route | B | [17_4_cross_refs.md](../tasks/17_4_cross_refs.md) |
| 17.5 | Consolidate `tqft_review.bib`, check for orphans | B | [17_5_bib_consolidation.md](../tasks/17_5_bib_consolidation.md) |
| 17.6 | Add chapter-to-chapter pedagogical glue (1–2 closing sentences per chapter) | B+H | [17_6_chapter_glue.md](../tasks/17_6_chapter_glue.md) |
| 17.7 | Generate TikZ figures; extract experimental figures | B+H | [17_7_figure_generation.md](../tasks/17_7_figure_generation.md) |
| 17.8 | Audit the paper's core deliverables: gluing example (Ch 3), FQH connection (Ch 5), dictionary table (Ch 8), caveats sections (Ch 11-13) | B+H | [17_8_must_include_audit.md](../tasks/17_8_must_include_audit.md) |

### Proofreading

| # | Task | Owner | File |
|---|---|---|---|
| 17.9 | Math correctness pass (reads down the claim ledger) | B | [17_9_math_proof_pass.md](../tasks/17_9_math_proof_pass.md) |
| 17.10 | Physics and experimental-citation pass | H | [17_10_physics_proof_pass.md](../tasks/17_10_physics_proof_pass.md) |
| 17.11 | Prose pass, purge AI-tell phrases | B+H | [17_11_prose_pass.md](../tasks/17_11_prose_pass.md) |

### Appendices

| # | Task | Owner | File |
|---|---|---|---|
| A.1 | Appendix A: category theory primer (~5 pp) | B | [AA_1_category_primer.md](../tasks/AA_1_category_primer.md) |
| B.1 | Appendix B: full Frobenius ↔ 2D TQFT proof (handoff from Task 4.5) | B | — |
| C.1 | Appendix C: global CS + level quantization for general G + spin structure | B | [AC_1_cs_level_global.md](../tasks/AC_1_cs_level_global.md) |
| D.1 | Appendix D: BF ↔ $\mathbb{Z}_N$ lattice + $H^3(\mathbb{Z}_N, U(1))$ bar resolution | B | [AD_1_discrete_gauge_details.md](../tasks/AD_1_discrete_gauge_details.md) |
| E.1 | Appendix E: topological entanglement entropy derivation | B | [AE_1_tee_derivation.md](../tasks/AE_1_tee_derivation.md) |

## Acceptance criteria

- `paper/main.tex` compiles cleanly in the chosen build route, with zero undefined references.
- Abstract under 250 words, introduces the three-touchstone through-line.
- Outlook covers non-invertible symmetries (1 paragraph), SPT/SET beyond group cohomology (1), fermionic topological order (1), fault-tolerant architectures (1).
- All core deliverables confirmed present.
- All AI-tell phrases removed. Specific banned list: "we shall see", "in this chapter we have proved", "the key statement is", "an upshot of all this is", and "it can be seen/verified/shown that".
- Bibliography has no orphan entries and no undefined `\cite` calls.

## Dependencies

- Depends on: Stages II–V complete.
- Blocks: Stage VII (presentation rehearsal assumes the paper is finished).

## Risks

- **"Undefined reference" proliferation.** With ~14 chapters cross-referencing each other, this is likely. Mitigation: Task 17.4 runs the canonical compile route repeatedly; fix every warning before moving on.
- **Prose pass fatigue.** By Day 9 we will not want to do this. Mitigation: Task 17.11 is explicit about what to strip; it's mechanical rather than creative.
- **Figure generation runs long.** If TikZ figures aren't done by end of Day 8, hand-draw the cobordism diagrams on tablet / paper, scan, and insert as `\includegraphics`. Nothing in the rubric requires vector graphics.
- **Outline "must include" audit.** Easy to forget; Task 17.8 is a dedicated checklist pass.
