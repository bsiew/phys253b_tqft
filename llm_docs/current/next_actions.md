# Next Actions

## Current stage

conceptual_and_formal_modeling → **paper reorganization (simplified 7-section Part I/II structure)**

## Major update: 2026-05-02

The 10-section intermediate has been simplified to a 7-section Part I / Part II structure following the user's instructions in `253b_final_paper/llm_docs/reference/Final QFT Project Overview.md` and the detailed source map in `253b_final_paper/llm_docs/reference/tqft_observables_literature_review.md`. The 10-section stubs are now in `tex_docs/archive_2026-05-02_pre_simplification/`.

New files: `tex_docs/part1_01_introduction.tex` through `tex_docs/part2_07_defects_caveats_outlook.tex`, each with inline bibliographic citations keyed to `tex_docs/tqft_observables_unresolved_refs.bib`.

## Current bottleneck

Content migration from archived files to the new Part I / Part II structure. Section 5 (2+1d response) already has the Laughlin / quasihole / edge / K-matrix prose migrated inline and cited; Sections 2, 3, 4 need extraction from archive; Sections 6 and 7 are new writing.

## Top priorities

1. **Finish Section 5**: write the Maxwell-CS contrast (5.5) and the QHE caveats (5.6) subsections.
2. **Migrate Section 2** (Mathematical Toolkit): extract eight subsections from `archive_2026-05-01/topology_review.tex` and `differential_forms_csimons_foundations_v2.tex` into `part1_02_mathematical_toolkit.tex` per its subsection plan.
3. **Migrate Section 3** (Ordinary Gauge -> CS): pull the anomaly-descent derivation from `archive_2026-05-01/differential_forms_csimons_foundations_v2.tex` and the level-quantization calculation from `archive_2026-05-01/dense_derivation_expansion.tex` into `part1_03_ordinary_to_chern_simons.tex`.
4. **Write Section 4** (TQFT + observables): functorial axioms, TQFT classes, Wilson/linking/framing, Hilbert-space / GSD, observable taxonomy; migrate worked calculations from `archive_2026-05-01/dense_derivation_expansion.tex`.
5. **Write Section 6** (3+1d sectors): theta, chi_t, eta', Witten-Veneziano, strong CP, nEDM, axion, with local caveats subsection.
6. **Write Section 7** (defects, caveats, outlook): monopoles + line operators, unified strict-vs-effective taxonomy, guide du routard.
7. **Cleanup**: replace placeholder bib keys in `tqft_observables_unresolved_refs.bib` per `253b_final_paper/llm_docs/reference/tqft_observables_unresolved_cleanup_checklist.md`.
8. **Write bookends last**: Section 1 (introduction) and Section 7.3 (closing).

## Old priorities (deferred until after content migration)

- Review compiled PDFs (previous modular structure now archived)
- Notation/cross-reference audit (will do after migration)
- Sign/normalization checks (incorporate during migration)
- Figure specification (update for new structure)
- Project-local literature notes (still needed)

## Completion signal for current phase

Phase 2 (Content Migration) complete when:
- Sections 2, 3, 4 fully migrated from `archive_2026-05-01/` content.
- Section 5 final subsections (5.5 Maxwell-CS and 5.6 QHE caveats) written.
- Sections 6 and 7 drafted from the source map in `tqft_observables_literature_review.md`.
- Inline `\cite{...}` calls resolve against `tqft_observables_unresolved_refs.bib`.
- Placeholder bib keys replaced with concrete papers.
- All TODO comments removed and FIGURE FLAGs promoted to figure specs.
- Main wrapper (`tex_docs_main_wrapper_20260501.tex`) compiles end-to-end with bibliography.

## Expected artifacts

- 7 populated section files in `253b_final_paper/tex_docs/` (Part I and Part II).
- Updated `REORGANIZATION_STATUS.md` tracking progress.
- Bibliography with all concrete entries resolved; no placeholder keys.
- Notation / convention decisions documented.
- Figure inventory updated for the new 7-section structure.
- Compiled PDF artifact in `PROJECTS/QFT/artifacts/253b_final_paper_compile/`.
- Archive files preserved (`archive_2026-05-01/` and `archive_2026-05-02_pre_simplification/`) for reference.

## Key files for this phase

- **Strategy**: `253b_final_paper/llm_docs/reference/Final QFT Project Overview.md` and `253b_final_paper/llm_docs/reference/tqft_observables_literature_review.md`
- **Legacy 10-section mapping**: `253b_final_paper/llm_docs/current/content_mapping_2026-05-01.md`  
- **Status**: `253b_final_paper/llm_docs/current/REORGANIZATION_STATUS.md`
- **Quick start (historical)**: `253b_final_paper/llm_docs/logs/2026-05-01-claude-opus-log-quick-start-guide.md`
- **Old content**: `253b_final_paper/tex_docs/archive_2026-05-01/`

## Timeline estimate

- Phase 1 (structure): ✅ Complete (2026-05-01)
- Phase 2 (content migration): ~2-3 weeks
- Phase 3 (quality control): ~1 week  
- Phase 4 (integration): ~2-3 days

**Target**: Complete reorganization in ~4-5 weeks
