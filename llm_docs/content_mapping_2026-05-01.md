# Content Mapping for QFT Paper Reorganization

**Created:** 2026-05-01  
**Purpose:** Map existing content from TeX files to new target sections I-X  
**Source:** Reorganization plan at `llm_docs/reorganization_plan_2026-05-01.md`

---

## Summary

This document maps all major content from the existing TeX files in `253b_final_paper/tex_docs/` and `writings/` to the new 10-section structure. Each entry specifies:
- **Source**: Original file and section/subsection
- **Destination**: Target section (I-X) in the reorganized paper
- **Action**: Copy, rewrite, merge, cut, or create new
- **Notes**: Dependencies, duplicates, or special handling

---

## Section I: Introduction (NEEDS TO BE WRITTEN)

### Status
No existing content. Must be written fresh.

### Required Content
- State the physics problem: what is topological structure inside ordinary QFT?
- Why does Chern-Simons theory isolate that structure cleanly?
- How does this lead to the formal TQFT framework?
- Roadmap of the paper

### Dependencies
- Must be written after the rest of the paper is complete
- Should reference specific results from Sections II-IX

---

## Section II: Topological Structures in Ordinary Gauge Theory (PARTIALLY EXISTS)

### From `topology_review.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 24-49: Homotopy groups | π₁, π₃, fundamental groups | II (intro to homotopy) | **Rewrite** | Keep lightweight, physics-oriented. Current version too abstract |
| Lines 51-73: π₁(S¹), π₁(T²) | Circle and torus examples | II (examples) | **Copy with editing** | Good concrete examples |
| Lines 75-114: π₃(SU(2)), fibrations | Higher homotopy, level quantization preview | II (π₃ and winding) | **Merge and condense** | Distribute: keep physics motivation here, formal proof later |

**Overlap/Duplicate Note:** The π₃(SU(2)) calculation appears in multiple files. See Section V for full derivation.

### From `differential_forms_csimons_foundations.tex` and `_v2.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| v1, lines 1-22: Motivation | Why forms? Schwartz bridge | II (intro) | **Cut** | Too meta. Replace with direct physics motivation |
| v2, lines 14-22: Physical motivation | Anomaly descent, why CS | II (intro paragraph) | **Adapt** | Better starting point than v1 |
| v1, lines 24-86: Forms toolkit | Differential forms, exterior derivative | III (just-in-time math) | **Move to Section III** | Not part of "ordinary QFT" story |
| v2, lines 24-84: Forms and orientation | Same as v1 but cleaner | III | **Prefer v2 version** | Better sign explanations |

**Action:** Section II needs NEW CONTENT on:
- Yang-Mills vacua and large gauge transformations
- Instanton number and π₃(G)
- θ-term in QCD
- Anomalies and descent (Schwartz Ch. 30 bridge)
- Wilson loops as nonlocal observables
- Monopoles and charge quantization

**Source for new content:** Class notes (mentioned in reorganization plan), Schwartz excerpts, and standard QFT texts.

---

## Section III: Mathematical Toolkit (DISTRIBUTE AS NEEDED)

This section does NOT exist as a standalone block. Math should appear just-in-time throughout Sections IV-VII.

### From `topology_review.tex` (BREAK UP AND DISTRIBUTE)

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 116-169: Bundles, connections, characteristic classes | Basic gauge-field geometry | IV (when introducing CS action) | **Extract and simplify** | Keep only what's needed for transgression |
| Lines 171-226: Homology, cohomology, Poincaré duality | Linking, de Rham | V (Wilson loops section) | **Move to linking discussion** | Only introduce when computing Wilson loops |
| Lines 228-280: Lie groups and homotopy | SU(2)≅S³, SO(3), π₁(U(n)) | V (level quantization) | **Distribute** | Each fact appears when used |
| Lines 282-328: Holonomy and flat connections | Parallel transport, flat moduli space | V (classical solutions) | **Move to flatness section** | Core content for Section V |
| Lines 330-390: Symplectic geometry, moment maps | Moduli space structure | VI (quantization on surfaces) | **Move to quantization** | Appears when discussing phase space |
| Lines 392-474: Bordism and TQFT axioms | Functorial TQFT definition | VII (formal TQFT) | **Condense and move** | Most of this goes to Section VII |

