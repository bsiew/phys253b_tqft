# Quick Start Guide - Paper Reorganization

## What Just Happened

Your QFT final paper has been reorganized based on the ChatGPT conversation analysis in `/Users/helenabrittain/Downloads/Final QFT Project Overview.md`.

The previous modular structure has been replaced with a 10-section narrative arc that follows the principle: **ordinary QFT problem → topological structure emerges → Chern-Simons isolates it → formal TQFT completes it**

## Where Things Are Now

### New Structure (10 sections)
```
tex_docs/
├── 01_introduction.tex                          [TO BE WRITTEN - write last]
├── 02_topological_structures_ordinary_qft.tex   [TO BE WRITTEN]
├── 03_mathematical_toolkit.tex                  [EXTRACT from archive]
├── 04_chern_simons_from_anomalies.tex          [REORGANIZE from archive]
├── 05_classical_level_observables.tex          [MERGE from archive]
├── 06_quantization_functorial_emergence.tex    [EXTRACT from archive]
├── 07_functorial_tqft.tex                      [WRITE NEW - brief]
├── 08_physical_applications.tex                [REORGANIZE from archive]
├── 09_contrasts_and_limits.tex                 [EXTRACT + WRITE]
├── 10_outlook.tex                              [TO BE WRITTEN - write last]
└── archive_2026-05-01/                         [OLD FILES - for reference]
    ├── topology_review.tex
    ├── differential_forms_csimons_foundations.tex
    ├── differential_forms_csimons_foundations_v2.tex
    ├── chern_simons_two_review_synthesis.tex
    ├── dense_derivation_expansion.tex
    ├── anomalies_boundaries_topological_response.tex
    └── chern_simons_theory_FQHE_throughline_v2.tex
```

### Planning Documents
```
llm_docs/
├── reorganization_plan_2026-05-01.md       [STRATEGY: read this first]
├── content_mapping_2026-05-01.md           [DETAILED MAPPING: what goes where]
├── REORGANIZATION_STATUS.md                [PROGRESS TRACKER: phases and timeline]
├── QUICK_START_GUIDE.md                    [YOU ARE HERE]
└── [other existing docs]
```

## Read This First

**Start here**: `reorganization_plan_2026-05-01.md`
- Why this structure
- Section-by-section rationale
- Key principles from ChatGPT conversation

**Then read**: `content_mapping_2026-05-01.md`
- Where every piece of old content should go
- What to cut, merge, or rewrite
- Handles all duplicates and overlaps

**Track progress**: `REORGANIZATION_STATUS.md`
- Current phase (just completed Phase 1: structure creation)
- Next steps (Phase 2: content migration)
- Timeline and priorities

## What to Do Next

### Option 1: Start Migrating Content (Recommended)

**Priority 1 sections (strongest existing content)**:
1. **Section VIII** (Physical Applications): `chern_simons_theory_FQHE_throughline_v2.tex` is excellent
2. **Section IV** (CS from Anomalies): `differential_forms_csimons_foundations_v2.tex` is good base
3. **Section V** (Classical/Level/Observables): Merge synthesis + dense_derivation + Brian
4. **Section VI** (Quantization): Brian + dense torus calculation

Each stub file has detailed header comments telling you:
- What to include
- Which archive files to draw from
- How to organize the content
- What to watch out for

### Option 2: Write New Content

If you prefer to write fresh rather than migrate:
- **Section II**: Topological structures in ordinary QFT (bridge from Schwartz)
- **Section VII**: Functorial TQFT (brief, ~2-3 pages)

These are mostly new writing, not reorganization of existing content.

### Option 3: Review and Plan

If you want to think before executing:
1. Read the planning documents
2. Review the content mapping
3. Look at the archived files to refresh memory
4. Decide which section to start with
5. Optionally revise the mapping if you disagree with decisions

## Quick Reference: Where Did X Go?

