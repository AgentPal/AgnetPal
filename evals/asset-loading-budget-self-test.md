# Asset Loading Budget Self-Test

## Purpose

Verify default file budgets for Simple Pal Mode.

## Pass

- Default initialization uses the short path with `content_read_count` target 10-15.
- Deep initialization is diagnostic only and must state why the budget expanded.
- Mira initial judgement uses summary-level contacts / registry.
- Owner Pal required files stay around 4-5 files.
- Owner Pal selected assets stay around 1-3 files unless expanded with reason.
- Project files stay within a task-relevant slice.
- Memory summaries are 0-2 relevant summaries.
- Asset Loading Report separates `index_known_count` from `content_read_count`.
- Index-known paths are not reported as content-read files.

## Fail

- Any Pal silently expands to whole-workspace loading.
- Asset loading report claims files were used without evidence.
- Initialization defaults to wide loading without diagnostic reason.
- Future design material is loaded for ordinary task handling.
