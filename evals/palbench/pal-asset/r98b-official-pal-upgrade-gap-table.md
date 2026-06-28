# R98-B Official Pal Upgrade Gap Table

Date: 2026-06-28

Scope: gap table for the 9 official Pal Packs under `official/pals/`. This is an audit artifact only; it does not modify official Pal assets.

| pal_id | display_name | missing_root_entry | missing_asset_dirs | missing_index_files | pal_json_schema_gap | skill_vs_agent_skill_risk | workflow_runbook_memory_report_risk | recommended_fix | priority | safe_to_auto_fix_later | requires_human_review |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| mira-main | Mira | none | none | none | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | low: `SKILL.md` has Pal orientation and runtime boundary signals | high: legacy project-workgroup assets mention external `.agentpal/` project facts / memory and need central project-record reconciliation | Review Mira project-workgroup memory/binding wording; then add v0.5 metadata and manifest in later phases | high | no | yes |
| atlas-developer | Atlas | none | none | `memory/index.md` or `memory/README.md` | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | medium: implementation skills and imported skill-card references need explicit Pal Skill vs Runtime Skill classification | medium: verify imported skill cards stay knowledge/reference; reports not memory | Add memory index; review imported Skill-card placement; add v0.5 metadata later | medium | yes | yes |
| nova-product | Nova | none | none | `memory/index.md` or `memory/README.md` | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | low: Pal orientation present, but standard wording can be strengthened | low: examples vs memory templates should stay separate | Add memory index; add v0.5 metadata later | medium | yes | no |
| vega-research | Vega | none | none | `memory/index.md` or `memory/README.md` | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | low: Pal orientation present | medium: research source notes should not be promoted to durable knowledge without review | Add memory index; review research/knowledge distinction; add v0.5 metadata later | medium | yes | yes |
| quinn-quality | Quinn | none | none | `memory/index.md` or `memory/README.md` | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | low: Pal orientation present | low: eval/report distinction should stay explicit | Add memory index; add v0.5 metadata later | medium | yes | no |
| morgan-document | Morgan | none | none | `memory/index.md` or `memory/README.md` | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | low: Pal orientation present | low: privacy-sensitive document assets appear correctly scoped; keep reports out of memory | Add memory index; add v0.5 metadata later | medium | yes | no |
| harper-writing | Harper | none | none | `memory/index.md` or `memory/README.md` | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | low: Pal orientation present | low: style examples should not become private user memory | Add memory index; add v0.5 metadata later | medium | yes | no |
| rhea-system | Rhea | none | none | `memory/index.md` or `memory/README.md` | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | low: Pal orientation present | medium: runtime state examples must remain examples, not current machine state | Add memory index; review state/memory wording; add v0.5 metadata later | medium | yes | yes |
| palsmith-pal-governor | PalSmith | none | `learning/`; `memory/` | `runbooks/index.md` or `runbooks/README.md`; `memory/`; `learning/` | missing `asset_standard`; missing `asset_dirs`; missing manifest reference | low: Pal Pack governance role is explicit | high: `.agentpal/import-staging/` examples and missing memory/learning classification need v0.5 policy decision | Decide whether memory/learning are required or not-applicable; add runbooks index; review staging path wording; add v0.5 metadata later | high | no | yes |

## Cross-Pal Standard Gaps

| Gap | Affected Pals | Recommended Fix | Priority |
| --- | --- | --- | --- |
| No `asset-manifest.json` | all 9 | Generate after R101 manifest schema is approved | high |
| No `asset_standard` in `pal.json` | all 9 | Add in R100 using the R98-A Pal Asset Standard after integration | high |
| No `asset_dirs` in `pal.json` | all 9 | Add explicit directory classification in R100 | high |
| Memory index missing | Atlas, Nova, Vega, Quinn, Morgan, Harper, Rhea | Add minimal public-safe `memory/README.md` or `memory/index.md` in R99 | medium |
| Pal asset standard source integration | all 9 | R98-A standard files are present in the current worktree; integrate them before applying R100 metadata changes | high |
| Stale `.agentpal/` wording | Mira, PalSmith | Review against central `agentpal_project_record` and staging policy before edits | high |

## Auto-Fix Boundary

Safe to auto-fix later means a future single-thread repair can probably add a minimal public-safe index/README after human review of wording. It does not authorize this R98-B thread to edit official Pal assets.

Not safe to auto-fix later means the item needs a policy or content decision before any edit, especially when it touches external project boundary, manifest schema, Pal Skill vs Runtime Skill classification, or PalSmith memory/learning applicability.
