---
created_at: "2026-05-01T17:14:25-04:00"
updated_at: "2026-05-01T23:45:36-04:00"
generated_by: "unknown_llm"
timestamp_source: "filesystem_birthtime"
---

# Paper Reorganization Plan - 2026-05-01

## Source
Based on ChatGPT conversation analysis in `/Users/helenabrittain/Downloads/Final QFT Project Overview.md`

## Core Thesis
Ordinary gauge QFT already contains topological sectors, characteristic classes, anomalies, and nonlocal observables; Chern-Simons theory is the place where these structures stop being peripheral and become the defining data of the theory; the functorial TQFT program is then the conceptual completion of that story.

## Target Audience
Graduate student who knows standard QFT (Schwartz-level) well, familiar with gauge fields, anomalies, Wilson lines, instantons, θ-terms, symmetry, quantization, and effective actions.

## Recommended Structure (10 sections)

### I. Introduction: from standard QFT to topological organization
**Purpose**: State the physics problem, not an abstract definition
**Key questions to answer**:
- (i) what is topological structure inside ordinary QFT?
- (ii) why does Chern-Simons theory isolate that structure so cleanly?
- (iii) how does this lead to the formal TQFT framework?

**Status**: Needs to be written
**Existing content**: None yet

---

### II. Topological structures already present in ordinary gauge theory
**Purpose**: Bridge from Schwartz - make reader feel "I already know the raw materials"
**Ingredients**:
- Yang-Mills vacua and large gauge transformations
- π₃(G), instanton number
- θ-term
- Anomalies and descent
- Wilson loops as nonlocal observables
- Monopoles and charge quantization

**Status**: Partially exists in class notes (not yet integrated)
**Existing content**: Need to review `/Users/helenabrittain/Documents/Research/Playground/RESEARCH/PROJECTS/QFT/literature/` for class materials
**End goal**: Transition to "ordinary QFT contains topological sectors, but still has local propagating degrees of freedom and metric dependence. We therefore look for a theory in which the topological data are themselves the primary degrees of freedom."

---

### III. Mathematical toolkit, but only in service of Chern-Simons
**Purpose**: Just-in-time math, not front-loaded
**Organization**: Distribute concepts where they're needed:
- π₃(G) when discussing large gauge transformations and level quantization
- Holonomy and flat connections when discussing classical solutions: M_flat(M,G) ≅ Hom(π₁(M),G)/G
- Symplectic quotient when discussing canonical quantization on a surface
- Bordisms when discussing formal TQFT program

**Status**: Exists but needs reorganization
**Existing content**: 
- `tex_docs/topology_review.tex` (current comprehensive math section)
- `tex_docs/differential_forms_csimons_foundations.tex` and `_v2.tex`
**Action**: Break up `topology_review.tex` and distribute sections to where they're used

---

### IV. Chern-Simons theory from anomaly descent and transgression
**Purpose**: Motivate CS action physically before diving into structure
**Content**:
- Classical action: S_CS[A] = (k/4π)∫_M tr(A∧dA + 2/3 A∧A∧A)
- Equations of motion: F_A = 0
- Why this is different from Yang-Mills (no metric needed)

**Status**: Content exists but needs restructuring
**Existing content**:
- `tex_docs/differential_forms_csimons_foundations_v2.tex` (section on "From Anomalies to Chern-Simons Theory")
- `tex_docs/anomalies_boundaries_topological_response.tex` (anomaly inflow section)
**Action**: Extract and reorganize the anomaly→CS derivation as the entry point

---

### V. Classical solutions, level quantization, and Wilson observables
**Purpose**: Global structure of the theory
**Four layers**:
1. Classical theory: action and F_A=0
2. Global structure: large gauge transformations and level quantization via π₃(G)≅ℤ
3. Quantization: phase space is moduli space of flat G-connections on Σ
4. Observables: Wilson loops, linking, knot data, framing

**Status**: Content scattered across multiple files
**Existing content**:
- `tex_docs/chern_simons_two_review_synthesis.tex` (Schwartz current, CS action, level quantization)
- `tex_docs/dense_derivation_expansion.tex` (worked calculations)
- Parts of the Brian review in `/writings/brian_chern_simons_theory.tex`
**Action**: Merge and reorganize into the four-layer structure

---

### VI. Quantization on surfaces, moduli of flat connections, and emergence of TQFT structure
**Purpose**: Show how canonical quantization leads to functorial structure
**Key idea**: On M=ℝ×Σ, phase space is moduli space of flat connections, quantization gives Hilbert space assigned to the surface