**Action:** Delete `topology_review.tex` as a standalone file. Redistribute all subsections to where they're used.

### From `differential_forms_csimons_foundations_v2.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 24-84: Differential forms basics | Forms, wedge, exterior derivative | IV (early subsection) | **Keep concise version** | Introduce just before CS action |
| Lines 86-120: Gauge curvature | F = dA + A∧A, gauge transformations | IV (before transgression) | **Copy with sign checks** | Essential setup for Section IV |
| Lines 122-164: Transgression identity | dω_CS = Tr(F∧F) | IV (central result) | **Keep as main derivation** | This is the heart of Section IV |

---

## Section IV: Chern-Simons Theory from Anomaly Descent (EXISTS, NEEDS RESTRUCTURING)

### From `differential_forms_csimons_foundations_v2.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 14-22: Physical motivation | Anomaly → CS current → 3D action | IV (opening) | **Use as introduction** | Better than v1 version |
| Lines 122-212: Transgression derivation | dω_CS = Tr(F∧F), full proof | IV (main body) | **Keep, clean up notation** | Central calculation |
| Lines 214-266: Gauge transformation of ω_CS | CS not gauge-invariant, WZ term | IV (before level quantization) | **Keep full derivation** | Needed for Section V |
| Lines 268-320: Euler-angle winding | Explicit π₃ integral | IV or V | **Decision needed** | Could go here or in level quantization |
| Lines 322-376: Flatness and moduli | F=0, boundary terms, conventions | IV (end) → V (start) | **Split** | EOM here, moduli in V |

### From `differential_forms_csimons_foundations.tex` (v1)

**Status:** v2 is superior. Use v1 only for missing details.

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 149-164: Transgression identity | Same as v2 but less clean | IV | **Discard, use v2** | v2 has better sign tracking |

### From `anomalies_boundaries_topological_response.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 23-69: Anomaly inflow intro | Boundary variation of CS action | IV (end subsection) | **Merge with v2 boundary discussion** | Sets up Section VIII boundary modes |

**Duplicate Alert:** Transgression identity appears in:
- `differential_forms_csimons_foundations.tex` (v1)
- `differential_forms_csimons_foundations_v2.tex` (better)
- `chern_simons_two_review_synthesis.tex` (summary version)
- `writings/brian_chern_simons_theory.tex` (most detailed)

**Action:** Use v2 as base, supplement with Brian's detailed proof if needed for pedagogy.

---

## Section V: Classical Solutions, Level Quantization, Wilson Observables (EXISTS, SCATTERED)

### From `chern_simons_two_review_synthesis.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 36-53: Schwartz bridge | How CS appears in Schwartz | V (intro) or IV | **Decision needed** | Could be intro to Section IV instead |
| Lines 55-90: Gauge invariance and level | k∈ℤ from large gauge transformations | V (layer 2) | **Core content** | Main level-quantization statement |
| Lines 92-118: Flatness and moduli | F=0, Hom(π₁,G)/G | V (layer 1 and 3) | **Central content** | Classical solutions |
| Lines 120-160: Torus quantization | U(1)_k on T², dim H = k | V or VI | **Could go either place** | Canonical quantization preview |
| Lines 162-196: Wilson loops and framing | Wilson lines, linking, self-linking | V (layer 4) | **Core observables** | Keep here |
| Lines 198-229: Nonabelian roadmap | SU(2), Jones polynomial mention | V (layer 4 end) | **Brief roadmap** | Don't prove, just state structure |

