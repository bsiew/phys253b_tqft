---
created_at: "2026-05-05T17:39:15-04:00"
updated_at: "2026-05-05T22:03:06-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# REDUNDANCY AND IMPROVEMENT PLAN

> **Superseded by:** [`CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md`](CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md) (2026-05-05, same directory). That document provides chapter-by-chapter grading, a two-part (math+theory / experiment+application) structure, and an explicit prioritized action list with pointers into `plan/tasks/17_*`. This file is retained for archival context.

## Date: 2026-05-05
## Evaluator perspective: Grumpy, rigorous physics professor

---

## I. REDUNDANCY DIAGNOSIS

### A. Dead-weight file duplication

The `part1_*` and `part2_*` files are **entirely redundant** with the `ch*` files. They are stubs whose subsection plans map one-to-one onto the chapter structure. The mapping:

| Stub file | Corresponds to | Status of stub |
|-----------|---------------|----------------|
| `part1_01_introduction.tex` | No chapter counterpart yet | Pure TODO |
| `part1_02_mathematical_toolkit.tex` | `ch02_forms.tex` | Pure TODO; ch02 is written |
| `part1_03_ordinary_to_chern_simons.tex` | Subsumed into `ch05_chern_simons.tex` | Pure TODO; ch05 is written |
| `part1_04_tqft_and_observables.tex` | `ch03_axiomatic.tex` + `ch04_frobenius.tex` | Pure TODO; ch03/ch04 are written |
| `part2_05_response_2plus1d.tex` | `ch11_fqhe.tex` | DRAFTED; ch11 header says it migrated this |
| `part2_06_sectors_3plus1d.tex` | `ch14_sectors_3plus1d.tex` | Pure TODO; ch14 is also TODO |
| `part2_07_defects_caveats_outlook.tex` | `ch15_defects_synthesis.tex` + `ch16_outlook.tex` | Pure TODO |

**Verdict:** The `part*` files should be deleted or archived. They add zero content and create confusion about which file is authoritative.

### B. Internal content duplication

The most serious redundancy: **`chern_simons_body.tex` Section 2 ("Differential forms: a working toolkit") re-derives the entire content of `ch02_forms.tex`.**

Specifically, `chern_simons_body.tex` lines 41-80+ contain:
- Definition of p-forms (duplicates ch02 Sec 2.1)
- Wedge product and graded commutativity (duplicates ch02 Prop 2.1)
- Exterior derivative (duplicates ch02 Sec 2.3)
- Leibniz rule and d^2=0 (duplicates ch02 Lemma 2.1)
- Lie-algebra-valued forms and non-abelian F (duplicates ch02 Sec 2.3-2.5)
- Gauge transformations, Maurer-Cartan (duplicates ch02 Sec 2.5)

This is ~600 lines of duplicated material. A reader going ch02 -> ch03 -> ch04 -> ch05 encounters the same definitions, the same proofs, the same conventions *twice*. That's not pedagogy; it's a copy-paste artifact from when `chern_simons_theory.tex` was a standalone document.

### C. Conceptual overlap between chapters

- **Atiyah-Segal axioms** are stated in `ch03_axiomatic.tex` Sec 3.2 AND promised again in `chern_simons_body.tex` Section 7 ("TQFT assembly"). The axiomatic chapter gives a full treatment; the CS chapter doesn't need to restate them.
- **Wilson loops and linking** appear in the CS chapter AND are promised in `part1_04_tqft_and_observables.tex` subsection 4.4. The ch03/ch04 text doesn't cover them (wisely), but the planned overlap would be gratuitous.
- **Ground-state degeneracy on T^2** is derived in the CS chapter's canonical quantization section AND in the FQHE chapter (ch11/part2_05). These are different derivations of the same result for the same theory. That's fine if acknowledged; currently it's not.

---

## II. PEDAGOGICAL VALUE ASSESSMENT

### Target reader: "familiar with QFT but may not know all the formalism"

I take this to mean: has Schwartz or Peskin-Schroeder level QFT, knows path integrals, gauge theory, anomalies in components. Does NOT necessarily know differential forms, fiber bundles, TQFT axioms, or condensed-matter topology.

### What works

1. **`ch02_forms.tex` is genuinely excellent.** The Schwartz anchor ("you already know F_μν"), the Maxwell example making the abstract concrete, the forward pointers to level quantization, the "identity vs equation of motion = topological vs dynamical" leitmotif. This is what pedagogical exposition looks like. Grade: A.

