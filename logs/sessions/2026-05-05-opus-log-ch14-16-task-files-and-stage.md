---
created_at: "2026-05-05T17:54:10-04:00"
updated_at: "2026-05-05T17:54:10-04:00"
generated_by: "opus"
updated_by: "opus"
timestamp_source: "agent_clock"
project: "QFT"
log_type: "generated_session"
---

## Summary

Inspected the migration plan (`llm_docs/current/migration_plan_2026-05-04.md`) against the actual `tex_docs/` and `brians_dumping_ground/` contents. Found consistency issues (stale section references in ch14/ch15 comment headers) and a major gap: no writing task files existed for the second-half chapters (Ch 14–16). Created all missing planning artifacts and linked them to the ingested literature.

## Deliverables

### New task files (9 total)

- `brians_dumping_ground/plan/tasks/ch14_1_theta_chi_u1a.md`
- `brians_dumping_ground/plan/tasks/ch14_2_eta_prime_wv.md`
- `brians_dumping_ground/plan/tasks/ch14_3_strong_cp_axion.md`
- `brians_dumping_ground/plan/tasks/ch14_4_qcd_caveats.md`
- `brians_dumping_ground/plan/tasks/ch15_1_monopoles_line_operators.md`
- `brians_dumping_ground/plan/tasks/ch15_2_when_topological.md`
- `brians_dumping_ground/plan/tasks/ch16_1_demonstrated.md`
- `brians_dumping_ground/plan/tasks/ch16_2_open_directions.md`
- `brians_dumping_ground/plan/tasks/ch16_3_guide_du_routard.md`

### New stage file

- `brians_dumping_ground/plan/stages/stage_IVb_partII_crossdisciplinary.md` — covers Ch 14–15 writing with explicit disambiguation from BSIEW integration/presentation task numbering.

### Fixes

- `tex_docs/ch14_sectors_3plus1d.tex` — updated stale comment references (Sec 6.x → Ch 14.x).
- `tex_docs/ch15_defects_synthesis.tex` — updated stale comment references (Sec 7.x / 5.x / 6.x → Ch 15.x / 11.x / 14.x).

### Literature linking

Each task file now contains a `## Literature summaries` section with relative paths to the matching `codex_paper_summary.md` files under `PROJECTS/QFT/literature/`. Key matches:

| Reference | arXiv ID |
|-----------|----------|
| Dine 2000 TASI | `hep-ph_0011376` |
| Hook 2018 TASI | `1812.02669` |
| Marsh 2016 | `1510.07633` |
| Teper 2000 | `hep-lat_9909124` |
| Cichy et al. 2015 | `1504.07954` |
| Arean et al. 2021 | `2105.00923` |
| Abel nEDM 2020 | `2001.11966` |
| ADMX Gen 2 | `1804.05750` |
| BabyIAXO | `2010.12076` |
| CASPEr | `1306.6089` |
| Borsanyi lattice | `1606.07494` |
| Rajantie 2024 | `2411.05753` |
| Fairbairn 2021 | `2005.05100` |
| GKSW 2015 | `1412.5148` |
| Kapustin–Witten 2007 | `hep-th_0604151` |
| Witten 2016 | `1510.07698` |
| Stern 2008 | `0711.4697` |
| Wen 1995 | `cond-mat_9506066` |
| FMT 2022 | `2209.07471` |
| Bhardwaj 2023 | `2307.07547` |
| Nayak 2008 | `0707.1889` |

## Consistency notes

- Migration plan and actual file tree are aligned.
- BSIEW task number collision (14_x = integration, 15_x = presentation) disambiguated with `ch14_*` / `ch15_*` / `ch16_*` prefix for the new writing tasks.
- Superseded `part2_05/06/07` files still in `tex_docs/` (quarantine deferred per migration plan §8).
- References not yet ingested into literature: 't Hooft 1976, Witten 1979, Veneziano 1979, Di Vecchia–Veneziano 1980, Dirac 1931, Polyakov 1974, Manton–Sutcliffe, Shnir, Birmingham 1991.

## Current stage

**Stage IV-b** (new): Ch 14–15 writing. Independent of the condensed-matter core (Stages IV–V). The writing order is ch14.1 → ch14.2 → ch14.3 → ch14.4 → ch15.1 → ch15.2. Ch 16 tasks are Stage VI (write last).

## Next actions

1. Begin drafting ch14.1 (theta vacua / chi_t / U(1)_A) — the narrative entry point.
2. Ingest missing literature (especially 't Hooft 1976, Witten 1979, Veneziano 1979) if PDFs are available.
3. Write Ch 11 §11.6 (Maxwell-CS) and §11.7 (honesty box) to unblock Ch 15 §15.2 dependency.
