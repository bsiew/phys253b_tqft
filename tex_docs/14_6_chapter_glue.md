# Task 14.6 — Chapter-to-Chapter Pedagogical Glue

- **Status:** pending
- **Owner:** Brian + Helena
- **Duration:** 60 min
- **Stage:** [VI](../stages/stage_VI_integration.md)

## Goal

Every chapter ends with 1–2 sentences pointing to the next chapter. This is the through-line made visible at every chapter boundary.

## Audit list

| Chapter | Ends with | Points to |
|---|---|---|
| 1 | "The mathematical machinery is built in Part I; the physical realizations and experiments are in Part II." | Ch 2 |
| 2 | "With the language of forms in place, we can state the Atiyah–Segal axioms of TQFT." | Ch 3 |
| 3 | "The simplest nontrivial case — two-dimensional oriented TQFTs — is entirely classified by commutative Frobenius algebras, the subject of Chapter 4." | Ch 4 |
| 4 | "In three dimensions the Schwarz-type example par excellence is Chern–Simons theory." | Ch 5 |
| 5 | Already has a pointer section; keep as is. | Ch 6, 8, 11 |
| 6 | "The abelian case compactified at level $N$ is $\mathbb{Z}_N$ gauge theory, a special case of Dijkgraaf–Witten." | Ch 7 |
| 7 | "These discrete gauge theories exhibit rich anomaly structure, which is the subject of Chapter 8." | Ch 8 |
| 8 | "Part II turns to the physical realization of this machinery in gapped phases of matter." | Ch 9 |
| 9 | "To compute anyon statistics we need modular-tensor-category data, introduced in Chapter 10." | Ch 10 |
| 10 | "The canonical physical realization is the fractional quantum Hall effect." | Ch 11 |
| 11 | "We now turn to the direct experimental observations." | Ch 12 |
| 12 | "The braiding experiments motivate a proposal for fault-tolerant quantum computation." | Ch 13 |
| 13 | "We conclude with an outlook." | Ch 14 |

## Steps

1. For each chapter, add the glue sentence(s) at the end if not present.
2. Verify each one is already implemented by the current chapter's closing paragraph or adjust.

## Acceptance criteria

- Every chapter except the last has a closing pointer.
- Pointers are specific (e.g., "Chapter 4") not vague ("later in the paper").