### From `dense_derivation_expansion.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 26-82: Component dictionary | Forms ↔ components, F∧F | V or Appendix | **Decision needed** | Useful but disrupts flow |
| Lines 84-115: Quartic trace vanishes | Tr(A⁴)=0 proof | IV (transgression derivation) | **Merge into Section IV** | Technical detail for transgression |
| Lines 117-208: Gauge transformation, full | Detailed CS gauge law derivation | V (level quantization) | **Extract key steps** | Too dense for main text, use for checks |
| Lines 210-434: Euler-angle SU(2) winding | Explicit 24π² calculation | V (layer 2) | **Essential calculation** | Keep in main text or detailed appendix |
| Lines 439-509: Torus quantization details | Symplectic form, Wilson algebra | VI | **Move to Section VI** | Belongs with canonical quantization |
| Lines 511-541: Theta wavefunctions | Geometric quantization on T² | VI | **Move to Section VI** | Detailed quantization |
| Lines 543-642: Abelian Wilson loops | Gaussian path integral, linking | V (layer 4) | **Use as main Wilson calculation** | Excellent explicit derivation |
| Lines 644-674: Framing | Self-linking and framing shifts | V (layer 4) | **Include in observables** | Essential for completeness |
| Lines 676-713: K-matrix formulas | Multi-component abelian theory | V (end) or VIII | **Brief mention here, full in VIII** | Framework preview |
| Lines 715-742: Chiral edge boson | Boundary mode from bulk variation | VIII | **Move to applications** | Physical application |
| Lines 744-794: Maxwell-Chern-Simons | Topological mass, contrast | IX | **Move to contrasts section** | Shows what CS is NOT |

**Action:** `dense_derivation_expansion.tex` is a goldmine of worked calculations. Extract and distribute to Sections IV, V, VI, VIII, IX. Keep file as computational reference.

### From `writings/brian_chern_simons_theory.tex`

This is the most complete mathematical treatment. Use for detailed proofs and notation consistency checks.

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 157-223: Forms toolkit | Comprehensive forms review | III/IV | **Use for detailed explanations** | Most thorough forms introduction |
| Lines 390-486: Transgression derivation | Most detailed proof of dω_CS=Tr(F∧F) | IV | **Use for full proof** | Better than any other version |
| Lines 488-632: Gauge transformation | Complete CS gauge law derivation | V | **Use for level quantization** | Most rigorous version |
| Lines 634-683: Maurer-Cartan | Wess-Zumino form properties | V | **Include in level quantization** | Mathematical foundation |
| Lines 684-773: CS action definition | Action, first-order nature, no metric | V (layer 1) | **Core definition section** | Essential conceptual discussion |
| Lines 774-926: Level quantization | Complete argument with Euler angles | V (layer 2) | **Main level quantization section** | Most complete treatment |
| Lines 1003-1159: Canonical quantization | Full torus derivation with theta functions | VI | **Use as main quantization section** | Most detailed treatment |

**Action:** Brian's document is the reference for rigorous derivations. Use it to fill gaps and check signs throughout Sections IV-VI.

### From `writings/chern_simons_review.tex`

Pedagogical review focused on physics. Good for motivation and applications.

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 36-155: Why CS after Schwartz | Motivation, Schwartz bridge | II or IV (intro) | **Use for motivation** | Excellent pedagogical framing |
| Lines 157-389: Forms and connections | Standard toolkit | IV | **Condense and use** | Not as detailed as Brian, but clearer |
| Lines 391-607: Transgression and level | Clean derivation | V | **Use for main text** | Good balance of detail and clarity |
| Lines 609-753: Observables | Wilson loops, linking, framing | V (layer 4) | **Use for main Wilson section** | Excellent explicit calculation |
| Lines 755-920: Summary and pointers | Conceptual chain, annotated refs | X (outlook) | **Adapt for conclusion** | Good big-picture framing |

---

## Section VI: Quantization on Surfaces, Functorial Emergence (PARTIALLY EXISTS)

### From `chern_simons_two_review_synthesis.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 120-160: U(1)_k torus | Wilson algebra, k-dimensional H | VI (main example) | **Core content** | Central example of finite-dim H |

