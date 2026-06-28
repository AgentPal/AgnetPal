# R116 PalSmith Asset Manifest Proposal Review

Date: 2026-06-28

## Purpose

Review the R115 PalSmith asset manifest dry-run proposal and decide which proposed records are suitable for a future official manifest writeback candidate.

Reviewed proposal:

`release/integration-notes/r115-palsmith-asset-manifest-dry-run.proposed.json`

R116 does not write the official manifest.

## Review Verdict

Decision: `candidate_allowed_with_review_flags`

The R115 proposal has no public-safety blocker and can be converted into a writeback candidate under `release/integration-notes/`. It is not ready for direct official writeback without R117 pre-gate and post-writeback audit.

## Asset Group Review

| asset_group | proposed_item_count | ready_count | needs_review_count | missing_count | unsafe_count | decision | notes |
| --- | ---: | ---: | ---: | ---: | ---: | --- | --- |
| root_entries | 6 | 5 | 1 | 1 | 0 | keep_with_manifest_missing_note | Root entries are present except official `asset-manifest.json`, which remains intentionally missing in R116. |
| identity | 2 | 1 | 1 | 0 | 0 | keep_with_review_required | README can be indexed; directory is boundary-only and needs fuller identity review later. |
| core | 2 | 0 | 2 | 0 | 0 | keep_in_candidate_as_partial | Core protocol group lacks root index and needs item-level review; do not mark stable. |
| knowledge | 2 | 1 | 1 | 0 | 0 | keep_with_review_required | README can be indexed; knowledge files need item-level review before stable claims. |
| research | 2 | 0 | 2 | 0 | 0 | keep_with_review_required | Research sources can be indexed at summary level; no raw research dump or promotion claim. |
| skills | 2 | 1 | 1 | 0 | 0 | keep_with_review_required | `skills/index.md` is strong evidence; individual skill cards still need review before stable official writeback. |
| workflows | 1 | 0 | 1 | 0 | 0 | keep_with_review_required | Group-level workflow entry is acceptable as partial. |
| runbooks | 1 | 0 | 1 | 0 | 0 | keep_with_review_required | Group-level runbook entry is acceptable as partial. |
| learning | 1 | 0 | 1 | 1 | 0 | keep_missing_optional | Optional directory remains missing; candidate must preserve it honestly. |
| memory | 1 | 1 | 0 | 0 | 0 | keep_boundary_only | README boundary is safe; no private memory content is indexed. |
| state | 1 | 1 | 0 | 0 | 0 | keep_boundary_only | README boundary is safe; no runtime state content is indexed. |
| reports | 1 | 0 | 1 | 0 | 0 | keep_in_candidate_as_partial | Nested README coverage exists, but root report index is missing. |
| evals | 1 | 0 | 1 | 0 | 0 | keep_with_review_required | Group-level eval entry is acceptable; item-level review remains open. |
| examples | 1 | 0 | 1 | 0 | 0 | keep_with_review_required | Group-level examples entry is acceptable; do not overclaim example quality. |
| checklists | 1 | 0 | 1 | 0 | 0 | keep_in_candidate_as_partial | Checklist files exist but no directory index exists. |
| governance | 1 | 0 | 1 | 0 | 0 | keep_in_candidate_as_partial | Governance policy files exist but no directory index exists. |
| templates | 1 | 0 | 1 | 0 | 0 | keep_with_review_required | Group-level template entry is acceptable; item-level review remains open. |

## Writeback Readiness Classification

| Classification | Asset groups |
| --- | --- |
| ready_for_official_manifest | root entry records for present root files, `identity/README.md`, `knowledge/README.md`, `skills/index.md`, `memory/README.md`, `state/README.md` |
| keep_in_candidate_with_review_flags | core, knowledge group, research, skills group, workflows, runbooks, reports, evals, examples, checklists, governance, templates |
| missing_source | `asset-manifest.json` official file, optional `learning/` |
| unsafe_to_write | none found |

## Review Notes

- The candidate must not include raw file bodies, full report bodies, raw research dumps, private data, private access material, deterministic routes, runtime execution instructions, external API instructions, or copied external project assets.
- The candidate may preserve group-level entries with `review_required: true`.
- Any future official writeback must run a separate R117 pre-gate, write only the PalSmith official manifest, and run post-writeback audit plus selected R95 gates.
