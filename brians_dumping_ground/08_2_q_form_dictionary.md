# Task 8.2 --- Chapter 8 Sec. 8.2 $q$-Form Symmetries and Dictionary Table

- **Status:** done
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Generalize 0-form to $q$-form: charged objects are $q$-dimensional (worldlines, worldsheets), symmetry operators are codimension-$(q+1)$. Include the required dictionary table.

## Dictionary table (core paper deliverable)

| Object (charged) | Dimension | Symmetry defect | Codim of defect | Conserved current | Background field |
|---|---|---|---|---|---|
| Local operator $\phi(x)$ | 0 | $U_g(\Sigma^{d-1})$ | 1 | $J^{(1)}$ | $A^{(1)}$ |
| Wilson line $W(C)$ | 1 | $U_g(\Sigma^{d-2})$ | 2 | $J^{(2)}$ | $B^{(2)}$ |
| Surface operator $\mathcal S(\Sigma)$ | 2 | $U_g(\Sigma^{d-3})$ | 3 | $J^{(3)}$ | $C^{(3)}$ |

## Content

1. **Examples.**
   - Maxwell theory has a 1-form electric symmetry (acts on Wilson lines) and a 1-form magnetic symmetry (acts on 't Hooft lines).
   - Non-abelian gauge theory has a center symmetry as a 1-form symmetry.
2. **Conserved current for $q$-form.** $d(\star J^{(q+1)}) = 0$; the symmetry operator is $U_g(M^{d-q-1}) = \exp(i\alpha \int_{M^{d-q-1}} \star J^{(q+1)})$.
3. **Background field.** A $(q+1)$-form gauge field coupled to $\star J^{(q+1)}$.

## Acceptance criteria

- Dictionary table present, all rows filled.
- At least one worked example (center symmetry of Yang--Mills).
- Maxwell example with both electric and magnetic 1-form symmetries.

## References

- GKSW 2015.
- Bhardwaj et al. 2023 lectures.

## Result

- `paper/ch08_gensym.tex` now contains a real `\S8.2` at `sec:qform-dictionary`.
- The section defines continuous abelian $q$-form symmetries, proves the topological-invariance statement, and states the general crossing relation with charged $q$-dimensional operators.
- The required dictionary table is present as `tab:qform-dictionary`.
- Two worked examples are included: Maxwell theory with electric and magnetic 1-form symmetries, and the discrete center 1-form symmetry of pure Yang--Mills.
