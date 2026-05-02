# Paper Reorganization Status - 2026-05-01

## What Was Done

### 1. Created New Structure
- Created 10 new section files following the ChatGPT conversation recommendations
- Files: `01_introduction.tex` through `10_outlook.tex`
- Each file has detailed header comments documenting:
  - Purpose and goals
  - Content checklist
  - Source files to draw from
  - Current status (TO BE WRITTEN, EXTRACT, MERGE, etc.)
  - Writing notes and guidelines

### 2. Archived Old Files
- Moved all previous modular TeX files to `tex_docs/archive_2026-05-01/`
- Archived files:
  - `topology_review.tex`
  - `differential_forms_csimons_foundations.tex`
  - `differential_forms_csimons_foundations_v2.tex`
  - `chern_simons_two_review_synthesis.tex`
  - `dense_derivation_expansion.tex`
  - `anomalies_boundaries_topological_response.tex`
  - `chern_simons_theory_FQHE_throughline_v2.tex`

### 3. Created Planning Documents
- `reorganization_plan_2026-05-01.md`: Overall strategy and rationale
- `content_mapping_2026-05-01.md`: Detailed mapping of old → new content (created by agent)
- This file: Status tracker

## New Paper Structure

### I. Introduction [TO BE WRITTEN - write last]
- Physics problem, not abstract definition
- Three key questions frame the entire paper
- 2-3 pages max

### II. Topological Structures in Ordinary QFT [TO BE WRITTEN]
- Bridge from Schwartz
- Survey: instantons, θ-term, anomalies, Wilson loops, monopoles
- End: "now look for theory where topology is central, not peripheral"
- ~10-15 pages

### III. Mathematical Toolkit [EXTRACT from topology_review.tex]
- Just-in-time math, not front-loaded
- Brief conventions and prerequisites only
- Detailed treatments moved to sections where used
- ~5 pages max

### IV. Chern-Simons from Anomalies [REORGANIZE from v2 + Brian]
- Physical motivation: anomaly descent
- CS action and why it's different (no metric)
- Use differential_forms_v2 as base, supplement with Brian's rigor
- ~15-20 pages

### V. Classical, Level, Observables [MERGE scattered content]
- Four layers: action, global structure, quantization setup, observables
- Sources: synthesis.tex + dense_derivation + Brian
- ~15-20 pages

### VI. Quantization and Functorial Emergence [EXTRACT from Brian + dense]
- Canonical quantization on surfaces
- Torus example (key!)
- Show functorial structure emerging
- ~10-15 pages

### VII. Functorial TQFT [WRITE NEW - brief]
- Atiyah-Segal axioms
- "This codifies what we already computed"
- 2-3 pages max

### VIII. Physical Applications [REORGANIZE using FQHE_v2 backbone]
- Five parts: Laughlin, anyons, anomaly inflow, torus degeneracy, nonabelian
- This is the HEART - longest section
- ~25-30 pages

### IX. Contrasts and Limits [EXTRACT + WRITE]
- What is and isn't TQFT
- Maxwell-CS, YM+θ, instantons, monopoles
- ~8-10 pages

### X. Outlook [TO BE WRITTEN - write after rest]
- Why should QFT student care?
- What does TQFT enable?
- Forward look and open questions
- ~3-5 pages

**Expected total: ~100-120 pages**

## Next Steps

### Immediate (Phase 1)
1. ✅ Create stub files with structure (DONE)
2. ✅ Archive old files (DONE)
3. ✅ Create planning documents (DONE)
4. ⏳ Review content mapping document created by agent
5. ⏳ Begin content migration starting with strongest existing content

### Phase 2: Content Migration Priority Order
Based on "build from strength" principle:

**Priority 1: Strong existing content (can migrate now)**
- Section IV: Use differential_forms_v2 as base
- Section V: Merge synthesis + dense + Brian
- Section VIII: FQHE_v2 is excellent backbone
- Section VI: Brian has good quantization story + dense has torus example

**Priority 2: Extraction/reorganization**
- Section III: Extract minimal toolkit from topology_review
- Section IX: Extract Maxwell-CS contrast and write comparison

**Priority 3: New writing (do later)**
- Section II: Survey of topological QFT features (new)
- Section VII: Brief functorial TQFT (new, but short)

**Priority 4: Bookends (write last)**
- Section I: Introduction (write when rest is done)
- Section X: Outlook (write when rest is done)

### Phase 3: Quality Control
After initial content migration:
- Notation consistency audit across all sections
- Cross-reference audit
- Figure specification for each FIGURE FLAG
- Compile test with shared preamble
- Style consistency pass

### Phase 4: Integration
- Create main wrapper document including all 10 sections
- Bibliography integration
- Final compile and review

## Key Principles to Maintain

1. **Just-in-time math**: Introduce concepts where they're used, not front-loaded
2. **Physics first**: Reader should always know physical motivation
3. **One narrative arc**: Not "math chapter" + "physics chapter"
4. **Center = Chern-Simons**: Everything else motivates or applies it
5. **Concrete before abstract**: Examples and calculations before formal axioms

## Files to Reference

- **Planning**: `reorganization_plan_2026-05-01.md`
- **Content mapping**: `content_mapping_2026-05-01.md`
- **Old content**: `tex_docs/archive_2026-05-01/`
- **Source writings**: `PROJECTS/QFT/writings/brian_chern_simons_theory.tex`, `chern_simons_review.tex`

## Dependencies for Content Migration

Before starting migration, ensure:
- [ ] Content mapping document reviewed and approved
- [ ] Notation conventions documented
- [ ] Decide on sign conventions (review dense_derivation alerts)
- [ ] Figure inventory updated for new structure

## Timeline Estimate

- Phase 1 (structure): ✅ Complete
- Phase 2 (content migration): ~2-3 weeks
  - Priority 1: ~1 week
  - Priority 2: ~3-4 days
  - Priority 3: ~3-4 days
  - Priority 4: ~2-3 days
- Phase 3 (quality control): ~1 week
- Phase 4 (integration): ~2-3 days

**Total: ~4-5 weeks to fully reorganized, migrated, integrated paper**

## Notes

- Preserve all FIGURE FLAG comments during migration
- Update cross-references as content moves
- Keep TODO comments explicit about what needs work
- Original source files remain in archive for reference
- Can work on multiple sections in parallel once mapping is clear