### From `dense_derivation_expansion.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 439-541: Torus quantization | Symplectic form, Wilson ops, theta functions | VI | **Main quantization section** | Comprehensive treatment |

### From `writings/brian_chern_simons_theory.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 1003-1159: Canonical quantization | Complete torus treatment | VI | **Most detailed version** | Use as primary source |
| Lines 1161-1195: TQFT axioms | Atiyah-Segal framework | VII | **Brief mention, full in VII** | Transition to functorial picture |

**New Content Needed:**
- Emphasis on functorial structure emerging from canonical quantization
- How phase space = moduli space → finite-dim H
- Connection between symplectic volume and Hilbert space dimension
- Preview of TQFT structure (full treatment in Section VII)

---

## Section VII: Functorial TQFT and Atiyah-Segal (NEEDS TO BE WRITTEN, BRIEF)

### From `topology_review.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 392-474: Bordism and TQFT | Atiyah-Segal axioms, functorial definition | VII | **Condense drastically** | Keep only what's essential |

### From `writings/brian_chern_simons_theory.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 1161-1210: TQFT axioms | Atiyah-Segal setup, CS as TQFT | VII | **Use as skeleton** | Most complete statement |

**Status:** Should be SHORT (2-3 pages). Main message: "CS path integral is already doing functorial gluing. TQFT axioms codify this."

**Action:** Write new, concise section using Brian's axioms as template. Emphasize that this is not a new theory pasted on, but the abstract language for what CS already does.

---

## Section VIII: Physical Applications (STRONG EXISTING CONTENT)

This is the best-developed section across all files. Main task is to organize according to the 5-part sequence: Abelian theory → fractional charge → anomaly inflow → torus degeneracy → nonabelian roadmap.

### From `chern_simons_theory_FQHE_throughline_v2.tex`

This file is already well-structured for Section VIII. Much of it can be used directly.

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 14-48: FQHE puzzle | Three requirements: quantization, fractional charge, statistics | VIII (intro) | **Use as introduction** | Perfect framing for applications |
| Lines 50-94: Integrate out emergent field | Laughlin action, Hall response | VIII (part 1) | **Core abelian calculation** | Clean derivation |
| Lines 96-128: Fractional charge | Flux attachment, charge e/m | VIII (part 2) | **Central result** | Excellent explanation |
| Lines 130-196: Wilson loops and linking | Abelian linking phase calculation | VIII (part 2/3) | **Merge with braiding** | Shows charge and statistics together |
| Lines 198-254: K-matrix framework | General abelian structure | VIII (part 5 or separate) | **Decision needed** | Could be its own subsection |
| Lines 256-299: Anomaly inflow | Boundary variation, edge modes | VIII (part 3) | **Anomaly inflow section** | Critical for edge modes |
| Lines 301-351: Torus quantization | Topological degeneracy | VIII (part 4) | **Torus degeneracy** | Concrete example of topological order |
| Lines 353-365: Nonabelian roadmap | SU(2), Jones polynomial, roadmap | VIII (part 5) | **Brief nonabelian pointer** | Don't prove, just state structure |
| Lines 367-399: Maxwell-CS contrast | MCS ≠ pure CS | IX | **Move to Section IX** | This is a contrast, not an application |
| Lines 401-422: Summary | Why CS solves FQHE puzzle | VIII (end) | **Use as subsection conclusion** | Ties applications together |

**Action:** `chern_simons_theory_FQHE_throughline_v2.tex` is already well-organized for Section VIII. Use it as the primary source, supplementing with calculations from other files.

