---
created_at: "2026-05-01T17:25:51-04:00"
updated_at: "2026-05-02T18:16:10-04:00"
generated_by: "claude"
timestamp_source: "filesystem_birthtime"
---

# Paper Reorganization Summary - 2026-05-01

## What Was Done

Your QFT final paper has been completely reorganized based on the ChatGPT conversation analysis from `/Users/helenabrittain/Downloads/Final QFT Project Overview.md`.

## The Problem That Was Solved

The previous structure felt like separate blocks (math + physics + applications) rather than one coherent argument. The ChatGPT conversation identified that the paper needed to:

1. **Start from familiar ground**: Bridge from Schwartz-level QFT, not jump into abstract TQFT
2. **Introduce math just-in-time**: Not front-loaded topology, but concepts appearing when needed
3. **Center on Chern-Simons**: Make CS theory the heart, with everything else motivating or applying it
4. **Build one narrative**: Show how topological structure in ordinary QFT → CS theory isolates it → TQFT formalizes it

## The New Structure

### 10 Sections Following Physics-First Arc

**I. Introduction** [write last]
- Frame the physics problem, not abstract math
- Three key questions guide the entire paper

**II. Topological Structures in Ordinary QFT** [new writing needed]
- Bridge from Schwartz: instantons, θ-term, anomalies, Wilson loops, monopoles
- "You already know these. Now let's reorganize them."

**III. Mathematical Toolkit** [extract minimal from old topology_review]
- Brief conventions only (~5 pages)
- Detailed treatments moved to sections where used

**IV. Chern-Simons from Anomaly Descent** [reorganize from v2]
- Physical motivation first
- Shows how CS action emerges

**V. Classical Solutions, Level Quantization, Observables** [merge 3 sources]
- Four layers: action, global structure, quantization setup, observables
- π₃(G) and level quantization here

**VI. Quantization on Surfaces** [extract from Brian + dense]
- Canonical quantization → Hilbert spaces H(Σ)
- Torus example (explicit calculation)
- Functorial structure emerges

**VII. Functorial TQFT** [write new, brief ~2-3 pages]
- Atiyah-Segal axioms
- "This codifies what we already computed"

**VIII. Physical Applications** [reorganize using FQHE_v2 backbone] ← **HEART OF PAPER**
- Five parts: Laughlin, anyons, anomaly inflow, torus degeneracy, nonabelian
- Shows why TQFT matters for physics (~25-30 pages)

**IX. Contrasts and Limits** [extract + write]
- What is and isn't TQFT
- Maxwell-CS contrast, YM+θ, instantons, monopoles

**X. Outlook** [write last]
- Why should QFT student care?
- What does TQFT perspective enable?

## What Changed

### Before (problematic aspects)
- Math front-loaded in one big block
- Felt like "topology chapter" + "physics chapter" glued together
- Functorial TQFT introduced before reader saw why it's useful
- Applications felt disconnected from formalism

### After (improvements)
- Math introduced just-in-time when needed to solve physics problem
- One narrative arc: ordinary QFT → topological structure → CS isolates it → TQFT formalizes → applications
- Chern-Simons as clear center of gravity (Sections IV-VI)
- Applications (Section VIII) connected to formalism developed in Sections IV-VII
- Bookends (I, X) frame everything after content is established

## Files and Locations

### New structure
- **Section files**: `253b_final_paper/tex_docs/01_introduction.tex` through `10_outlook.tex`
- **Each file has**: Detailed header comments with purpose, sources, migration instructions

### Archived old structure
- **Location**: `253b_final_paper/tex_docs/archive_2026-05-01/`
- **Files preserved**: All 7 previous modular TeX files
- **Status**: Reference only, no longer active

### Planning documents
- **Strategy**: `llm_docs/reference/Final QFT Project Overview.md` and `llm_docs/reference/tqft_observables_literature_review.md`
- **Mapping**: `llm_docs/current/content_mapping_2026-05-01.md` (detailed, created by agent)
- **Status**: `llm_docs/current/REORGANIZATION_STATUS.md` (progress tracker)
- **Quick start**: `llm_docs/logs/2026-05-01-claude-opus-log-quick-start-guide.md` (historical oriented guide)
- **This file**: `REORGANIZATION_SUMMARY.md` (high-level overview)

