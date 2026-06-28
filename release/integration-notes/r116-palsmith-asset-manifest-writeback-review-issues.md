# R116 PalSmith Asset Manifest Writeback Review Issues

Date: 2026-06-28

No blocking issues found.
Official writeback is still not performed in R116.

## Issues

| issue_id | severity | finding | affected_asset_group | expected | actual | recommended_fix | blocks_r117_writeback | status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| R116-GAP-001 | medium | Several groups still need stronger root index coverage before stable manifest claims. | `core`, `checklists`, `governance`, `reports` | Future official manifest should avoid implying unindexed groups are stable. | Candidate keeps these groups as partial / review-required. | R117 may write with review flags, or defer until reviewed indexes are added. | no | open |
| R116-GAP-002 | medium | Item-level review is incomplete for large groups. | `core`, `knowledge`, `skills`, `workflows`, `runbooks`, `evals`, `examples`, `templates` | Item-level summaries should be reviewed before claiming stable coverage. | Candidate keeps group-level summaries and review-required flags. | Run a later item-level review before removing review flags. | no | open |
| R116-GAP-003 | low | Optional learning directory is missing. | `learning` | Missing optional directories must remain explicit. | Candidate records `learning/` as missing. | Decide later whether to keep it missing or add a public-safe boundary directory. | no | open |

## Blocking Status

No blocking issue prevents advancing to an R117 official writeback pre-gate.

## Official Writeback Status

Official manifest writeback remains not performed and not approved in R116.