### From `anomalies_boundaries_topological_response.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 10-22: Overview | Anomaly, Hall response, contrast | VIII (intro) | **Merge with FQHE intro** | Conceptual framing |
| Lines 23-69: Anomaly inflow | Bulk boundary variation, edge cancellation | VIII (part 3) | **Core anomaly section** | Merge with FQHE version |
| Lines 71-91: Abelian edge mode | Chiral boson from bulk flatness | VIII (part 3) | **Edge mode calculation** | Explicit derivation |
| Lines 93-107: Nonabelian WZW boundary | WZW for nonabelian CS | VIII (part 5) | **Brief mention** | Nonabelian roadmap |
| Lines 109-167: Laughlin response | Hall conductivity derivation | VIII (part 1) | **Merge with FQHE version** | Duplicate, use FQHE version |
| Lines 169-203: Fractional anyons | Charge e/m, statistics π/m | VIII (part 2) | **Merge with FQHE version** | Duplicate, use FQHE version |
| Lines 205-247: K-matrix | Multi-component abelian theory | VIII (K-matrix subsection) | **Merge with FQHE K-matrix** | Combine treatments |
| Lines 249-287: Maxwell-CS | Topological mass, contrast | IX | **Move to Section IX** | Not an application of pure CS |

**Duplicate Alert:** Laughlin response, fractional charge/statistics, and K-matrix appear in both:
- `chern_simons_theory_FQHE_throughline_v2.tex` (better organization)
- `anomalies_boundaries_topological_response.tex` (more detail on anomaly inflow)

**Action:** Use FQHE_v2 as primary, supplement anomaly inflow part 3 with detailed edge-mode calculation from `anomalies_boundaries_topological_response.tex`.

### From `dense_derivation_expansion.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 676-713: K-matrix integrate out | Detailed K-matrix formulas | VIII | **Use for K-matrix subsection** | Most complete formulas |
| Lines 715-742: Chiral edge boson | Boundary kinetic term from bulk | VIII (part 3) | **Merge with anomaly section** | Technical detail for edge modes |

### From `writings/chern_simons_review.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 609-670: Abelian Wilson/linking | Clean derivation | VIII or V | **Use for explicit linking calculation** | Good pedagogical version |
| Lines 672-753: Hall response, anyons, K-matrix | Summary of applications | VIII | **Use for cross-checks** | Good conceptual framing |

**Action:** Section VIII is in good shape. Primary source: `chern_simons_theory_FQHE_throughline_v2.tex`. Supplement with:
- Anomaly inflow details from `anomalies_boundaries_topological_response.tex`
- K-matrix formulas from `dense_derivation_expansion.tex`
- Edge mode derivation from multiple sources

---

## Section IX: Contrasts and Limits (EXISTS, NEEDS ORGANIZATION)

### From `anomalies_boundaries_topological_response.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 249-287: Maxwell-CS | MCS action, topological mass | IX (main body) | **Core contrast content** | Shows CS + metric → propagating mode |

### From `dense_derivation_expansion.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 744-794: MCS topological mass | Detailed derivation, mass formula | IX | **Use as main calculation** | Most complete MCS derivation |

### From `chern_simons_theory_FQHE_throughline_v2.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 367-399: MCS contrast | CS topological, MCS not | IX | **Use for conceptual framing** | Good physics explanation |

**New Content Needed:**
- Yang-Mills with θ-term is NOT a TQFT (topological sectors, not topological dynamics)
- Topological effects in ordinary QFT vs. TQFT proper
- CS anomaly-inflow from 4D vs. 3D dynamical CS
- Table or summary distinguishing topological features

**Action:** Merge MCS content from three sources. Add NEW comparative discussion of topological sectors vs. topological theories.

---

## Section X: Outlook (NEEDS TO BE WRITTEN)

### From `chern_simons_two_review_synthesis.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 198-229: Physical fit | Why CS is powerful | X | **Adapt for outlook** | Good bullet-point summary |

### From `writings/chern_simons_review.tex`

| Source Location | Content | Destination | Action | Notes |
|----------------|---------|-------------|---------|-------|
| Lines 793-920: Summary and reading list | Conceptual chain, why TQFT matters | X | **Use as template** | Excellent concluding framing |

**Required New Content:**
- Why should a QFT student care about TQFT?
- TQFT reorganizes gauge theory around global data
- Makes quantization and response structurally transparent
- Exposes anomaly/boundary relations cleanly
- Language for universality classes and protected observables
- Bridge to condensed matter, high-energy, and math physics

