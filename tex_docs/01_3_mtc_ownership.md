# Task 1.3 — Decide MTC Formalism Ownership in Chapter 10

- **Status:** pending
- **Owner:** Brian + Helena
- **Duration:** 15 min during Task 1.2
- **Stage:** [I](../stages/stage_I_scope_freeze.md)

## Goal

Decide, without ambiguity, who writes the modular tensor category formalism subsections §10.3 ($S$ and $T$ for $U(1)_k$) and §10.4 (CS primary labels).

## Default decision

- §10.3 (derive modular $S$ for $U(1)_k$ from the CS Hilbert space, Proposition `prop:dimU1k` in the CS chapter): **Brian**.
- §10.4 (list primary labels for $SU(N)_k$, connect to CS Wilson loops): **Brian**.
- §10.1, §10.2 (fusion/pentagon, braiding/hexagon, at review level, no formal derivation): **Helena**.
- §10.5 (the three-anyon comparison table): **joint**; Brian fills the toric code and Laughlin rows, Helena fills the Ising row and the physical-interpretation columns.

## Alternative if Helena wants more formalism

Helena writes §10.2 and §10.4; Brian writes §10.1 and §10.3. This puts the $S$-matrix derivation with Brian (where it belongs mathematically) while keeping the WZW connection with Helena (where it belongs physically).

## Inputs

- Outline v3
- `paper/chern_simons_theory.tex` Section 7 (U(1)_k on torus)

## Steps

1. Present the default and alternative to Helena.
2. Settle on one option.
3. Record in `plan/notes/author_split_decisions.md` under a "Chapter 10 split" heading.
4. Update `plan_of_attack.tex` Task 10.3 and 10.4 owner fields if different from default.

## Acceptance criteria

- Decision recorded with a rationale one sentence long.
- Both authors agree and have read the decision.

## Risks

- **Deferral.** It's tempting to say "we'll figure it out later." Don't; Stage IV is where this bites if unresolved.