2. **`ch03_axiomatic.tex` earns its keep.** The cobordism-as-spacetime picture, the worked disk-gluing example, the proof that closed manifolds give numbers—these make the abstract machinery tangible. The taxonomy (Schwarz/Witten/invertible) at the end is a useful orientation. Grade: A-.

3. **`ch04_frobenius.tex` is rigorous and complete.** The Morse-function generation proof, the explicit Frobenius classification, the finite-group foreshadowing for Dijkgraaf-Witten. Every statement is proved. Grade: A for mathematical correctness.

4. **The FQHE section (`part2_05`/`ch11`) is the best physics writing in the paper.** One action, three observables, each derived cleanly. The Laughlin → K-matrix generalization is well-paced. The connection back to Part I formalism (linking = braiding, anomaly inflow = edge modes) is explicit. Grade: A.

5. **`app_e_tee.tex` (topological entanglement entropy)** is a clean, self-contained derivation. Good appendix material.

### What fails

#### Problem 1: The paper doesn't know what it is

Is this a 30-page review paper for a graduate course? A 200-page textbook draft? A 500-page monograph? The current scope—16 chapters covering forms, bundles, cobordisms, Frobenius algebras, Chern-Simons, BF theory, Dijkgraaf-Witten, generalized symmetries, topological order, anyons, FQHE, interferometry experiments, topological quantum computation, QCD topology, axions, monopoles, and an outlook—is a **multi-year book project**, not a final paper. The ambition is admirable; the execution is ~40% complete and the unfinished portions are exactly the parts that would justify the claimed scope.

**Consequence for the reader:** They get 860 lines of Frobenius algebra (ch04) but zero lines on the eta-prime mass, zero lines on monopole charge quantization, zero lines on the axion, and zero lines on Maxwell-Chern-Simons. The paper promises "observables ranging from Hall response to axion physics" in its thesis statement and then delivers on exactly one of those five observable families.

#### Problem 2: The Frobenius chapter is in the wrong place

Ch04 (2D TQFT = Frobenius algebras) is a beautiful piece of mathematics. But it comes BEFORE the reader has seen Chern-Simons theory, before they know why TQFT matters, and before any physical system has been introduced. A QFT-literate reader will ask: "Why am I learning about commutative algebras classified by handle operators when I came here to understand topological phases of matter?"

The paper's own CLAUDE.md says: "Introduce standard definitions and equations before applying them" and "user preference: its better to have it centralized rather than scattered bc im always kind of frustrated at having something mathy defined and then not being able to see any consequences of that definition until pages of physics."

Ch04 violates this. The consequence of the Frobenius classification doesn't appear until ch07 (Dijkgraaf-Witten), which is 200+ pages later. The reader wades through the full algebraic classification theorem, works through the handle-element spectral decomposition, and then... moves on to Chern-Simons theory, which has nothing to do with Frobenius algebras. The payoff is deferred past the entire physical heart of the paper.

#### Problem 3: The CS chapter doesn't trust the rest of the paper

`chern_simons_body.tex` was written as a standalone document. It still reads like one. It re-derives forms, gauge transformations, the Maurer-Cartan equation, and the Atiyah-Segal axioms—all material that ch02 and ch03 already cover in greater depth and clarity. A reader who followed the book in order now reads:

- Ch02: "Here are forms. Here is d. Here is d^2=0. Here is F=dA+A∧A."
- Ch03: "Here are cobordisms. Here are the Atiyah-Segal axioms."
- Ch04: "Here is the 2D classification."
- Ch05 (=CS body): "Let me now teach you forms. Here is d. Here is d^2=0. Here is F=dA+A∧A. Later I will state the Atiyah-Segal axioms."

This is not a recap or a reminder—it's a full re-derivation with slightly different notation. The reader either skips it (losing the thread) or re-reads 600 lines of material they already know (wasting their time and patience).

#### Problem 4: No through-line from formalism to physics

After Parts I (ch02-ch08) the reader arrives at ch09 (toric code) which starts from scratch with a lattice model, not from the continuum TQFT formalism. The toric code section says "Section 9.4 is SELF-CONTAINED for BF theory: does not assume Part I has a BF chapter." So Part I developed BF theory in ch06, and then ch09 re-derives BF theory independently. Why?

Similarly, the anyons chapter (ch10) develops fusion rules, braiding, and modular data without connecting them to the CS Wilson-loop framework of ch05 until subsection 10.4. The bridge is an afterthought rather than the organizing principle.

