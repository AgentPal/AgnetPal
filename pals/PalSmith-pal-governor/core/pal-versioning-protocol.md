# Pal Versioning Protocol

PalSmith supports lightweight version governance for Pal Packs.

## Version States

- draft
- testing
- stable
- deprecated
- archived

## Before Modification

Before L2 or L3 writes, generate either:

- a snapshot plan, or
- an actual Runtime-created snapshot after confirmation.

Suggested snapshot path:

```text
.snapshots/YYYY-MM-DD-before-<change-slug>/
```

If snapshots are not committed, keep a README or `.gitignore` rule that explains the boundary.

## Version Report

Use `templates/version-report.md`. Include current version, target version, change type, affected paths, rollback path, audit entry, and verification command.

## Rollback

Rollback is L3 if it replaces existing files. It requires strong confirmation and evidence from the Runtime.
