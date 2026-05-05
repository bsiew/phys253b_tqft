# Plan of Attack — TQFT Review Paper

This directory is the working plan for the rest of the Physics 253b final paper. It mirrors the structure of Schwartz's sample plan of attack (`references/sample_plan_of_attack.pdf`): stages -> subsections -> granular tasks, with insight/warning callouts where needed.

## Top-level

- [plan_of_attack.tex](plan_of_attack.tex) — Master narrative plan, Schwartz-style.
- [stages/](stages/) — One summary markdown per stage.
- [tasks/](tasks/) — One detailed markdown per individual task. This is the canonical operational layer.
- [notes/](notes/) — Living notes: author split decisions, claim ledger, trim log.
- [presentation/](presentation/) — Board-script drafts, dry-run notes, and cheat-card materials.
- [revision_log.md](revision_log.md) — Record of every substantive revision round (Codex pass, Gemini pass, etc.).

## Stage map

| Stage | Scope | Summary | Days |
|---|---|---|---|
| **0** | Precondition (Chern–Simons chapter, outline v2) | [stage_0_precondition.md](stages/stage_0_precondition.md) | done |
| **I** | Scope freeze and repo skeleton | [stage_I_scope_freeze.md](stages/stage_I_scope_freeze.md) | 0.75 |
| **II** | Part I mathematical buildup A (Ch 2, 3, 4) + Ch 5 W-J bridge | [stage_II_partI_A.md](stages/stage_II_partI_A.md) | 1.5 |
| **III** | Part I mathematical buildup B (Ch 6, 7, 8) | [stage_III_partI_B.md](stages/stage_III_partI_B.md) | 1.5 |
| **IV** | Part II physical applications (Ch 9, 10, 11) | [stage_IV_partII_A.md](stages/stage_IV_partII_A.md) | 1.5 |
| **V** | Part II experiments and applications (Ch 12, 13) | [stage_V_partII_B.md](stages/stage_V_partII_B.md) | 1 |
| **VI** | Integration, polish, appendices | [stage_VI_integration.md](stages/stage_VI_integration.md) | 1 |
| **VII** | Presentation and final submission | [stage_VII_presentation.md](stages/stage_VII_presentation.md) | 0.75 |

Total: 8 scheduled days + 1 explicit buffer day for slips, trims, and emergency refactors.

## Author split

- **B** = Brian (mathematical / axiomatic side)
- **H** = Helena (physical / experimental side)
- **B+H** = joint

Complete split section-by-section is in [notes/author_split_decisions.md](notes/author_split_decisions.md).

## Through-line (repeat in abstract and outlook)

> *TQFT is the infrared language of gapped phases. We develop this through three touchstones — Frobenius 2D TQFT, Chern–Simons theory, and Dijkgraaf–Witten theory — and use them to organize generalized symmetries, anomaly inflow, topological order, and the experimental anyon program.*

The existing [paper/chern_simons_theory.tex](../paper/chern_simons_theory.tex) draft is the mathematical anchor of this through-line. The rest of the paper is built around it.

Every chapter must either reinforce the through-line or be cut.

## Editorial rules (non-negotiable)

1. **No ghost references.** If you cite `\cite[Theorem X.Y]{Source}`, open the source and confirm the theorem number before the citation survives review.
2. **No AI environments.** Never use `upshot`, `note`, `slogan`, `motivation`, `warning`, `idea`, `intuition`, `terminology` environments in the final paper. Allowed environments are those in `references/style references/hdr.tex` and `springer.tex` only.
3. **No AI-tell phrasing.** Ban list (Task 14.11): "we shall see", "in this chapter we have proved", "the key statement is", "an upshot of all this is", "it can be seen/verified/shown". Natural mathematical connectives like "observe" and "note that" are allowed when used the way Brian's style references use them.
4. **Honesty boxes are non-negotiable.** Chapters 11, 12, 13 each carry an honesty box. Do not soften.
5. **Page target:** 110–120 main + 10–15 appendix, for ~120–135 pp total.
6. **Preserve `paper/chern_simons_theory.tex`** as a standalone archival compile target. Integrate via wrapper/body architecture, not destructive stripping.
7. **No LLM-generated TikZ for complex topology.** Hand-draw and scan knots, braid traces, fusion trees. See Task 1.11.
8. **Maintain the claim ledger.** Every non-trivial mathematical claim is entered in [notes/claim_ledger.md](notes/claim_ledger.md) as it's drafted. See Task 1.12.

