# Task 9.2 — Chapter 9 §9.2 Toric Code and the 4-Fold Torus GSD

- **Status:** pending
- **Owner:** Helena
- **Duration:** 2 hours
- **Stage:** [IV](../stages/stage_IV_partII_A.md)

## Goal

Define the toric code Hamiltonian on a square lattice on the torus, identify its ground states explicitly, and derive the 4-fold ground-state degeneracy.

## Content

1. **Lattice.** Put qubits on edges of a square lattice on $T^2$.
2. **Hamiltonian.** $H = -J_v \sum_v A_v - J_p \sum_p B_p$, where:
   - $A_v = \prod_{e \in v} X_e$ (star operator on vertex $v$, product of Pauli-X on the four edges meeting $v$).
   - $B_p = \prod_{e \in p} Z_e$ (plaquette operator on $p$, product of Pauli-Z on the four edges bounding $p$).
3. **Commutation.** $[A_v, B_p] = 0$ for all $v, p$ (verify: any $A_v$ and $B_p$ share either 0 or 2 edges).
4. **Ground-state condition.** $A_v |\psi\rangle = B_p |\psi\rangle = |\psi\rangle$ for all $v, p$.
5. **Constraints.** $\prod_v A_v = \prod_p B_p = 1$, so only $V-1$ independent $A_v$ and $P-1$ independent $B_p$; total constraint count is $V + P - 2$. For a torus lattice with $E$ edges, $V + P = E$, so the constraint count is $E - 2$, and the ground-state manifold has dimension $2^{E - (E-2)} = 4$.
6. **String operators.** $W_1 = \prod Z_e$ along a non-contractible loop in one direction, $W_2$ in the other. These commute with all $A_v, B_p$, anticommute with each other's duals, and distinguish the 4 ground states.

## Acceptance criteria

- $[A_v, B_p] = 0$ proved by edge count.
- Constraint count derived explicitly.
- String operator algebra worked out.
- Forward-pointer to Chapter 6 (BF theory) and Chapter 7 (DW).

## References

- Kitaev 2003.
