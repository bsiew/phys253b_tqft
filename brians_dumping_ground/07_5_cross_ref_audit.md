# Task 7.5 --- Chapter 7 Cross-Reference Audit

- **Status:** done
- **Owner:** Brian
- **Duration:** 15 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Verify every forward-pointer from Chapter 7 resolves, and that downstream chapters (8, 9, 10, 14) will know where to find DW material.

## Checklist

- [x] Chapter 6 Sec. 6.2 (compact BF = $\mathbb{Z}_N$) -> Chapter 7 Sec. 7.3 (DW = toric code): bidirectional `\ref`.
- [x] Chapter 7 Sec. 7.2 ($H^3(\mathbb{Z}_N, U(1))$ computation) -> Chapter 8 Sec. 8.5 (anomaly inflow): forward reference.
- [x] Chapter 7 Sec. 7.4 (twisted DW) -> Chapter 8 Secs. 8.5--8.7: forward reference.
- [x] Chapter 9 (toric code) <- Chapter 7 Sec. 7.3: backward reference from Helena's chapter.
- [x] Chapter 10 (anyons) <- Chapter 7 Sec. 7.1: group-cohomology framing of anyon data.
- [x] Outlook <- Chapter 7: "classification of gapped phases beyond group cohomology".

## Acceptance criteria

- All `\ref`s compile.
- All backward-references from later chapters are listed in this task file.

## Audit notes

- `paper/ch06_bf.tex` now points explicitly from Sec. 6.2 to Chapter 7, especially Sec. 7.3, for the untwisted $\mathbb{Z}_2$ / toric-code reinterpretation.
- `paper/ch07_dw.tex` now ends with a roadmap remark that tells later chapters exactly which DW sections they should reuse:
  - Chapter 8: Secs. 7.2 and 7.4 for group cohomology and anomaly inflow.
  - Chapter 9: Sec. 7.3 for untwisted $\mathbb{Z}_2$ DW = toric code.
  - Chapter 10: Secs. 7.1, 7.2, and 7.4 for finite-group anyon data and twisted-vs-untwisted contrast.
  - Chapter 14: Chapter 7 as the baseline group-cohomology classification to be contrasted with beyond-group-cohomology phases.
- `paper/ch08_gensym.tex`, `paper/ch09_toporder.tex`, `paper/ch10_anyons.tex`, and `paper/ch14_outlook.tex` now each contain an explicit Chapter 7 hook so the later drafting stages know where to pull DW material from.
- The Chapter 8 pointers remain prose (`Sections 8.5--8.7`) rather than label-based `\ref`s for now, because Chapter 8 is still a placeholder and does not yet define stable subsection labels.
