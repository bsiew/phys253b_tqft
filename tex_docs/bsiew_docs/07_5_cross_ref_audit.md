# Task 7.5 — Chapter 7 Cross-Reference Audit

- **Status:** pending
- **Owner:** Brian
- **Duration:** 15 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Verify every forward-pointer from Chapter 7 resolves, and that downstream chapters (8, 9, 10, 14) will know where to find DW material.

## Checklist

- [ ] Chapter 6 §6.2 (compact BF = $\mathbb{Z}_N$) → Chapter 7 §7.3 (DW = toric code): bidirectional `\ref`.
- [ ] Chapter 7 §7.2 ($H^3(\mathbb{Z}_N, U(1))$ computation) → Chapter 8 §8.5 (anomaly inflow): forward reference.
- [ ] Chapter 7 §7.4 (twisted DW) → Chapter 8 §8.5–8.7: forward reference.
- [ ] Chapter 9 (toric code) ← Chapter 7 §7.3: backward reference from Helena's chapter.
- [ ] Chapter 10 (anyons) ← Chapter 7 §7.1: group-cohomology framing of anyon data.
- [ ] Outlook ← Chapter 7: "classification of gapped phases beyond group cohomology".

## Acceptance criteria

- All `\ref`s compile.
- All backward-references from later chapters are listed in this task file.
