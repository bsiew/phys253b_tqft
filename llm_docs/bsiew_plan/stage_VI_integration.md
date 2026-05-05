# Stage VI — Integration and Polish

**Duration:** 1 day (target: Day 8 afternoon through Day 9 morning).
**Lead:** joint.

## Objective

Draft front matter, back matter, and all appendices. Propagate cross-references. Install figures. Proofread three times. Consolidate the bibliography.

## Tasks

### Front and back matter

| # | Task | Owner | File |
|---|---|---|---|
| 14.1 | Draft abstract (<250 words) | B+H | [14_1_abstract.md](../tasks/14_1_abstract.md) |
| 14.2 | Draft Chapter 1 introduction | B+H | [14_2_introduction.md](../tasks/14_2_introduction.md) |
| 14.3 | Draft Chapter 14 outlook | B+H | [14_3_outlook.md](../tasks/14_3_outlook.md) |

### Integration

| # | Task | Owner | File |
|---|---|---|---|
| 14.4 | Propagate `\ref`s across chapters, three `latexmk` passes | B | [14_4_cross_refs.md](../tasks/14_4_cross_refs.md) |
| 14.5 | Consolidate `tqft_review.bib`, check for orphans | B | [14_5_bib_consolidation.md](../tasks/14_5_bib_consolidation.md) |
| 14.6 | Add chapter-to-chapter pedagogical glue (1–2 closing sentences per chapter) | B+H | [14_6_chapter_glue.md](../tasks/14_6_chapter_glue.md) |
| 14.7 | Generate TikZ figures; extract experimental figures | B+H | [14_7_figure_generation.md](../tasks/14_7_figure_generation.md) |
| 14.8 | Audit outline v2's "must include" items: gluing example (Ch 3), FQH connection (Ch 5), dictionary table (Ch 8), honesty box (Ch 12) | B+H | [14_8_must_include_audit.md](../tasks/14_8_must_include_audit.md) |

### Proofreading

| # | Task | Owner | File |
|---|---|---|---|
| 14.9 | Math correctness pass | B | [14_9_math_proof_pass.md](../tasks/14_9_math_proof_pass.md) |
| 14.10 | Physics and experimental-citation pass | H | [14_10_physics_proof_pass.md](../tasks/14_10_physics_proof_pass.md) |
| 14.11 | Prose pass, purge AI-tell phrases | B+H | [14_11_prose_pass.md](../tasks/14_11_prose_pass.md) |

## Acceptance criteria

- `paper/main.tex` compiles cleanly (zero warnings, zero undefined references) after three `latexmk` passes.
- Abstract under 250 words. Through-line updated: "Ordinary QFT contains
  topological sectors; CS isolates them; TQFT formalizes them; observable
  families organize the physics." (See migration_plan_2026-05-04.md §7.)
- Outlook (Ch 16) covers non-invertible symmetries (1 paragraph), classification
  beyond group cohomology (1), fault-tolerant architectures (1), SymTFT (1),
  lattice/holographic chi_t checks (1).
- "Must include" audit updated for new chapter numbers: gluing example (Part I
  Sec 4), FQH connection (Ch 11), anyon comparison table (Ch 10 §10.5),
  honesty boxes (Ch 11 §11.7, Ch 12 §12.3, Ch 13 §13.3).
- All AI-tell phrases removed. Specific banned list: "we shall see", "in this chapter we have proved", "the key statement is", "an upshot of all this is", "note that", "it can be seen/verified/shown that".
- Bibliography has no orphan entries and no undefined `\cite` calls.

## Dependencies

- Depends on: Stages II–V complete.
- Blocks: Stage VII (presentation rehearsal assumes the paper is finished).

## Risks

- **"Undefined reference" proliferation.** With ~14 chapters cross-referencing each other, this is likely. Mitigation: Task 14.4 runs `latexmk` repeatedly; fix every warning before moving on.
- **Prose pass fatigue.** By Day 9 we will not want to do this. Mitigation: Task 14.11 is explicit about what to strip; it's mechanical rather than creative.
- **Figure generation runs long.** If TikZ figures aren't done by end of Day 8, hand-draw the cobordism diagrams on tablet / paper, scan, and insert as `\includegraphics`. Nothing in the rubric requires vector graphics.
- **Outline "must include" audit.** Easy to forget; Task 14.8 is a dedicated checklist pass.