**Action:** Write new conclusion synthesizing the organizing-principle perspective. Use review paper's summary as structural template.

---

## Content Not Included (CUT or ARCHIVE)

### From `topology_review.tex`
- **Lines 1-23:** Preamble and abstract - **CUT** (not part of modular snippet)
- Most of the file is distributed elsewhere, not cut entirely

### From `differential_forms_csimons_foundations.tex` (v1)
- **Most of file:** Superseded by v2 - **ARCHIVE** as reference, use v2 for main content

### Meta-commentary throughout
- Phrases like "This section deliberately slows down" or "The intended rhythm is..." - **CUT**
- Writing advice and pedagogical notes - **MOVE TO CLAUDE.md or CUT**

---

## Summary Table: Which Files Feed Which Sections

| Target Section | Primary Sources | Secondary/Reference Sources |
|---------------|----------------|----------------------------|
| I. Introduction | **NEW** | All sections (written last) |
| II. Topological Structures | **NEW + class notes** | `topology_review.tex` (examples), Schwartz Ch. 30 |
| III. Math Toolkit | **Distributed, no standalone** | `topology_review.tex`, Brian's forms section |
| IV. CS from Anomaly Descent | `differential_forms_csimons_foundations_v2.tex` | Brian's transgression proof, `anomalies_boundaries...` |
| V. Classical Solutions, Level Quantization | `chern_simons_two_review_synthesis.tex`, `dense_derivation_expansion.tex` | Brian's level quantization, review paper |
| VI. Quantization on Surfaces | `dense_derivation_expansion.tex` (torus), Brian's canonical quantization | `chern_simons_two_review_synthesis.tex` |
| VII. Functorial TQFT | **NEW (brief)** | Brian's TQFT axioms, `topology_review.tex` bordism |
| VIII. Physical Applications | `chern_simons_theory_FQHE_throughline_v2.tex` | `anomalies_boundaries_topological_response.tex`, `dense_derivation_expansion.tex` |
| IX. Contrasts and Limits | All three MCS discussions + **NEW** | Comparative discussion needed |
| X. Outlook | **NEW** | Review paper summary, synthesis conclusion |

---

## Duplicate Content: Decisions Made

| Content | Appears In | Decision | Rationale |
|---------|-----------|----------|-----------|
| Transgression identity dω_CS=Tr(F∧F) | v1, v2, Brian, synthesis, review | **Use v2 as base** | Clearest sign tracking, supplement with Brian for rigor |
| Level quantization argument | Brian (most detailed), review (clearest), synthesis (summary) | **Use review for main text, Brian for details** | Review has best pedagogy, Brian for mathematical completeness |
| Abelian Wilson loops/linking | Dense derivation, review, FQHE v2, anomalies | **Use dense_derivation as main calculation** | Most explicit Gaussian path integral |
| Laughlin Hall response | FQHE v2, anomalies_boundaries, review | **Use FQHE v2** | Best-organized narrative |
| Fractional charge/statistics | FQHE v2, anomalies_boundaries | **Use FQHE v2** | Unified with Hall response |
| K-matrix formulas | Dense derivation, FQHE v2, anomalies, review | **Use dense_derivation for formulas, FQHE v2 for context** | Most complete formulas in dense_derivation |
| Maxwell-Chern-Simons | Dense derivation, anomalies, FQHE v2 | **Use dense_derivation for calculation, FQHE v2 for contrast** | Best derivation in dense_derivation |
| Torus quantization | Dense derivation, Brian, synthesis | **Use Brian as primary, dense_derivation for details** | Brian most pedagogical, dense has theta functions |
| Edge modes/anomaly inflow | Anomalies_boundaries (most detailed), FQHE v2 (context), dense (calculation) | **Merge: use anomalies for inflow argument, FQHE v2 for physics context** | Complement each other |

---

## Key Notation and Convention Checks

Before merging content, verify consistency:

1. **Differential form conventions:**
   - v2 uses `\dd` consistently
   - Brian uses `d` for exterior derivative
   - **Decision:** Standardize on `\dd` throughout

