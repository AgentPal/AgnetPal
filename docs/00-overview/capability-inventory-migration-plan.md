# Capability Inventory Migration Plan

R78 completed the first staged split of `capabilities/`, `runtime/`, `models/`, and `plugins/`. Low-risk standard-like files moved to `standards/capability-inventory/`, example profiles moved to `examples/capability-inventory/`, and current organization placeholders moved to `workspace/organization/capability-inventory/`.

The root directories now remain as temporary compatibility pointers only.

## Current Surfaces

| current path | current role | future home |
| --- | --- | --- |
| `standards/capability-inventory/` | profile standards, policies, protocols, and matrices | active standard source |
| `examples/capability-inventory/` | illustrative runtime/model/reasoning/Skill/plugin/MCP/Pal profiles | active example source |
| `workspace/organization/capability-inventory/` | current central organization records and usage memory placeholders | active central organization record source |
| `capabilities/`, `runtime/`, `models/`, `plugins/` | temporary compatibility pointers | remove or archive when R79 proves all active references are updated |

## Target Split

- Standards: reusable schemas, profile fields, privacy rules, and judgement rules go under `standards/capability-inventory/`.
- Organization records: current organization capability inventory and public-safe central examples go under `workspace/organization/capability-inventory/`.
- Project records: project-specific capability findings go under `workspace/projects/<project-id>/capability-inventory/`.
- Examples: illustrative fake profiles go under `examples/capability-inventory/`.
- Evals and release evidence: checks stay under `evals/capability-inventory/` or `release/`.
- Archive: superseded profile notes move to `archive/migration-from-v0.3/root-legacy/`.

## Migration Rounds

1. R78: inventory all references to `capabilities/`, `runtime/`, `models/`, and `plugins/`; add compatibility pointers. Done.
2. R78: move schema-like and standard-like content into `standards/capability-inventory/`. Done for low-risk files.
3. R78: move illustrative examples into `examples/capability-inventory/` and update active references. Done for low-risk files.
4. R78: move current organization placeholders into `workspace/organization/capability-inventory/`. Done for low-risk files.
5. R79: decide whether root `capabilities/`, `runtime/`, `models/`, and `plugins/` can be archived or deleted after compatibility references are no longer needed.

## Boundaries

- Capability profiles are judgement inputs, not fixed routes.
- Do not introduce `keyword_map`, `domain_map`, `role_map`, deterministic semantic routing, or automatic runtime selection.
- Do not create scanners, validators, daemons, databases, or auto inventory sync.