The paper SAYS its thesis is "ordinary gauge QFT already contains topological sectors; CS isolates them; TQFT formalizes them; observables are the payoff." But the STRUCTURE of the paper is: "here's some math (ch02-04), here's CS theory standalone (ch05), here's more math (ch06-08), here's some condensed matter (ch09-13), here are some stubs (ch14-16)." The claimed narrative arc is not reflected in the actual chapter sequence.

#### Problem 5: The "iffiness" / honesty-box material is all unwritten

The paper's most distinctive pedagogical contribution—the careful taxonomy of "when is an observable strictly topological vs IR-effective vs theory-side vs model-dependent"—exists only as TODO comments. This is the material a QFT-literate reader would most benefit from. They can find forms in Nakahara, Atiyah-Segal in any TQFT review, and the FQHE derivation in Tong's lectures. What they cannot easily find elsewhere is a unified critical assessment of which "topological" claims in the literature are really topological. That assessment is the unique value proposition of this paper, and it doesn't exist yet.

#### Problem 6: The experimental chapter is a list, not an argument

Ch12 (experiments) is structured as a sequence of experiment summaries. For a QFT reader, the interesting question is not "what did Nakamura measure" but "what is the relationship between the theoretical prediction σ_xy = e²/(mh) and the quantity extracted from the interferometer data, and how many non-topological assumptions intervene?" That question is partially raised in the unwritten caveats sections but never answered. The experiments chapter should be organized by the epistemological status of the evidence, not by chronology.

#### Problem 7: Missing derivations that are repeatedly promised

- The Jones polynomial connection (promised in ch05 "Sec 8: Witten-Jones bridge") — exists as a section header in the CS body but I didn't see a full derivation.
- Non-abelian braiding matrices (promised in ch10.3-10.4) — section headers only.
- The Witten-Veneziano formula (promised in ch14.2) — pure stub.
- Level quantization for general G (promised in ch05) — the CS body does SU(2) explicitly but the generalization is stated without proof.
- The Maxwell-Chern-Simons analysis (promised in ch11.6) — pure stub.

A paper that says "we derive X from first principles" and then provides a section header is worse than a paper that never mentions X. It creates a false sense of completeness.

---

## III. EXPLICIT IMPROVEMENT PLAN

### Phase 0: Decide what this actually is (IMMEDIATELY)

Before writing another line, answer: **Is this a ~60-page review paper or a ~250-page book?**

- If a 60-page paper: chs 02, 03, 04, 05, 11, and a shortened synthesis chapter are the core. Everything else gets cut or compressed to 1-2 paragraphs of signposting.
- If a 250-page book: the current chapter list is reasonable, but 60% of it is unwritten and the timeline must be realistic.

**Recommendation:** This is a term paper for 253b. It should be 60-80 pages. The 16-chapter structure is not viable.

### Phase 1: Kill the redundancy (1-2 days)

1. **Delete or archive all `part1_*` and `part2_*` files.** They are dead weight. Their content exists in the ch* files.

2. **Gut the forms/gauge-transformation material from `chern_simons_body.tex`.** Replace Sections 2-3 of the CS body (~600 lines) with a single paragraph: "We use the conventions and results of Chapter 2; in particular, the field strength is F = dA + A∧A in anti-Hermitian convention (Eq. 2.X), and the gauge transformation law is A^g = g⁻¹Ag + g⁻¹dg (Eq. 2.Y)." The CS chapter should start at "The Chern-Simons form and its properties" (currently Section 3 of the body).

3. **Decide: does ch09 use ch06, or is ch06 cut?** If BF theory is developed in ch06, then ch09 section 9.4 should CITE ch06, not re-derive BF. If the paper is being shortened, ch06 may not survive—in which case ch09's self-contained BF insert becomes the only treatment and ch06 is deleted.

### Phase 2: Fix the structural ordering (2-3 days)

The current order (forms → axioms → Frobenius → CS → BF → DW → gensym → toric code → anyons → FQHE → ...) front-loads 200+ pages of formalism before any physics. For a QFT reader, this is deadly.

**Proposed reordering for a 60-80 page paper:**

1. **Introduction** (3-5 pp): The thesis statement, observable families, roadmap. Currently a pure stub—write it LAST.

