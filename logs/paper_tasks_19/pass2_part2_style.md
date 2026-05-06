---
created_at: "2026-05-06T02:42:58-04:00"
updated_at: "2026-05-06T02:42:58-04:00"
generated_by: "us.anthropic.claude-opus-4-6-v1"
updated_by: "us.anthropic.claude-opus-4-6-v1"
timestamp_source: hook
---
# Pass 2 Style Rewrite: Part II + Introduction

**Date:** 2026-05-06  
**Scope:** ch01_introduction, ch09_topological_order, ch10_anyons, ch11_fqhe, ch12_experiments, ch13_tqc, ch14_sectors_3plus1d, ch15_defects_synthesis, ch16_outlook  
**Target voice:** David Tong lecture notes  
**Status:** COMPLETE

---

## Style principles applied

1. Physical questions open sections (not history, not formalism)
2. Equations live in sentences with punctuation
3. Short punchlines after every derivation
4. Parenthetical personality: wit in service of clarity
5. Forward references name the payoff
6. Technical precision, zero pomposity
7. Tight prose (5 sentences -> 2 where possible)
8. Passive-voice hedges killed unless physically necessary

---

## Chapter-by-chapter changes

### ch01_introduction.tex
- Section titles changed: "Scope and thesis" -> "Why topology?", "Target audience" -> "Prerequisites", "Decisions and non-coverage" -> "What we leave out"
- Opens with: "Here is a fact that ought to disturb you."
- Roadmap descriptions compressed to one-line punchy characterizations
- Two reading paths kept but made crisper

### ch09_topological_order.tex
- Killed "Plan for the remainder" paragraph
- Eliminated \medskip\noindent\textbf{} sub-headers in favor of flowing prose
- Section 9.4 opener tightened
- Reader's note made punchier
- Passive voice killed throughout

### ch10_anyons.tex
- Opening compressed to 3 sentences with physical hook ("Why does 2d physics admit...")
- Pentagon/hexagon remarks compressed
- Tension-building added in S-matrix derivation
- "The physical content of..." filler killed
- Comparison table commentary compressed ~30%

### ch11_fqhe.tex
- Merged duplicate paragraphs in 11.1 (two overlapping FQHE-discovery descriptions)
- Flux-attachment prose tightened
- Block-quote structure in 11.7 replaced with flowing paragraphs
- Signpost-y ending killed; new ending: "The fractional quantum Hall effect is not merely an application of topological field theory. It is the experimental proof that topological field theory governs macroscopic matter."

### ch12_experiments.tex
- Each experiment now opens with a question it answers
- Falsifiability statements added to each experiment
- Nakamura device paragraph compressed
- Werkmeister: focus on material independence as key novelty
- Andersen "What this is..." section compressed
- Synthesis numbered list replaced with two-sentence punchline

### ch13_tqc.tex
- Triple structure (degeneracy, protection, braiding) flows as a single argument: "three faces of a single structure, the modular tensor category"
- Experimental Status block quote compressed ~25% (all 4 points retained, punchier)
- Architecture enumerate converted to flowing prose
- Closing bridge to ch14 strengthened: ends with "...with the same force it brings to the quantum Hall effect"

### ch14_sectors_3plus1d.tex
- Opening eta-prime question preserved (already great)
- ~Half of \medskip\noindent breaks removed, paragraphs flow naturally
- Signpost phrases killed ("The logical chain:", "What makes this formula remarkable:", "The defining feature:")
- Numerical evaluation given punchline: "You weigh pions and kaons, and the answer tells you how much the gluon vacuum fluctuates between topological sectors."
- "Summary" subsubsections replaced with single-sentence forward-driving closers

### ch15_defects_synthesis.tex
- Opens with physical question: "Which bundles can exist?"
- Four-category taxonomy made authoritative (hedging phrases like "One might say..." cut)
- Each category paragraph: one-sentence definition, physical example, done
- "Upgrading and downgrading" integrated into flow (not a textbook aside)
- Final "What the taxonomy reveals" paragraph lands: the synthesis of the entire paper in three sentences

### ch16_outlook.tex
- Section 16.1 rewritten as thesis statement (2 paragraphs, not a flat chapter list)
- Each open direction opens with a physical question ("Can we classify phases whose symmetries have no inverse?")
- Five directions compressed from 10-15 lines each to 6-8 tight lines
- Guide du routard annotations: one punchy sentence per reference
- Closing paragraph rebuilt with three-beat structure (manifest / functorial / computable)
- Final two sentences isolated for impact: "Topology is not a decoration on quantum field theory. It is the load-bearing structure."

---

## Constraints respected

- No math changed (equations, labels, \ref{}, \cite{} all untouched)
- No section structure changed
- No new sections added or existing ones removed
- Header comments preserved in all files
- All \begin{definition}, \begin{proposition}, \begin{example}, \begin{remark} environments preserved
- Table environments (observable taxonomy) preserved exactly

---

## Status: PASS 2 COMPLETE for all Part II chapters + Introduction
