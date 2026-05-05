# Task 1.12 — Claim Verification Ledger

- **Status:** pending
- **Priority:** important
- **Owner:** Brian
- **Duration:** 30 min (setup) + 5 min per claim as the paper is drafted
- **Stage:** [I](../stages/stage_I_scope_freeze.md)

## Goal

Single living file where every non-trivial mathematical claim in the paper is tagged with its verification status. This is the operational implementation of "you are responsible for the correctness of the results" from the professor's rubric.

## Location

`plan/notes/claim_ledger.md`

## Schema

Each row:

```
| ID | Claim | Chapter/Section | Status | Source |
|---|---|---|---|---|
| C.5.1 | $\tr(F \wedge F) = d\omega_{CS}$ | Ch 5 §3 | derived-here | Proposition 5.3.4 |
| C.5.2 | $\int_{SU(2)}\tr(\theta^3) = 24\pi^2$ | Ch 5 §5 | derived-here | Eq. 5.5.30 |
| C.5.3 | Level quantization $k \in \mathbb{Z}$ | Ch 5 §5 | derived-here ($SU(2)$ case) | Theorem 5.5.14 |
| C.5.4 | CS Wilson correlator = Jones polynomial | Ch 5 §8 | cited (Witten 1989) | bridge task 5.1 |
| C.6.1 | Compact BF level-$N$ = $\mathbb{Z}_N$ gauge theory | Ch 6 §2 | derived-here | Task 6.2 |
| C.7.1 | $H^3(\mathbb{Z}_N, U(1)) = \mathbb{Z}_N$ | Ch 7 §2 + App D | moved-to-appendix | App D.2 |
| ... | ... | ... | ... | ... |
```

## Status tags

- `derived-here`: full derivation in the paper body.
- `derived-elsewhere`: derived in another chapter or appendix with explicit cross-reference.
- `moved-to-appendix`: derivation is in an appendix because of space.
- `cited`: stated with a source citation and not re-derived.
- `cut`: considered and dropped.

## Claims to track from the start

Extract from `paper/chern_simons_theory.tex` (Chapter 5) and seed the ledger with these:
- $d\omega_{CS} = \tr(F \wedge F)$
- $F^g = g^{-1}Fg$
- $\omega_{CS}(A^g) - \omega_{CS}(A) = -\tfrac13 \tr(\theta^3) + d(\cdots)$
- Maurer–Cartan $d\theta = -\theta \wedge \theta$
- $\int_{SU(2)}\tr(\theta^3) = 24\pi^2$
- $SU(2)$ level quantization
- Abelian Wilson linking-number formula
- $\dim \mathcal{H}_{U(1),k}(T^2) = k$
- Atiyah–Segal axioms ⟹ $\dim Z(\Sigma) < \infty$

## Acceptance criteria

- `plan/notes/claim_ledger.md` exists with schema + seed entries.
- Every new chapter drafting task adds its claims to the ledger as it goes.
- Task 14.9 (math proofreading) reads down the ledger and marks each claim verified/unverified.

## Risks

- **Ledger drifts out of date.** Mitigation: updating the ledger is part of each chapter's acceptance criteria, not an optional afterthought.
