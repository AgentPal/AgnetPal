# R115 PalSmith Asset Manifest Source Map

Date: 2026-06-28

## Purpose

Map each proposed dry-run manifest field to current PalSmith source evidence.

## Source Map

| Manifest field | Source path | Source type | Confidence | Safe summary | Missing / needs review | Included in dry-run | Reason |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `schema` | `standards/schemas/pal-asset-manifest.schema.json` | schema | high | v0.5 manifest schema id. | no | yes | Required manifest metadata. |
| `manifest_type` | R115 objective | task boundary | high | Marks file as dry-run proposal. | no | yes | Prevents official writeback confusion. |
| `official_writeback` | R115 objective | task boundary | high | Official writeback disallowed. | no | yes | Required safety flag. |
| `pal_id` | `workspace/organization/contacts/pals.json`; PalSmith `pal.json` | roster and metadata | high | `palsmith-pal-governor`. | no | yes | Stable owner id. |
| `pal_path` | central roster `pack_path` | roster | high | PalSmith official Pal path. | no | yes | Source path reference. |
| `source_pal_json` | `official/pals/PalSmith-pal-governor/pal.json` | metadata | high | v0.5 Pal metadata source. | no | yes | Manifest proposal derives from current metadata. |
| `asset_standard` | PalSmith `pal.json`; v0.5 standard | metadata and standard | high | `agentpal-pal-asset-standard.v0.5`. | no | yes | Required standard reference. |
| `generated_from` | R115 evidence files | dry-run evidence | high | Manual dry-run from source inventory and source map. | no | yes | No automatic inventory claim. |
| `root_entries` | PalSmith root files | filesystem evidence | high | Root entries exist except official manifest. | official manifest missing by design | yes | Root loading evidence. |
| `assets.identity` | `identity/README.md` | directory boundary | medium | Identity directory boundary only. | needs fuller identity review | yes | Directory exists with README only. |
| `assets.core` | `core/` files | protocol directory | medium | Core protocols exist without root index. | needs index and item review | yes | Group-level record only. |
| `assets.knowledge` | `knowledge/README.md` and knowledge files | directory index and assets | medium | Knowledge files exist. | needs item review | yes | Group-level and README record. |
| `assets.research` | `research/README.md`, source inventory, coverage matrix | research index | medium | Research source context exists. | needs promotion review before stable knowledge claims | yes | Group-level record. |
| `assets.skills` | `skills/index.md`, `skills/README.md`, skill map | skill index | high | Pal-owned skill cards are indexed. | item review still needed before official manifest writeback | yes | Strongest asset index source. |
| `assets.workflows` | `workflows/README.md` and workflow files | workflow directory | medium | Workflow files exist. | needs item review | yes | Group-level record. |
| `assets.runbooks` | `runbooks/README.md` and runbook files | runbook directory | medium | Runbook files exist. | needs item review | yes | Group-level record. |
| `assets.learning` | no directory | missing optional group | high | Optional learning area absent. | missing optional | yes | Record honestly as missing. |
| `assets.memory` | `memory/README.md` | boundary index | high | Memory boundary exists only. | no public memory items beyond README | yes | Prevents overclaiming memory content. |
| `assets.state` | `state/README.md` | boundary index | high | State boundary exists only. | no runtime state content | yes | Clean-copy placeholder and boundary. |
| `assets.reports` | `reports/*/README.md` | nested report indexes | medium | Report subdirectories have README files. | root report index absent | yes | Group-level partial record. |
| `assets.evals` | `evals/README.md` and eval files | eval directory | medium | Eval files exist. | needs item review | yes | Group-level record. |
| `assets.examples` | `examples/README.md` and examples | example directory | medium | Examples and task packages exist. | needs item review | yes | Group-level record. |
| `assets.checklists` | `checklists/` | checklist directory | medium | Checklist files exist. | needs index | yes | Group-level partial record. |
| `assets.governance` | `governance/` | governance directory | medium | Governance files exist. | needs index | yes | Group-level partial record. |
| `assets.templates` | `templates/README.md` and templates | template directory | medium | Templates exist. | needs item review | yes | Group-level record. |
| `public_safety` | PalSmith `pal.json`; PalSmith root boundaries | metadata and root docs | high | No private access material, route maps, or external-project write default. | no | yes | Required dry-run boundary. |
| `skill_boundary` | `skills/index.md`; PalSmith `pal.json` | skill index and metadata | high | Pal Skills are role-level; Agent Skills are references only. | no | yes | Required safety boundary. |
| `runtime_boundary` | `PAL.md`; `AGENTS.md`; `SKILL.md` | root entries | high | PalSmith produces plans and packages; host runtime executes only with evidence. | no | yes | Prevents behavior expansion. |
| `known_gaps` | source inventory | inventory evidence | high | Missing optional learning dir, no official manifest, several groups need index/item review. | yes | yes | Honest gap reporting. |
| `review` | R115 objective and source inventory | review state | high | Human review required before official writeback. | yes | yes | Dry-run not ready for direct official writeback. |

## Inclusion Rule

The proposed manifest includes only path-level and summary-level records. It does not include raw file contents, full reports, full research, private data, private access material, route maps, external project absolute paths, or runtime execution instructions.
