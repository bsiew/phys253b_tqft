# QFT Final Paper - 253b

## Project Overview

Comprehensive review paper on TQFTs in physics, structured around Chern-Simons theory, with mathematical foundations, explicit computations, and emphasis on what topological reformulations let us understand or compute better.

**Target audience**: Graduate student with Schwartz-level QFT knowledge

**Core thesis**: Ordinary gauge QFT already contains topological sectors, characteristic classes, anomalies, and nonlocal observables; Chern-Simons theory is where these structures become the defining data; the functorial TQFT program is the conceptual completion of that story.

## Repository Structure

### `/tex_docs/`
Main paper sections (10 files):
- `01_introduction.tex` - [TO BE WRITTEN]
- `02_topological_structures_ordinary_qft.tex` - [TO BE WRITTEN]
- `03_mathematical_toolkit.tex` - [EXTRACT]
- `04_chern_simons_from_anomalies.tex` - [REORGANIZE]
- `05_classical_level_observables.tex` - [MERGE]
- `06_quantization_functorial_emergence.tex` - [EXTRACT]
- `07_functorial_tqft.tex` - [WRITE NEW]
- `08_physical_applications.tex` - [REORGANIZE]
- `09_contrasts_and_limits.tex` - [EXTRACT + WRITE]
- `10_outlook.tex` - [TO BE WRITTEN]

See `tex_docs/archive_2026-05-01/` for previous modular organization.

### `/llm_docs/`
Planning and review documents:
- `reorganization_plan_2026-05-01.md` - Overall strategy based on ChatGPT conversation analysis
- `content_mapping_2026-05-01.md` - Detailed old→new content mapping
- `REORGANIZATION_STATUS.md` - Current status and next steps (this tracks progress)
- `figure_wishlist.md` - Figure specifications
- `writing_style_guide.md` - Style guidelines
- Other review and planning docs

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
3. See `llm_docs/REORGANIZATION_STATUS.md` for detailed plan

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

1. **Strategy**: `llm_docs/reorganization_plan_2026-05-01.md`
   - Rationale for new structure
   - Section-by-section purpose and goals
   - Content sources and migration strategy

2. **Mapping**: `llm_docs/content_mapping_2026-05-01.md`
   - Line-by-line mapping old → new
   - Duplicate resolution decisions
   - What to cut, merge, or rewrite

3. **Status**: `llm_docs/REORGANIZATION_STATUS.md`
   - Current phase and progress
   - Next steps and timeline
   - Dependencies and quality gates

## Working with This Paper

### To continue content migration:
1. Check `llm_docs/REORGANIZATION_STATUS.md` for current phase
2. Consult `llm_docs/content_mapping_2026-05-01.md` for which old content maps to which new section
3. Reference archived files in `tex_docs/archive_2026-05-01/` as needed
4. Each new section file has header comments with detailed migration instructions

### To write new sections:
- Sections I, II, VII, X need new writing
- Each stub file has purpose, content checklist, and guidelines in header comments
- Maintain physics-first narrative arc
- See `llm_docs/writing_style_guide.md` for style guidance

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
