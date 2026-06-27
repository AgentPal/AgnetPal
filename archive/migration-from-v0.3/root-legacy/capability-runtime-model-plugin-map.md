# Capability, Runtime, Model, And Plugin Map

R77 identified these directories as high-risk active references. R78 completed the first staged migration by moving low-risk standard-like, example-like, current-organization-record, and usage-memory files into their target homes.

Detailed R78 evidence:

- `archive/migration-from-v0.3/root-legacy/capability-inventory/r78-file-reference-map.md`
- `archive/migration-from-v0.3/root-legacy/capability-inventory/r78-migration-decisions.md`

| legacy path | R78 classification | current destination | R78 action |
| --- | --- | --- | --- |
| `capabilities/README.md` | compatibility pointer | `capabilities/README.md` | kept as root pointer |
| `capabilities/*-capability-matrix.md` | standard | `standards/capability-inventory/` | moved |
| `capabilities/task-routing-matrix.md` | standard AI judgement matrix | `standards/capability-inventory/task-routing-matrix-standard.md` | moved and renamed |
| `capabilities/*-profiles/` | examples | `examples/capability-inventory/` | moved |
| `runtime/README.md` | compatibility pointer | `runtime/README.md` | kept as root pointer |
| `runtime/runtime-detection-protocol.md` | standard | `standards/capability-inventory/runtime-detection-protocol.md` | moved |
| `runtime/current-runtime.md`, `runtime/runtime-registry.md`, `runtime/runtime-refresh-log.md` | current organization record / usage memory | `workspace/organization/capability-inventory/runtimes/` | moved |
| `models/README.md` | compatibility pointer | `models/README.md` | kept as root pointer |
| `models/model-profiles.md`, `models/model-routing-policy.md`, `models/reasoning-strengths.md` | standards | `standards/capability-inventory/` | moved |
| `models/available-models.md`, `models/model-selection-memory.md` | current organization record / usage memory | `workspace/organization/capability-inventory/` | moved |
| `plugins/README.md` | compatibility pointer | `plugins/README.md` | kept as root pointer |
| `plugins/plugin-scan-protocol.md` | standard | `standards/capability-inventory/plugin-scan-protocol.md` | moved |
| `plugins/installed-skills.md`, `plugins/installed-plugins.md`, `plugins/installed-mcp.md`, `plugins/plugin-usage-memory.md` | current organization record / usage memory | `workspace/organization/capability-inventory/` | moved |

Capability files remain judgement inputs only. They must not become deterministic semantic routing tables, automatic scans, or external project binding payloads.
