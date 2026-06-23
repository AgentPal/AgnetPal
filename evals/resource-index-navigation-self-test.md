# Resource Index Navigation Self-Test

## Purpose

Verify `RESOURCE_INDEX.md` and Pal indexes are navigation tools, not default context bundles.

## Pass

- Runtime reads `RESOURCE_INDEX.md` to choose a small target file set.
- Pal indexes explain when to read and when not to read assets.
- Reading an index does not cause all referenced files to load.
- Paths discovered through `RESOURCE_INDEX.md`, registry, or directory lists are reported as `index_known_*`.
- Only files actually opened as content are reported as `content_read_*`.

## Fail

- `RESOURCE_INDEX.md` is treated as permission to load the whole workspace.
- Pal `index.md` causes every skill, knowledge card, runbook, or workflow to load.
- Index-only paths are reported as if their content was read.
