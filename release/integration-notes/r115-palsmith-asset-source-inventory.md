# R115 PalSmith Asset Source Inventory

Date: 2026-06-28

## Scope

Inventory for PalSmith asset manifest dry-run proposal only.

Owner Pal path resolved from central roster:

`official/pals/PalSmith-pal-governor`

## Root Entries

| Path | Exists | Proposed manifest status | Review required | Notes |
| --- | --- | --- | --- | --- |
| `pal.json` | yes | present | false | v0.5 metadata source. |
| `PAL.md` | yes | present | false | Pal identity and no-code governance boundary. |
| `README.md` | yes | present | false | Human-facing Pal overview. |
| `AGENTS.md` | yes | present | false | Runtime-facing loading and boundary instructions. |
| `SKILL.md` | yes | present | false | Pal Pack entry, not a single Agent Skill. |
| `asset-manifest.json` | no | missing | true | Official manifest is intentionally absent in R115. |

## Directory Inventory

| asset_group | path | exists | index_or_readme | file_count | status | proposed_manifest_status | review_required | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `identity` | `identity/` | yes | `README.md` | 1 | empty-with-readme | partial | true | Boundary placeholder; no deeper persona files yet. |
| `core` | `core/` | yes | none | 24 | present-needs-index | partial | true | Many protocol assets; no directory index. |
| `knowledge` | `knowledge/` | yes | `README.md` | 11 | present | present | true | Knowledge files exist and require later item-level review. |
| `research` | `research/` | yes | `README.md` | 3 | present | present | true | Contains source inventory and coverage matrix. |
| `skills` | `skills/` | yes | `README.md`, `index.md` | 18 | present | present | true | Formal skill cards and skill map exist. |
| `workflows` | `workflows/` | yes | `README.md` | 6 | present | present | true | Workflow files exist. |
| `runbooks` | `runbooks/` | yes | `README.md` | 4 | present | present | true | Runbooks exist. |
| `learning` | `learning/` | no | none | 0 | missing | missing | true | Optional gap already recorded in PalSmith compatibility metadata. |
| `memory` | `memory/` | yes | `README.md` | 1 | empty-with-readme | partial | true | Boundary-only memory directory. |
| `state` | `state/` | yes | `README.md` | 1 | empty-with-readme | partial | true | Boundary-only state directory added in R114 for clean-copy visibility. |
| `reports` | `reports/` | yes | nested READMEs | 5 | present-needs-root-index | partial | true | Nested report indexes exist; root index is absent. |
| `evals` | `evals/` | yes | `README.md` | 24 | present | present | true | Eval files exist. |
| `examples` | `examples/` | yes | `README.md` | 50 | present | present | true | Examples and task packages exist; item-level review deferred. |
| `checklists` | `checklists/` | yes | none | 3 | present-needs-index | partial | true | Checklist files exist without directory index. |
| `governance` | `governance/` | yes | none | 5 | present-needs-index | partial | true | Governance policy files exist without directory index. |
| `templates` | `templates/` | yes | `README.md` | 45 | present | present | true | Templates and task-package templates exist. |

## Public Safety Notes

- The proposed manifest must index paths and short summaries only.
- Full report bodies, full research bodies, private memory, runtime state, external project data, and private access material are excluded.
- The dry-run proposal must not become the official manifest and must not change runtime loading behavior.

## Summary

Covered groups: root entries, identity, core, knowledge, research, skills, workflows, runbooks, memory, state, reports, evals, examples, checklists, governance, templates.

Missing optional group: `learning/`.

Groups needing future index or item-level review: `identity`, `core`, `knowledge`, `research`, `skills`, `workflows`, `runbooks`, `learning`, `memory`, `state`, `reports`, `evals`, `examples`, `checklists`, `governance`, `templates`.