**Status**: Partially exists
**Existing content**:
- `writings/brian_chern_simons_theory.tex` (mathematical setup)
- `tex_docs/dense_derivation_expansion.tex` (torus Hilbert space calculations)
**Action**: Extract quantization story and emphasize functorial emergence

---

### VII. Functorial TQFT and the Atiyah-Segal viewpoint
**Purpose**: Formalize what CS path integral is already doing
**Content**:
- Z: Bord_n → Vect_k as symmetric monoidal functor
- Short and clarifying, not encyclopedic
- "The functorial definition is not a separate subject pasted onto the physics; it is the abstract codification of what the Chern-Simons path integral is already doing."

**Status**: Needs to be written (should be brief)
**Existing content**: References scattered throughout but not yet synthesized
**Action**: Write new short section (~2-3 pages)

---

### VIII. Physical applications: FQHE, anyons, anomaly inflow, edge modes, torus degeneracy
**Purpose**: Cash out the formalism - show explanatory power
**Ordering**:
1. Abelian theory and Laughlin response
2. Fractional charge and braiding
3. Anomaly inflow and edge modes
4. Torus degeneracy
5. Nonabelian roadmap

**Status**: Strong existing content
**Existing content**:
- `tex_docs/chern_simons_theory_FQHE_throughline_v2.tex` (FQHE narrative)
- `tex_docs/anomalies_boundaries_topological_response.tex` (anomaly inflow, edge modes)
- `writings/chern_simons_review.tex` (K-matrix theory, Hall response)
**Action**: Organize according to the five-part sequence above

---

### IX. Contrasts and limits: Yang-Mills, Maxwell-Chern-Simons, and what is not topological
**Purpose**: Clarify the distinction between "topological effects in QFT" and "TQFT proper"
**Key contrasts**:
- Chern-Simons is topological
- Maxwell-Chern-Simons is not
- Yang-Mills with θ-term is not
- Ordinary QFT can have topological sectors without being a TQFT

**Status**: Content exists
**Existing content**:
- `tex_docs/anomalies_boundaries_topological_response.tex` (Maxwell-CS contrast)
- `writings/chern_simons_review.tex` (comparative discussion)
**Action**: Extract into dedicated comparison section

---

### X. Outlook: why TQFT is useful across QFT and condensed matter
**Purpose**: Not just summary - answer "why should a QFT student care?"
**Answer**: TQFT reorganizes gauge theory around global data, makes quantization and response coefficients structurally transparent, exposes anomaly/boundary relations cleanly, provides a language in which low-energy universality classes and protected observables become computable.

**Status**: Needs to be written
**Existing content**: Themes scattered throughout
**Action**: Write new concluding section synthesizing the "organizing principle" perspective

---

## File Reorganization Strategy

### Phase 1: Create new outline structure
- Create 10 new stub TeX files named by section (e.g., `01_introduction.tex`, `02_topological_structures_ordinary_qft.tex`, etc.)
- Each file gets the new section heading and a comment block listing:
  - Purpose
  - Key content points
  - Source files to draw from
  - Status

### Phase 2: Content mapping
- Map every subsection from existing files to new target locations
- Create `llm_docs/content_mapping.md` documenting:
  - What content goes where
  - What gets cut
  - What needs to be written fresh
  - What needs reorganization vs. copy-paste

### Phase 3: Preserve old structure
- Move current `tex_docs/*.tex` to `tex_docs/archive_2026-05-01/`
- Keep them as reference during reorganization

### Phase 4: Execute reorganization
- Systematically populate new files from old content
- Write new sections where needed
- Maintain notation and cross-reference consistency

### Phase 5: Update state files
- Update `writing_pipeline.md` with new structure
- Update `next_actions.md` with reorganization status
- Create new `figure_wishlist.md` aligned to new structure

## Key Principles from ChatGPT Conversation

1. **Do not write "math chapter" and "physics chapter" as separate books**
   - Write one argument where each mathematical idea appears at the moment it resolves a physical problem

2. **The narrative arc is**:
   - Standard QFT problem → topological structure emerges → CS theory isolates it → formal TQFT completes it

3. **Target reader mindset**:
   - "I already know the raw materials. What changes now is how they are organized."

4. **When to introduce math**:
   - Just-in-time, not front-loaded
   - Each concept appears just before it is used

5. **Center of gravity**:
   - Chern-Simons theory should be the real center of the paper
   - Everything else either motivates it or applies it

## Next Steps

1. Review and approve this reorganization plan
2. Create stub files for new structure
3. Create detailed content mapping document
4. Archive existing files
5. Begin content migration section by section