## Key Principles (from ChatGPT conversation)

These are the organizing principles for the new structure:

1. **Just-in-time math**: π₃(G) appears with level quantization, not in separate topology chapter
2. **Physics first**: Always clear physical motivation before mathematical formalism
3. **Concrete before abstract**: Laughlin states and torus H(T²) BEFORE Atiyah-Segal axioms
4. **One argument**: Not disjoint blocks, but one story
5. **Reader mindset**: "I know the raw materials (Schwartz QFT), now they're reorganized"
6. **Center = CS**: Everything before motivates it, everything after applies or formalizes it

## What Happens Next

### Phase 1: Structure ✅ COMPLETE (2026-05-01)
- Created 10 stub files with detailed instructions
- Archived old files
- Created comprehensive planning documents

### Phase 2: Content Migration (current, ~2-3 weeks)
**Priority 1** (strong existing content):
- Section VIII: Use FQHE_v2 as backbone
- Section IV: Use differential_forms_v2 as base
- Sections V, VI: Merge from multiple sources

**Priority 2** (extraction/reorganization):
- Section III: Extract minimal from topology_review
- Section IX: Extract Maxwell-CS contrast

**Priority 3** (new writing):
- Section II: Survey of topological features in QFT
- Section VII: Brief functorial TQFT

**Priority 4** (bookends - write last):
- Section I: Introduction
- Section X: Outlook

### Phase 3: Quality Control (~1 week)
- Notation consistency audit
- Cross-reference audit
- Figure specification
- Compile test
- Style consistency

### Phase 4: Integration (~2-3 days)
- Main wrapper document
- Bibliography integration
- Final compile and review

**Total timeline**: ~4-5 weeks for complete reorganization

## How to Use This New Structure

### To continue the work:
1. **Read strategy first**: `llm_docs/reference/Final QFT Project Overview.md` and `llm_docs/reference/tqft_observables_literature_review.md`
2. **Consult legacy mapping only as needed**: `llm_docs/current/content_mapping_2026-05-01.md` 
3. **Track progress**: `llm_docs/current/REORGANIZATION_STATUS.md`
4. **Historical quick reference**: `llm_docs/logs/2026-05-01-claude-opus-log-quick-start-guide.md`

### To migrate content:
- Each section stub file has header comments with:
  - Purpose and goals
  - Source files to draw from
  - Content checklist
  - Migration instructions
  - Warnings and notes

### To check status:
- `llm_docs/current/REORGANIZATION_STATUS.md` tracks:
  - Current phase
  - What's complete
  - What's next
  - Dependencies and blockers

## Core Insight from Reorganization

The ChatGPT conversation revealed the key issue:

**Your professor's distinction**: "We're doing topological stuff but not TQFT"

**The solution**: Paper should show the PROGRESSION:
- Topological sectors/charges in ordinary QFT (Section II)
- → Chern-Simons theory where topology becomes central (Sections IV-VI)
- → Formal TQFT as completion (Section VII)
- → Applications showing why this matters (Section VIII)
- → Clarity on the distinction (Section IX)

This progression resolves the apparent tension between:
- Lecture material (topological features in Yang-Mills, monopoles, etc.)
- Your project (TQFT proper, Chern-Simons, functorial formalism)

They're not separate topics - they're stages in one story.

## Questions?

- **"Where did X content go?"**: See `content_mapping_2026-05-01.md`
- **"Why this structure?"**: See `Final QFT Project Overview.md` and `tqft_observables_literature_review.md`
- **"What should I do next?"**: See `REORGANIZATION_STATUS.md`
- **"How do I start?"**: See `2026-05-01-claude-opus-log-quick-start-guide.md`

## Bottom Line

You now have:
- ✅ A clear 10-section structure following physics-first narrative
- ✅ All old content preserved in archive
- ✅ Detailed migration instructions for every section
- ✅ Comprehensive planning and mapping documents
- ✅ Progress tracking framework

Ready to execute Phase 2: content migration.

The hard organizational thinking is done. Now it's systematic execution following the plan.
