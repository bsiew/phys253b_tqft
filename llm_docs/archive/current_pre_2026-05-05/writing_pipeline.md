# Writing Workflow Plan

- Project: `QFT`
- Research stage: `conceptual_and_formal_modeling`
- Writing stage: `pedagogical_rewrite`
- Recommended pack: `pedagogical_rewrite.md`
- Prompt path: `PROJECTS/_TEMPLATE/prompts/writing/pedagogical_rewrite.md`
- Target: Review the new modular TeX outputs for compile integration, notation consistency, physical motivation, and convention-safe mathematical density.
- Audience: advanced undergraduate or early graduate reader
- Scope: Integrate the Brian and Helena Chern-Simons reviews into modular TeX files under PROJECTS/QFT/253b_final_paper/tex_docs, with human-useful LLM review docs organized under PROJECTS/QFT/253b_final_paper/llm_docs/current, reference, and logs.

## Next Actions
1. Rewrite dense TeX into teacher-to-student exposition with short topic headings, explicit derivation narration, and figure flags.
2. Update `state/writing_context.yaml` with the active section goal, sources, and known risks.
3. Record notation and convention decisions before style polish.

## Quality Gates
- Outline before drafting.
- Verification before style review.
- Notation and cross-reference audit before final polish.
- Figure specification before plot or diagram generation.

## State Files
- `state/writing_pipeline.md`
- `state/writing_context.yaml`
- `state/writing/notation_registry.md`
- `state/writing/convention_registry.md`
- `state/writing/figure_inventory.md`
- `state/writing/writing_review.md`

## Warnings
- QFT is still formal-modeling heavy; writing should clarify assumptions without freezing unresolved claims.
