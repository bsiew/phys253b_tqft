# Task 3.3 — Chapter 3 §3.3 Worked Gluing Example

- **Status:** done
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [II](../stages/stage_II_partI_A.md)

## Goal

Work through one gluing example explicitly. This is one of the paper's core pedagogical deliverables because it is the first place the Atiyah-Segal axioms become concrete.

## Recommended example

**Two disks glued along their boundaries to form a sphere.**

- Disk $D^2$ with boundary $S^1$: a morphism $\emptyset \to S^1$, giving a vector $Z(D^2) \in Z(S^1)$.
- Upside-down disk $\bar D^2$: a morphism $S^1 \to \emptyset$, giving a dual vector $Z(\bar D^2) \in Z(S^1)^*$.
- Gluing: $Z(S^2) = Z(\bar D^2) \circ Z(D^2) = \langle Z(\bar D^2), Z(D^2)\rangle$.
- In 2D TQFT (foreshadowing Ch 4), $Z(D^2) = 1 \in V$ (the unit of the Frobenius algebra) and $Z(\bar D^2) = \epsilon \in V^*$ (the trace), so $Z(S^2) = \epsilon(1)$.

## Content outline

1. Draw the two disks and the sphere.
2. Identify which Atiyah–Segal axioms are used: monoidality + functoriality.
3. Compute $Z(S^2)$ in the simple Frobenius-algebra example and relate to the partition function.

## Acceptance criteria

- Pictures present.
- Computation shown step by step.
- The result is framed as a preview of Chapter 4.

## Risks

- **Overlap with Chapter 4.** Don't prove Frobenius classification here; just the gluing computation on a sphere.
