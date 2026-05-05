# Task 13.2 — Chapter 13 §13.2 Ising Anyon Braiding as Gate

- **Status:** pending
- **Owner:** Helena
- **Duration:** 90 min
- **Stage:** [V](../stages/stage_V_partII_B.md)

## Goal

Work through the Ising-anyon system as a concrete example: four $\sigma$-anyons give a 2-qubit space; braiding implements a specific subset of 2-qubit gates; supplement with a non-topological gate to achieve universal quantum computation.

## Content

1. **Ising fusion.** $\sigma \times \sigma = 1 + \psi$, so 4 $\sigma$'s fuse to 4-dim space = 2 qubits.
2. **Braiding group.** Exchanges of adjacent $\sigma$'s generate a representation of the braid group $B_4$ on the 2-qubit space.
3. **Gates implemented.** The generated gate set is the Clifford group — powerful but not universal.
4. **Need for additional resources.** Topologically-protected Clifford + a non-topological T gate gives universality. Fault-tolerance comes from magic-state distillation.

## Acceptance criteria

- 4-anyon = 2-qubit correspondence derived.
- Specific $R$-matrix entries for $\sigma \sigma$ braiding written.
- Clarification of what braiding alone achieves vs. what additional resources are needed.

## References

- Nayak et al RMP 2008.