| Old file | Main destination | Also appears in |
|----------|-----------------|-----------------|
| `topology_review.tex` | Section III (minimal toolkit) | Sections V, VI (detailed treatments) |
| `differential_forms_v2.tex` | Section IV (CS from anomalies) | - |
| `chern_simons_two_review_synthesis.tex` | Section V (classical/level/obs) | - |
| `dense_derivation_expansion.tex` | Sections V, VI (calculations) | Throughout (worked examples) |
| `anomalies_boundaries_topological_response.tex` | Sections IV, VIII (anomalies, FQHE) | Section IX (MCS contrast) |
| `chern_simons_theory_FQHE_throughline_v2.tex` | Section VIII (physical apps) | - |
| Brian's thesis | Sections V, VI (rigor) | Throughout (supplements) |
| Helena's review | Section VIII (K-matrix) | Section IX (contrasts) |

## The Big Picture

**Before**: Math block + physics block + applications (felt disjoint)

**After**: One narrative where each math concept appears just-in-time to solve a physics problem

**Center of gravity**: Chern-Simons theory (Section V-VI)
- Everything before motivates it (Sections II-IV)
- Everything after applies or formalizes it (Sections VII-IX)
- Bookends frame it (Sections I, X)

## Key Principles

From the ChatGPT conversation, these are non-negotiable:

1. **Just-in-time math**: Don't front-load topology. Introduce π₃(G) when discussing level quantization, not in a separate math chapter.

2. **Physics first**: Reader should always know the physical motivation. No "here's some math" without "here's why we need it."

3. **Concrete before abstract**: Show Laughlin states and torus Hilbert space BEFORE Atiyah-Segal axioms.

4. **One argument**: This is not "math chapter" + "physics chapter." It's one story about how topology reorganizes gauge theory.

5. **Target audience mindset**: "I already know the raw materials (Schwartz QFT). What changes now is how they are organized."

## FAQ

**Q: Can I change the structure?**
A: Yes, but read the rationale first. The structure comes from specific recommendations about how to motivate TQFT for a Schwartz-trained reader.

**Q: What if I disagree with a mapping decision?**
A: Update `content_mapping_2026-05-01.md` with your decision and rationale. It's a living document.

**Q: Do I need to migrate all content?**
A: No. Cut ruthlessly. The mapping document already flags content to cut. Quality over completeness.

**Q: How do I handle duplicates?**
A: `content_mapping_2026-05-01.md` has decisions for every major duplicate. Use the recommended version.

**Q: Should I write intro first?**
A: **NO.** Write it LAST (after Sections II-IX). You can't frame the paper until you know what's in it.

**Q: What about figures?**
A: All FIGURE FLAG comments preserved during migration. Update `figure_wishlist.md` aligned to new structure later.

**Q: How long will this take?**
A: Estimate: ~4-5 weeks for complete reorganization. But you can work section-by-section and have partial results much sooner.

## Status Check

- [x] Structure created (10 stub files)
- [x] Old files archived
- [x] Planning documents written
- [ ] Content mapping reviewed
- [ ] Content migration begun
- [ ] Priority 1 sections completed
- [ ] New writing completed
- [ ] Bookends written
- [ ] Quality control pass
- [ ] Final integration and compile

**You are here**: ⬆ Beginning of content migration phase

## Get Started

1. Open `reorganization_plan_2026-05-01.md` and read Section I-X descriptions
2. Open `content_mapping_2026-05-01.md` and skim the mapping tables
3. Pick a Priority 1 section (recommend Section VIII or IV)
4. Open the stub file, read header comments
5. Open archive file(s) listed in header
6. Start migrating/reorganizing content following instructions
7. Update `REORGANIZATION_STATUS.md` when section is complete

## Help

- **Strategy questions**: See `reorganization_plan_2026-05-01.md`
- **"Where does X go?"**: See `content_mapping_2026-05-01.md`
- **"What's next?"**: See `REORGANIZATION_STATUS.md`
- **"How do I write this?"**: See section stub file header comments
- **Style questions**: See `writing_style_guide.md`

Good luck! The hard organizational thinking is done. Now it's execution.
