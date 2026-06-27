# R79 Root Pointer Audit

Date: 2026-06-28

Scope: root `capabilities/`, `runtime/`, `models/`, and `plugins/` compatibility pointer directories after R78.

## Summary

R79 found that all four root directories contained only tracked README pointer files. No tracked active capability inventory files, no ignored private files, and no required root facts sources remained.

After active references were updated, all four root pointer directories were moved to:

`archive/migration-from-v0.3/root-legacy/capability-inventory/root-pointers/`

## Audit Table

| root_dir | exists_before | files_before | only_readme_pointer | referenced_by_active_docs | referenced_by_archive_only | can_remove_from_root | blocker | decision |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `capabilities/` | yes | `capabilities/README.md` | yes | yes before R79; no after active reference update | yes | yes | none | archived to `root-pointers/capabilities/` |
| `runtime/` | yes | `runtime/README.md` | yes | yes before R79; no after active reference update | yes | yes | none | archived to `root-pointers/runtime/` |
| `models/` | yes | `models/README.md` | yes | yes before R79; no after active reference update | yes | yes | none | archived to `root-pointers/models/` |
| `plugins/` | yes | `plugins/README.md` | yes | yes before R79; no after active reference update | yes | yes | none | archived to `root-pointers/plugins/` |

## Active Sources After R79

- Standards: `standards/capability-inventory/`
- Current organization records: `workspace/organization/capability-inventory/`
- Examples: `examples/capability-inventory/`
- Historical migration evidence: `archive/migration-from-v0.3/root-legacy/capability-inventory/`

## Boundary

The archived pointer files are historical references only. Future development should not restore root `capabilities/`, `runtime/`, `models/`, or `plugins/` as active facts sources.
