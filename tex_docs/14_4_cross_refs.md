# Task 14.4 — Propagate Cross-References

- **Status:** pending
- **Owner:** Brian
- **Duration:** 45 min
- **Stage:** [VI](../stages/stage_VI_integration.md)

## Goal

Resolve every `\ref{}` so the compiled PDF has no "undefined reference" warnings.

## Steps

1. `latexmk -pdf paper/main.tex` three times (first pass builds .aux, second resolves forward refs, third catches anything missed).
2. Grep the log for `LaTeX Warning: Reference`.
3. For each unresolved reference:
   - Find the intended target.
   - If the target exists, fix the label.
   - If the target doesn't exist, either create it or replace the reference with prose.
4. Repeat until the log is clean.

## Acceptance criteria

- Zero `LaTeX Warning: Reference ... undefined` messages in the log.
- Zero `?? ??` rendered in the PDF.

## Risks

- **Dangling refs from trim decisions.** If Stage III Task 8.9 cut a section that other chapters reference, those references are orphaned. Expect to fix ~5–10 of these.
