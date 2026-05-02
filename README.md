# QFT Final Paper - 253b

## Project Overview

Comprehensive review paper on TQFTs in physics, structured around Chern-Simons theory, with mathematical foundations, explicit computations, and emphasis on what topological reformulations let us understand or compute better.

**Target audience**: Graduate student with Schwartz-level QFT knowledge

**Core thesis**: Ordinary gauge QFT already contains topological sectors, characteristic classes, anomalies, and nonlocal observables; Chern-Simons theory is where these structures become the defining data; the functorial TQFT program is the conceptual completion of that story.

## Repository Structure

### `/tex_docs/`
Simplified Part I / Part II structure (7 files, 2026-05-02):

Part I: Construction
- `part1_01_introduction.tex` - [TO WRITE - write last]
- `part1_02_mathematical_toolkit.tex` - [EXTRACT from archive]
- `part1_03_ordinary_to_chern_simons.tex` - [REORGANIZE]
- `part1_04_tqft_and_observables.tex` - [MERGE + write]

Part II: Physics organized by observable family
- `part2_05_response_2plus1d.tex` - [PARTIALLY DRAFTED; subs. 5.5, 5.6 TODO]
- `part2_06_sectors_3plus1d.tex` - [NEW WRITING]
- `part2_07_defects_caveats_outlook.tex` - [NEW WRITING]

Wrapper: `tex_docs_main_wrapper_20260501.tex`
Bibliography: `tqft_observables_unresolved_refs.bib`

Previous organizations preserved under:
- `tex_docs/archive_2026-05-01/` (original 7 modular drafts)
- `tex_docs/archive_2026-05-02_pre_simplification/` (2026-05-01 10-section intermediate)

### `/llm_docs/`
Planning and review documents, split by lifecycle:
- `current/` - active status, mapping, strategy, style, and figure guidance
- `reference/` - long-lived literature and background review notes
- `logs/` - generated session summaries, imported conversation records, and historical handoff notes

### `/style_guide_docs/`
Writing style examples from previous papers (for reference)

## Current Status (2026-05-01)

**Phase**: Structure created, beginning content migration

**Last major update**: Reorganization based on external conversation analysis
- Created new 10-section structure following physics-first narrative arc
- Archived previous modular files
- Created comprehensive planning and mapping documents

**Next steps**: 
1. Review content mapping document
2. Begin migrating Priority 1 content (strongest existing sections)
3. See `llm_docs/current/REORGANIZATION_STATUS.md` for detailed plan

## Paper Structure Philosophy

**Core organizing principle**: Start from QFT problem reader already understands → show where ordinary QFT forces topological language → Chern-Simons emerges as clean theory → formalize as TQFT

**NOT**: Math chapter + physics chapter as separate books  
**YES**: One argument where each mathematical idea appears when it resolves a physical problem

**Key principles**:
1. Just-in-time math (not front-loaded)
2. Physics motivation always clear
3. Concrete before abstract (calculations before axioms)
4. Chern-Simons at center (everything else motivates or applies it)
5. One narrative arc, not disjoint pieces

## Source Materials

**Within this repository**:
- `PROJECTS/QFT/writings/brian_chern_simons_theory.tex` - Mathematical treatment
- `PROJECTS/QFT/writings/chern_simons_review.tex` - Physics-motivated review

**Archived previous drafts**:
- `tex_docs/archive_2026-05-01/` - Previous modular organization

## Key Documents for Reorganization

1. **Strategy**: `llm_docs/current/reorganization_plan_2026-05-01.md`
   - Rationale for new structure
   - Section-by-section purpose and goals
   - Content sources and migration strategy

2. **Mapping**: `llm_docs/current/content_mapping_2026-05-01.md`
   - Line-by-line mapping old → new
   - Duplicate resolution decisions
   - What to cut, merge, or rewrite

3. **Status**: `llm_docs/current/REORGANIZATION_STATUS.md`
   - Current phase and progress
   - Next steps and timeline
   - Dependencies and quality gates

## Working with This Paper

### To continue content migration:
1. Check `llm_docs/current/REORGANIZATION_STATUS.md` for current phase
2. Consult `llm_docs/current/content_mapping_2026-05-01.md` for which old content maps to which new section
3. Reference archived files in `tex_docs/archive_2026-05-01/` as needed
4. Each new section file has header comments with detailed migration instructions

### To write new sections:
- Sections I, II, VII, X need new writing
- Each stub file has purpose, content checklist, and guidelines in header comments
- Maintain physics-first narrative arc
- See `llm_docs/current/writing_style_guide.md` for style guidance

### Quality control checklist:
- [ ] Notation consistency across sections (document in state files)
- [ ] Cross-references updated
- [ ] FIGURE FLAGs specified in figure inventory
- [ ] Compiles with shared preamble
- [ ] Style consistent with pedagogical guidelines

## Expected Final Product

- **Length**: ~100-120 pages
- **Audience**: Advanced undergrad / early grad student
- **Style**: Pedagogical review with worked calculations
- **Key feature**: Shows how topological structures in ordinary QFT → Chern-Simons → TQFT formalism → physical applications
- **Main application**: Fractional Quantum Hall Effect and anyonic physics

## Contact / Notes

- Project coordination in `PROJECTS/QFT/state/`
- Literature notes in `PROJECTS/QFT/literature/`
- Shared research tools at workspace root `scripts/` and `research_tools/`
