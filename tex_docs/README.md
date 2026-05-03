# Plan of Attack — TQFT Review Paper

This directory is the working plan for the rest of the Physics 253b final paper. It mirrors the structure of Schwartz's sample plan of attack (`references/sample_plan_of_attack.pdf`): stages → subsections → granular tasks, with insight/warning callouts where needed.

## Top-level

- [plan_of_attack.tex](plan_of_attack.tex) — Master plan, Schwartz-style, compiles to ~15 pages.
- [stages/](stages/) — One summary markdown per stage.
- [tasks/](tasks/) — One detailed markdown per individual task.
- [notes/](notes/) — Living notes, decisions, risk log (created as we go).

## Stage map

| Stage | Scope | Summary | Days |
|---|---|---|---|
| **0** | Precondition (Chern–Simons chapter, outline v2) | [stage_0_precondition.md](stages/stage_0_precondition.md) | done |
| **I** | Scope freeze and repo skeleton | [stage_I_scope_freeze.md](stages/stage_I_scope_freeze.md) | 0.5 |
| **II** | Part I mathematical buildup A (Ch 2, 3, 4) | [stage_II_partI_A.md](stages/stage_II_partI_A.md) | 2 |
| **III** | Part I mathematical buildup B (Ch 6, 7, 8) | [stage_III_partI_B.md](stages/stage_III_partI_B.md) | 2 |
| **IV** | Part II physical applications (Ch 9, 10, 11) | [stage_IV_partII_A.md](stages/stage_IV_partII_A.md) | 2 |
| **V** | Part II experiments and applications (Ch 12, 13) | [stage_V_partII_B.md](stages/stage_V_partII_B.md) | 1.5 |
| **VI** | Integration and polish | [stage_VI_integration.md](stages/stage_VI_integration.md) | 1 |
| **VII** | Presentation and final submission | [stage_VII_presentation.md](stages/stage_VII_presentation.md) | 1 |

## Author split

- **B** = Brian (mathematical / axiomatic side)
- **H** = Helena (physical / experimental side)
- **B+H** = joint

The complete split, section by section, is in [notes/author_split_decisions.md](notes/author_split_decisions.md) once committed.

## Through-line (repeat in abstract and outlook)

> *TQFT is the infrared language of gapped phases. We demonstrate this on three touchstones — Frobenius 2D TQFT, Chern–Simons theory, and Dijkgraaf–Witten theory — and use them to motivate generalized symmetries, anomaly inflow, and the experimental anyon program.*

Every chapter must either reinforce this through-line or be cut.

## Editorial rules (non-negotiable)

1. No ghost references. If you cite `\cite[Theorem X.Y]{Source}`, open the source and confirm the theorem number before the citation survives review.
2. No `upshot`, `note`, `slogan`, `motivation` environments in the final paper; match the allowed environments in `references/style references/hdr.tex` and `references/style references/springer.tex`.
3. No AI-tell phrasing: "we shall see", "in this chapter we have proved", "the key statement is", "an upshot of all this is". Run Task 14.11 to purge.
4. Honesty boxes in Chapters 12 and 13 are required by the outline and the course rubric. No softening them.
5. Total main-text target: 75–100 pages. Appendix: 15–25 pages. If over budget, cut before submit.

## Task files

Task files are named `NN_M_short_slug.md` where `NN` is the stage number (I–VII) and `M` is the within-stage task number matching the master plan.

- [Stage I tasks →](tasks/) (1.1 – 1.9)
- [Stage II tasks →](tasks/) (2.1 – 2.7, 3.1 – 3.5, 4.1 – 4.5)
- [Stage III tasks →](tasks/) (6.1 – 6.4, 7.1 – 7.5, 8.1 – 8.9)
- [Stage IV tasks →](tasks/) (9.1 – 9.4, 10.1 – 10.5, 11.1 – 11.5)
- [Stage V tasks →](tasks/) (12.1 – 12.4, 13.1 – 13.3)
- [Stage VI tasks →](tasks/) (14.1 – 14.11)
- [Stage VII tasks →](tasks/) (15.1 – 15.7)

## How to use this tree

- When you pick up a writing session, open the relevant stage summary, scan its status, and open the task file for whatever is `pending` or `in_progress`.
- When a task is done, mark it `done` in its markdown and update the stage summary's status table.
- When a decision gets made that affects scope (e.g., cutting SymTFT, changing the author split), record it in `notes/` and update the master `plan_of_attack.tex` if it's a structural change.
- This tree is designed to survive being fed to other LLMs for second opinions. The task files are self-contained: each one states its goal, dependencies, acceptance criteria, and the risk it addresses. Handing `tasks/08_5_anomaly_inflow_general.md` to GPT-4 for sanity-checking is meant to work without any other context.
