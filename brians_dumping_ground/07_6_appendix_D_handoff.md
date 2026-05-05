# Task 7.6 - Appendix D Handoff for Discrete Gauge Theory

- **Status:** done
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Decide explicitly which discrete-gauge calculations stay in the Chapter 6-7 main text and which are deferred to Appendix D.

## Scope split

Main text should keep:

1. The conceptual BF <-> `\mathbb{Z}_N` bridge.
2. One concrete `H^3(\mathbb{Z}_N,U(1))` representative and the classification statement.
3. The toric-code / untwisted `\mathbb{Z}_2` round-trip.

Appendix D should absorb:

1. The longest bar-resolution bookkeeping.
2. Secondary checks that do not change the narrative.
3. Any overflow from the BF discrete-gauge equivalence derivation.

## Acceptance criteria

- Appendix D has a clear job description before Stage VI.
- Chapter 7 does not bloat because the appendix boundary was never stated.

## Result

- `paper/appD_bf_zn.tex` now has a real scope statement and three explicit sections:
  - `sec:appD-bf-lattice` for the full compact-BF lattice derivation,
  - `sec:appD-bar-resolution` for the chain-level $H^3(B\mathbb{Z}_N,U(1))$ proof,
  - `sec:appD-secondary` for overflow checks and convention comparisons.
- Chapter 6 now points directly to Appendix D, especially `sec:appD-bf-lattice`, from the `rem:bf-zn-scope` remark.
- Chapter 7 now points directly to Appendix D, especially `sec:appD-bar-resolution`, at every place where the main text defers the generator proof or longer bar-resolution bookkeeping.
- The appendix placeholder now matches Stage VI Task `AD.1` rather than the stale generic `Task D.1` wording.