## Task files

Task files are named `NN_M_short_slug.md` where `NN` is the chapter number (or stage number for Stage I/VI/VII tasks) and `M` is the sub-task index.

### By stage

- **Stage I:** 1.1–1.12 (outline, skeleton, bib, preamble, figures, tables, notes/presentation scaffold, build route, figure policy, claim ledger)
- **Stage II:** 2.1–2.7 (Ch 2: forms), 3.1–3.5 (Ch 3: axiomatic), 4.1–4.5 (Ch 4: Frobenius), 5.1 (Ch 5 W-J bridge)
- **Stage III:** 6.1–6.4 (Ch 6: BF), 7.1–7.6 (Ch 7: DW), 8.1–8.9 (Ch 8: gen sym + inflow)
- **Stage IV:** 9.1–9.5 (Ch 9: top order + TEE bridge), 10.1–10.5 (Ch 10: anyons + MTC), 11.1–11.5 (Ch 11: FQH)
- **Stage V:** 12.1–12.4 (Ch 12: experiments), 13.1–13.3 (Ch 13: TQC)
- **Stage VI:** 14.1–14.11 (front matter, integration, proofread), A.1 (App A: category primer), C.1 (App C: global CS), D.1 (App D: discrete gauge), E.1 (App E: TEE)
- **Stage VII:** 15.1–15.7 (presentation + submit)

Appendix B (Frobenius full proof) was already present as Task 4.5's handoff; formal appendix task not separately duplicated.

### By priority

Every task file carries a `Priority:` field. Tags:

- **`core`** — grade-critical. Slippage puts the paper in trouble.
- **`important`** — strengthens the paper significantly (e.g., Witten–Jones bridge). First-cut candidate if schedule slips.
- **`stretch`** — nice-to-have. Cut first without regret.

Trim order if Stage III runs long (in order of execution):
1. Cut §8.8 (SymTFT paragraph only).
2. Move the bar-resolution computation of $H^3(\mathbb{Z}_N, U(1))$ from Ch 7 main text entirely to Appendix D.
3. Drop §8.7's FQH-edge inflow (Ch 11 §11.4 already covers it) and recover a half-day.
4. Cut the Witten–Jones bridge (Task 5.1) entirely and fall back on the existing CS-chapter forward-pointer.
5. Compress Ch 10 §10.3–10.4 to a single page citing `$S$-matrix for $U(1)_k$ is the discrete Fourier transform`.

## How to use this tree

1. **Start of writing session:** open the stage summary for the current stage; pick a `pending` task; read its `.md` file; begin drafting the chapter file it targets.
2. **During writing:** when a non-trivial claim is written, add a row to `notes/claim_ledger.md`. Do not defer.
3. **End of writing session:** mark the task `done` in its own file and in the stage summary.
4. **Blocked:** record the blocker in `notes/trim_log.md` and move to the next task in priority order.
5. **LLM second opinions:** each task file is self-contained. Hand `tasks/07_2_H3_ZN.md` to another model with no extra context; it should be able to sanity-check the plan for that task.

## Files Gemini / other LLMs should read first for context

- `plan/plan_of_attack.tex` (master narrative)
- `plan/README.md` (this file)
- `plan/revision_log.md` (revision history)
- `plan/stages/stage_I_scope_freeze.md` (onboarding stage)
- `paper/chern_simons_theory.tex` (the existing anchor content)
- `references/style references/hdr.tex`, `springer.tex` (style targets)
