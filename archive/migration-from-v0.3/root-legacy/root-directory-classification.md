# Root Directory Classification

Date: 2026-06-28

This table records R76 root directory cleanup decisions.

| Old path | Classification | New path | Action | Kept at root | Reason | Future removal candidate |
| --- | --- | --- | --- | --- | --- | --- |
| `pals/` | `archive-legacy` | `archive/migration-from-v0.3/root-legacy/pals/` | moved | no | Root `pals/` was only a compatibility pointer; official Pal Packs are under `official/pals/`. | no, already moved |
| `contacts/` | `archive-legacy` | `archive/migration-from-v0.3/root-legacy/contacts/` | moved tracked files | no | Central contacts source of truth is `workspace/organization/contacts/`. | no, already moved |
| `contacts/collaboration-memory.md` | `ignored-local-runtime` | `.agentpal/local/contacts-collaboration-memory.md` | moved locally, not tracked | no | Ignored runtime collaboration note; not public release content. | local cleanup only |
| `registry/` | `migrate-to-new-structure` | `workspace/resources/registry/` | moved | no | Registry files are resource references, not central Pal contact source. | no, already moved |
| `capabilities/` | `current-reference` | future `standards/capability-inventory/` or `workspace/organization/capability-inventory/` | kept | yes | Still referenced by current capability docs and examples. | yes |
| `core/` | `current-reference` | none | kept | yes | Runtime gates are active initialization files. | no |
| `orchestration/` | `current-reference` | future selected standards/workflows split | kept | yes | Current no-code protocol surface used by initialization and task packages. | yes |
| `projects/` | `compatibility-pointer-only` | future `templates/project-binding/`, `standards/project-binding/`, or archive | kept | yes | Some remove/register project prompts and legacy references still point here. | yes |
| `prompts/` | `current-reference` | future `templates/prompts/` for non-runtime prompt families | kept | yes | Runtime entry prompts remain active at root for compatibility. | yes |
| `imports/` | `current-reference` | future `workspace/resources/imports/` | kept | yes | Public-safe import placeholders remain tracked. | yes |
| `memory/` | `compatibility-pointer-only` | future `workspace/state/` or `workspace/projects/_template/memory/` | kept | yes | Public-safe placeholder structure only; private content ignored. | yes |
| `state/` | `compatibility-pointer-only` | `workspace/state/` | kept | yes | Only README is tracked; other state files are ignored local runtime state. | yes |
| `reports/` | `compatibility-pointer-only` | future `release/`, `evals/evidence/`, or central project records | kept | yes | Public-safe placeholder structure only; real reports are ignored/private. | yes |
| `models/` | `current-reference` | future `standards/capability-inventory/` or `workspace/resources/` | kept | yes | Model-routing notes are still referenced by docs. | yes |
| `plugins/` | `current-reference` | future `standards/capability-inventory/` or `workspace/resources/` | kept | yes | Plugin-discovery notes are still referenced by docs. | yes |
| `runtime/` | `current-reference` | future `standards/capability-inventory/` or `workspace/resources/` | kept | yes | Runtime-awareness notes are still referenced by docs. | yes |
| `response-fingerprints/` | `current-reference` | future `official/pals/<Pal>/core/` or `workspace/resources/` | kept | yes | Pal-mode validation references still use this path. | yes |
| `.agentpal/` | `ignored-local-runtime` | none | kept locally, ignored | yes | Local import/smoke/runtime staging; not public source. | local cleanup only |
| `.agents/` | `ignored-local-runtime` | none | kept locally | yes | Local agent/runtime folder; empty in this checkout. | local cleanup only |
| `.codex/` | `ignored-local-runtime` | none | kept locally | yes | Local Codex folder; empty in this checkout. | local cleanup only |
| `exports/` | `ignored-local-runtime` | none | kept locally, ignored | yes | Local generated exports; not public source. | local cleanup only |
