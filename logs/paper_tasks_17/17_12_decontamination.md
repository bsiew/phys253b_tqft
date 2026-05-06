---
created_at: "2026-05-05T22:05:11-04:00"
updated_at: "2026-05-05T22:05:11-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.12 — LLM Decontamination Pass

**Date:** 2026-05-05
**Status:** Complete

## Summary

Eliminated all structural AI tells from tex_docs and updated all plan/tasks and llm_docs references.

## Changes to tex_docs/

### ch13_tqc.tex
- `\subsection{Required Honesty Box}` → `\subsection{Experimental Status}`
- `\label{subsec:tqc-honesty-box}` → `\label{subsec:tqc-experimental-status}`
- Killed throat-clearing paragraph ("The preceding sections developed topological quantum computation as a theoretical framework... Before proceeding to the outlook, we pause to state clearly the gap...") — replaced with one direct sentence.
- Killed `\noindent\textbf{Honesty Box: The Experimental Status...}` → `\noindent\textbf{The Experimental Status...}`
- Killed "It is worth noting that" lead-in (line 352) — sentence now starts with content directly.
- "three pillars of this scheme" → "three ingredients of this scheme"
- Header comments: replaced "honesty box" references with neutral terms.
- Updated internal `\ref{subsec:tqc-honesty-box}` → `\ref{subsec:tqc-experimental-status}` (2 instances).

### ch12_experiments.tex
- `\noindent\textbf{Honesty box: emulation versus discovery.}` → `\noindent\textbf{Caveat: emulation versus discovery.}`
- Header comment updated.

### ch11_fqhe.tex
- Three header comments: "honesty box" → "scope/limitations" or "Scope and Limitations"
- Section 11.7 opening: removed "Before moving on, we state clearly which of these predictions have been confirmed experimentally, and on which platforms." → replaced with "The experimental confirmation of these predictions varies sharply across platforms."

### ch16_outlook.tex
- "the honesty box of Section~\ref{subsec:tqc-honesty-box} stated clearly" → "Section~\ref{subsec:tqc-experimental-status} stated clearly"

### ch14_sectors_3plus1d.tex
- Killed "Before closing this chapter, we examine each link in that chain and state honestly where..." → replaced with direct question phrasing.
- "distills the four-category taxonomy of ``how topological is this observable?'' that runs through the entire paper" → "and asks, for each observable: how topological is it really?"
- "unified four-category taxonomy" → "four-category classification"

### ch15_defects_synthesis.tex
- "We now turn to the extended operators that probe the global form of the gauge group." → "The extended operators that probe the global form of the gauge group are Wilson and 't~Hooft lines."

### ch01_introduction.tex
- "a four-category taxonomy of ``when is a field theory topological?''" → "a systematic assessment of when an observable is genuinely topological versus merely topology-inspired."

## Changes to plan/tasks/

- 17_8_must_include_audit.md: all "honesty box" → "scope/limitations subsection" / "experimental status section" / "caveats"
- 17_10_physics_proof_pass.md: "Honesty-box tone" → "Caveats tone"; "Andersen honesty box sharpness" → "Andersen caveat sharpness"
- 17_11_prose_pass.md: removed "honesty box" from dependency note
- 18_2_helena_board_script.md: "honesty box on synthetic vs natural" → "caveat on synthetic vs natural"
- 18_5_cheat_cards.md: "honesty box from Ch 13 §13.3" → "experimental status from Ch 13 §13.3"

## Changes to llm_docs/

- CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md: 5 instances updated; item 26 marked [DONE]
- REDUNDANCY_AND_IMPROVEMENT_PLAN.md: 2 instances updated
- reference/compiled_literature_for_lit_review.md: 1 instance updated
- current/migration_plan_2026-05-04.md: 3 instances updated
- logs/2026-05-05-opus-log-ch14-16-task-files-and-stage.md: 1 instance updated

## Other files updated

- plan/COMPLETED_WORK_GUIDE.md
- plan/stages/stage_VI_integration.md
- plan/archive/tasks_14_16_completed/16_2_open_directions.md
- plan/notes/bibliography_pdf_shopping_list.md
- BSIEW_README.md

## Files intentionally left unchanged

- plan/tasks/17_12_decontamination_pass.md — the task spec itself (historical record)
- plan/archive/tasks_14_16_completed/11_5_honesty_box.md — archived task file (filename is the historical name)

## Acceptance criteria verification

- [x] Zero instances of "honesty box" in `tex_docs/`
- [x] Zero instances of "we pause to" / "before proceeding" / "it is worth noting" in paper body
- [x] All critical-assessment subsections have neutral, professional titles
- [x] Content of all former "honesty boxes" is preserved intact — only framing changed
- [x] "Three pillars" branding eliminated
- [x] "Four-category taxonomy" branding reduced (kept in \paragraph{} title where functional, removed from running prose)
