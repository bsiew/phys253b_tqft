# Task 8.1 --- Chapter 8 Sec. 8.1 0-Form Symmetries in Defect Language

- **Status:** done
- **Owner:** Brian
- **Duration:** 45 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Recast ordinary global symmetries as topological operators supported on codimension-1 manifolds. This is the foundation for the $q$-form generalization in Sec. 8.2.

## Content

1. Start with Noether: $\partial_\mu j^\mu = 0$ for a continuous 0-form symmetry $G$.
2. Define the charge operator $U_g(\Sigma)$ at a codimension-1 surface $\Sigma$: $U_g = \exp(i\alpha Q_\Sigma)$ where $Q_\Sigma = \int_\Sigma \star j$.
3. Current conservation = topological invariance of $U_g(\Sigma)$ under deformations of $\Sigma$ that do not cross charged operators.
4. Charged operators are 0-dimensional (local fields $\phi(x)$), and the symmetry-defect link picks up $U_g \cdot \phi(x) = g \cdot \phi(x)$.

## Acceptance criteria

- Translation from Noether language to defect language stated explicitly.
- Charged operator dimension identified: $q = 0$.
- Symmetry-operator dimension identified: codim $q+1 = 1$ (i.e., spacetime-dimension minus 1).

## References

- GKSW 2015.
- Bhardwaj et al. 2023 lectures.

## Result

- `paper/ch08_gensym.tex` now contains the Chapter 8 introduction and a full `\S8.1` draft.
- The section states the Noether-to-defect translation explicitly, defines `Q_\Sigma` and `U_g(\Sigma)`, proves deformation invariance by Stokes' theorem, and derives the crossing relation with a charged local operator.
- The $q=0$ and codimension-$1$ identifications are stated explicitly in the closing remarks and tied forward to Sec. 8.2.
