---
created_at: "2026-05-01T23:26:05-04:00"
updated_at: "2026-05-02T18:16:10-04:00"
generated_by: "codex"
timestamp_source: "filesystem_birthtime"
---

# LLM Docs

This folder is for final-paper collaboration material generated or maintained with LLM help.

## Current

Use `current/` for documents needed during the active paper-migration cycle:

- `REORGANIZATION_STATUS.md`
- `content_mapping_2026-05-01.md`
- `writing_style_guide.md`
- `figure_inventory.md`
- `next_actions.md`

The writing context, pipeline, review, figure inventory, and next-actions files
in `current/` are full copies for the nested final-paper git repository. The
project-control source of truth still lives in `PROJECTS/QFT/state/`; refresh
the git-local copies after state changes.

## Reference

Use `reference/` for longer-lived background and literature notes.

## Logs

Use `logs/` for final-paper-local copies of generated session summaries,
implementation records, imported conversation artifacts, and historical handoff
notes.

Canonical generated session logs belong first in
`PROJECTS/QFT/logs/sessions/`, then get mirrored here when they concern the
253b final paper. Use filename format:

```text
yyyy-mm-dd-model-log-brief-descriptor.md
```

The helper command is:

```bash
./research log-session --project QFT --model codex --descriptor final-paper-cleanup --body-file session.md --mirror 253b_final_paper/llm_docs/logs
```

Do not put fresh generated run logs directly at the top level of `llm_docs/`,
and do not add new nonstandard filenames to `logs/`.
