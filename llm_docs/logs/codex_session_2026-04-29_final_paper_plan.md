---
created_at: "2026-04-28T20:55:47-04:00"
updated_at: "2026-05-01T23:45:36-04:00"
generated_by: "codex"
timestamp_source: "filesystem_birthtime"
---

# Codex Session Plan - 2026-04-29

## Active Target

Final-paper modular TeX outputs live in `PROJECTS/QFT/253b_final_paper/tex_docs`.

Session-generated review and planning markdown lives in `PROJECTS/QFT/253b_final_paper/llm_docs`.

## Source Reviews

- `PROJECTS/QFT/writings/brian_chern_simons_theory.tex`: mathematical and differential-geometric Chern-Simons buildup.
- `PROJECTS/QFT/writings/chern_simons_review.tex`: physically motivated review with Wilson loops, Hall response, K-matrix theory, anomaly inflow, and Maxwell-Chern-Simons contrast.

## TeX Outputs Requested

- `differential_forms_csimons_foundations.tex`: differential forms, Lie-algebra-valued forms, curvature, gauge transformations, transgression, Maurer-Cartan, Wess-Zumino form, and level quantization.
- `chern_simons_two_review_synthesis.tex`: detailed synthesis of the Brian and Helena reviews, organized by mathematical dependency and physical meaning.
- `anomalies_boundaries_topological_response.tex`: anomaly inflow, boundary modes, Hall response, quasiparticle charge/statistics, K-matrix data, and Maxwell-Chern-Simons contrast.

## Workflow Notes

- Keep original source reviews intact.
- Write paper-facing modules under `tex_docs`.
- Copy or write human-useful LLM markdown under `llm_docs`.
- Keep project-control state under `PROJECTS/QFT/state`.
- Use Claude especially for dense algebra expansion, notation audits, and adversarial convention checks; use Codex for repo integration, large-context synthesis, and modular file production.
- Use `research writing-plan --project QFT --stage expand --write` when the next pass should grow source-grounded TeX rather than summarize it.
- Use `research writing-plan --project QFT --stage pedagogical --write` when the next pass should make dense derivations read like teacher-to-student exposition.
- Compare source and output line counts before finalizing an expansion pass; large compression should be intentional and documented.
- Keep section and subsection titles short topic labels, normally 2-4 words and at most 5 words when possible.
- Flag high-value figures in TeX with `FIGURE FLAG` comments and mirror reusable candidates into `llm_docs`.
