# Task 8.3 --- Chapter 8 Sec. 8.3 Gauging Higher-Form Symmetries

- **Status:** done
- **Owner:** Brian
- **Duration:** 60 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Define what it means to gauge a $q$-form symmetry, and work out the $\mathbb{Z}_N$ 1-form example explicitly. Also explain the relation between gauging the center symmetry of $SU(N)$ Yang--Mills and the passage to $PSU(N)$ global form.

## Content

1. **Gauging recipe.** Sum over configurations of the $(q+1)$-form background field $B$ with appropriate orbit-weighted measure.
2. **Worked example: gauge electric 1-form $\mathbb{Z}_N$ in 4D Maxwell.**
   - Start with free Maxwell theory with compact $U(1)$.
   - The 1-form electric symmetry is $U(1)^{(1)}_{\text{elec}}$; it acts on Wilson lines.
   - Gauge a $\mathbb{Z}_N$ subgroup by promoting the 2-form background field $B$ to a dynamical field and summing over it.
   - Result: only Wilson lines of charge divisible by $N$ remain genuine; this is the global-form statement usually summarized as passing from $U(1)$ to $U(1)/\mathbb{Z}_N$.
3. **Yang--Mills relation.**
   - Gauging the electric center 1-form symmetry of pure $SU(N)$ Yang--Mills changes the global form to $PSU(N)=SU(N)/\mathbb{Z}_N$.
   - The discrete theta-angle caveat is stated explicitly.

## Acceptance criteria

- Gauging defined precisely.
- The Maxwell / $\mathbb{Z}_N$ example worked through in full.
- Forward-pointer to how this relates to Dijkgraaf--Witten.

## References

- GKSW 2015.
- Bhardwaj et al. 2023 lectures.
- Aharony--Seiberg--Tachikawa 2013 for the global-form caveat.

## Result

- `paper/ch08_gensym.tex` now contains a real `\S8.3` at `sec:qform-gauging`.
- The section defines gauging for finite abelian $q$-form symmetries via an orbit-weighted sum over background fields.
- The four-dimensional Maxwell example is worked through explicitly: the one-form gauge transformation is written down, and the line-operator selection rule `n \equiv 0 \pmod N` is proved.
- The relation to $SU(N)$ versus $PSU(N)$ gauge theory is stated, including the discrete theta-angle caveat.
- The earlier task wording about a dual 0-form symmetry has been corrected: in four dimensions, gauging a 1-form symmetry produces another 1-form symmetry, not a 0-form symmetry.
