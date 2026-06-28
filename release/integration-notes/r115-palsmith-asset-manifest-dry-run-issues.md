# R115 PalSmith Asset Manifest Dry-run Issues

Date: 2026-06-28

No blocking issues found.
Official manifest writeback is still not performed.

## Issues

| issue_id | severity | finding | affected_path | expected | actual | recommended_fix | blocks_official_writeback | status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| R115-GAP-001 | medium | Several present asset groups need stronger root index coverage before official writeback. | `core/`, `checklists/`, `governance/`, `reports/` | Official manifest entries should have reviewed source indexes or item-level summaries. | Dry-run can record group-level partial coverage, but official writeback should not overclaim. | Add reviewed indexes or complete item-level review in a later allowed round. | yes | open |
| R115-GAP-002 | low | Optional learning directory is missing. | `learning/` | Missing optional directory should be explicit. | Missing and recorded as optional gap. | Decide in a later round whether to keep optional missing or add a public-safe boundary directory. | no | open |
| R115-GAP-003 | medium | Item-level human review is not complete for large groups. | `examples/`, `templates/`, `evals/`, `core/`, `knowledge/`, `skills/`, `workflows/` | Official manifest should not imply unreviewed item summaries are stable. | Dry-run records group-level summaries and review-required flags. | Complete item-level review before official writeback. | yes | open |

## Blocking Status

No blocking issue prevents the dry-run proposal.

## Official Writeback Status

Official manifest writeback remains not performed and not approved in R115.
