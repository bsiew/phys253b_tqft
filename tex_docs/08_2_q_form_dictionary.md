# Task 8.2 — Chapter 8 §8.2 $q$-Form Symmetries and Dictionary Table

- **Status:** pending
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Generalize 0-form to $q$-form: charged objects are $q$-dimensional (worldlines, worldsheets), symmetry operators are codimension-$(q+1)$. Include the required dictionary table.

## Dictionary table (required by outline v2)

| Object (charged) | Dimension | Symmetry defect | Codim of defect | Conserved current | Background field |
|---|---|---|---|---|---|
| Local operator $\phi(x)$ | 0 | $U_g(\Sigma^{d-1})$ | 1 | $j^{(1)}$ (1-form) | $A$ (1-form) |
| Wilson line $W(C)$ | 1 | $U_g(\Sigma^{d-2})$ | 2 | $J^{(2)}$ (2-form) | $B$ (2-form) |
| Surface operator $S(\Sigma)$ | 2 | $U_g(\Sigma^{d-3})$ | 3 | $J^{(3)}$ (3-form) | $C$ (3-form) |

## Content

1. **Examples.**
   - Maxwell theory has a 1-form electric symmetry (acts on Wilson lines) and a 1-form magnetic symmetry (acts on 't Hooft lines).
   - Non-abelian gauge theory has a center symmetry as a 1-form symmetry.
2. **Conserved current for $q$-form.** $d\star j^{(q+1)} = 0$; the symmetry operator is $U_g(M^{d-q-1}) = \exp(i\alpha \int_{M^{d-q-1}} \star j^{(q+1)})$.
3. **Background field.** A $(q+1)$-form gauge field coupled to $\star j^{(q+1)}$.

## Acceptance criteria

- Dictionary table present, all rows filled.
- At least one worked example (center symmetry of Yang–Mills).
- Maxwell example with both electric and magnetic 1-form symmetries.

## References

- GKSW 2015.
- Tong *Gauge Theory* notes on 1-form symmetry and center symmetry.
