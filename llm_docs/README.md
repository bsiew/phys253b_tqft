---
created_at: "2026-05-01T23:26:05-04:00"
updated_at: "2026-05-01T23:46:07-04:00"
generated_by: "codex"
timestamp_source: "filesystem_birthtime"
---

# LLM Docs

This folder is for final-paper collaboration material generated or maintained with LLM help.

## Metadata

Generated markdown files should begin with YAML front matter:

```yaml
---
created_at: "YYYY-MM-DDTHH:MM:SS-04:00"
updated_at: "YYYY-MM-DDTHH:MM:SS-04:00"
generated_by: "codex"
timestamp_source: "agent_clock"
---
```

Use full timestamps with timezone, not date-only stamps. Preserve `created_at` when editing an existing file, update `updated_at`, and set `generated_by` to the creating agent or import source.

## Current

Use `current/` for documents needed during the active paper-migration cycle:

- `REORGANIZATION_STATUS.md`
- `content_mapping_2026-05-01.md`
- `reorganization_plan_2026-05-01.md`
- `writing_style_guide.md`
- `figure_inventory.md`
- `figure_wishlist.md`
- `next_actions.md`

The writing context, pipeline, and review files in `current/` are pointers. Their canonical copies live in `PROJECTS/QFT/state/`.

## Reference

Use `reference/` for longer-lived background and literature notes.

## Logs

Use `logs/` for session summaries, generated implementation records, imported conversation artifacts, and historical handoff notes.

Do not put fresh generated run logs directly at the top level of `llm_docs/`.