2. **From Yang-Mills to Chern-Simons** (15-20 pp): Merge the forms toolkit (stripped to essentials—maybe 8 pp of ch02 instead of 30) with the CS construction. The reader needs forms *in order to write down CS*. Don't separate the tool from its immediate use. Include level quantization.

3. **TQFT structure and observables** (10-12 pp): Atiyah-Segal axioms, CS as the central example (Wilson loops, linking, GSD). The Frobenius classification gets 1-2 pages as a remark, not a 30-page chapter—defer the full proof to an appendix if desired.

4. **The Fractional Quantum Hall Effect** (15-20 pp): The effective action, Hall response, fractional charge, braiding, edge modes, K-matrix. This is already the best-written section. Keep it.

5. **When are the observables really topological?** (8-10 pp): The four-category taxonomy. This is currently all stubs. WRITE IT. It is the paper's unique contribution.

6. **Outlook** (2-3 pp): Point to QCD topology, monopoles, TQC as further directions without attempting full treatments.

**What gets cut or moved to appendices:**
- Ch04 (Frobenius full proof) → Appendix
- Ch06 (BF) → Folded into a remark in the TQFT chapter
- Ch07 (Dijkgraaf-Witten) → Folded into a remark or cut
- Ch08 (Generalized symmetries) → Cut for the paper; it's a separate project
- Ch09 (Toric code) → Cut or reduced to 2 paragraphs in the honesty chapter
- Ch10 (Anyons formal framework) → Subsection of the FQHE chapter
- Ch12 (Experiments) → Folded into FQHE chapter as a subsection
- Ch13 (TQC) → Cut; it's downstream of material the paper doesn't develop
- Ch14 (3+1d / axions) → Cut for the paper; mention in outlook
- Ch15 (Monopoles/synthesis) → The synthesis (honesty taxonomy) stays; monopoles → outlook

### Phase 3: Write the missing critical material (3-5 days)

In order of importance:

1. **The four-category observable taxonomy** (currently ch15 Sec 15.2 / old Sec 7.2): strict TQFT / IR response / theory-side / model-dependent. This is the intellectual payoff. For each category, give 2-3 concrete examples with explicit statements of what is and isn't topological. Currently pure TODO.

2. **Maxwell-Chern-Simons** (currently ch11 Sec 11.6): The conceptual lesson that "adding a CS term to a dynamical gauge theory does NOT give a TQFT" is essential for the QFT reader. It's the cleanest antidote to the sloppy claim "CS = topological." 2-3 pages. Currently pure TODO.

3. **The Introduction** (currently ch01): Write it last, after everything else is stable. It should state the thesis, preview the four observable families, and give the roadmap. 3-5 pages. Currently pure TODO.

4. **The FQHE caveats section** (currently ch11 Sec 11.7): What breaks in real interferometers, which edge properties are universal vs non-universal. This is what distinguishes a thoughtful review from a textbook recitation. 2-3 pages. Currently pure TODO.

### Phase 4: Polish and consistency (2-3 days)

1. **Notation audit**: The CS body uses slightly different notation from ch02 in places (e.g., the Schwartz comparison is done in both). Unify.

2. **Forward/backward references**: Currently many "see Sec. X" references point to section labels that exist in the stub files but not in actual content. Every cross-reference should point to material that exists.

3. **Bibliography**: The `.bib` file has multiple "Placeholder" entries. Replace with real references or delete the citations.

4. **Figures**: Many figure environments contain placeholder boxes. Either draw the figures or remove the float environments—a box that says "figure TBD" is worse than no figure.

---

## IV. SUMMARY VERDICT

**As a pedagogical review, this paper is currently a B+ outline attached to about 100 pages of A-quality mathematical exposition and 50 pages of stubs.** The written portions (ch02, ch03, ch04, ch05, FQHE section) are individually excellent. The problem is architectural: the paper is too ambitious, too long, structurally redundant, and critically missing the material that would make it more than a subset of existing textbooks (the honesty/taxonomy discussion).

A QFT reader who picks this up today will learn differential forms and Frobenius algebras very well, get a solid derivation of Chern-Simons observables and the FQHE, and then hit a wall of empty section headers for the remaining half of the claimed scope. The unique selling point—the unified assessment of which observables are "really topological"—is entirely unwritten.

The fix is simple in principle and painful in practice: **cut the scope by 60%, finish the remaining 40% properly, and write the honesty material that no other source provides.** A focused 60-page paper on "CS theory, its FQHE realization, and a critical assessment of topological observables" would be genuinely valuable. A 250-page half-finished omnibus review is not.
