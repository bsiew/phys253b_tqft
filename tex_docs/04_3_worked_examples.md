# Task 4.3 — Chapter 4 §4.3 Worked Examples: Group Algebras Foreshadowing DW

- **Status:** pending
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Exhibit commutative Frobenius algebras concretely and show one that foreshadows Dijkgraaf–Witten theory in Chapter 7.

## Examples

### Example 1: $V = \mathbb{C}[x]/(x^n - 1)$

- Multiplication is polynomial multiplication mod $x^n - 1$.
- Trace $\epsilon(x^k) = \delta_{k,0}$.
- Commutative, associative, unital, nondegenerate pairing.
- This computes $Z(\Sigma_g)$ for the 2D Dijkgraaf–Witten theory with gauge group $\mathbb{Z}_n$ and trivial cocycle.

### Example 2: $V = Z(G)$, the center of the group algebra of a finite group $G$

- Elements: class functions on $G$.
- Multiplication: convolution.
- Trace: evaluation at identity.
- This computes $Z(\Sigma_g)$ for 2D Dijkgraaf–Witten theory with gauge group $G$ and trivial cocycle.
- Bridges to Chapter 7 where 3D Dijkgraaf–Witten appears.

## Steps

1. Verify both examples satisfy the Frobenius axioms explicitly.
2. Compute $Z(\Sigma_1)$ (torus) in both: the torus partition function equals $|G|$ for Example 2 and $n$ for Example 1.
3. Foreshadow Chapter 7: "the 3D version replaces class functions on $G$ with cocycles in $H^3(G, U(1))$."

## Acceptance criteria

- Both examples worked out with verification of axioms.
- Torus partition function computed.
- Forward-pointer to Chapter 7.