2. **Trace normalization:**
   - Most files use Tr for fundamental rep of SU(N)
   - Check that Tr(T^a T^b) = (1/2)δ^{ab} is consistent
   - Winding number integral should give 24π² for SU(2)

3. **CS action coefficient:**
   - Standard form: S_CS = (k/4π)∫ω_CS
   - Verify this is consistent in all sources
   - Some sources absorb 2π into definition of k

4. **Sign conventions:**
   - Gauge transformation: A → g⁻¹Ag + g⁻¹dg (consistent)
   - CS gauge law: ω_CS(A^g) = ω_CS(A) - (1/3)Tr(θ³) + d(...)
   - Check signs in Euler-angle calculation
   - Hall conductivity sign depends on magnetic field orientation

5. **Wilson loop charges:**
   - Abelian: W_q(C) = exp(iq∮A)
   - Check if q is integer or allows fractional
   - Verify linking phase sign: exp(2πiq₁q₂Lk/k) or exp(-2πi...)

**Action:** Create notation file or use consistent macro definitions. Check all sign-sensitive calculations against at least two independent sources.

---

## Content Migration Strategy

### Phase 1: Sections with Strong Existing Content (Do First)
- **Section IV:** Use v2 as base, supplement with Brian's proofs
- **Section V:** Use synthesis + dense_derivation + Brian
- **Section VIII:** Use FQHE_v2 as backbone, merge in anomaly inflow details
- **Section IX:** Merge MCS discussions

### Phase 2: Sections Needing Significant New Writing (Do Second)
- **Section II:** Write new, using topology_review for examples
- **Section VI:** Adapt Brian + dense_derivation torus quantization
- **Section VII:** Write new 2-3 page functorial summary

### Phase 3: Bookend Sections (Do Last)
- **Section I:** Write after rest is complete
- **Section X:** Write after rest is complete

### Phase 4: Final Pass
- Check all cross-references
- Verify notation consistency
- Add figure placeholders (marked with FIGURE FLAG comments in several source files)
- Update bibliography
- Proofread for duplicated paragraphs or contradictory statements

---

## Next Actions

1. **Archive existing files:**
   - Move all `tex_docs/*.tex` to `tex_docs/archive_2026-05-01/`
   - Keep `writings/*.tex` in place as reference

2. **Create stub files for Sections I-X:**
   - Each with purpose, key content outline, source list, status
   - Comment blocks with this mapping document's decisions

3. **Begin content migration in this order:**
   - Section IV (transgression and CS action)
   - Section V (classical solutions, level quantization, observables)
   - Section VIII (physical applications)
   - Section VI (quantization on surfaces)
   - Section IX (contrasts)
   - Section II (ordinary QFT topological structures)
   - Section VII (functorial TQFT)
   - Section I (introduction)
   - Section X (outlook)

4. **Update related documents:**
   - `writing_pipeline.md` with new structure and migration status
   - `next_actions.md` with reorganization tasks
   - Bibliography with consistent cite keys

---

## Notes on Mathematical Rigor vs. Physics Narrative

The reorganization plan emphasizes physics-first narrative. When merging content:

- **Brian's document:** Most mathematically rigorous. Use for proofs and rigor checks.
- **Review paper:** Best pedagogical balance. Use for main text when available.
- **FQHE v2:** Best physics motivation. Use for applications and physical interpretation.
- **Dense derivation:** Best for explicit calculations. Use for worked examples and technical appendices.

**General rule:** Main text should read like the review paper. Mathematical details should be present but not obstruct the physics story. Technical calculations can go in subsections or clearly marked "Explicit Calculation" blocks.

---

## Figure Flags and Placeholders

Several source files contain `FIGURE FLAG` comments indicating where diagrams would help. Collect these into a figure wishlist aligned with the new structure.

**Action:** Create `figure_wishlist_2026-05-01.md` from existing flags.

---

**Document Status:** Complete  
**Next Step:** Create section stub files and begin content migration starting with Section IV
