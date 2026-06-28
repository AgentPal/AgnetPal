# R115 PalSmith Asset Manifest Coverage Gap Report

Date: 2026-06-28

## Scope

Coverage and gap report for the PalSmith asset manifest dry-run proposal:

`release/integration-notes/r115-palsmith-asset-manifest-dry-run.proposed.json`

This report does not approve official manifest writeback.

## Covered Asset Groups

| Group | Coverage status | Evidence |
| --- | --- | --- |
| root entries | covered | `pal.json`, `PAL.md`, `README.md`, `AGENTS.md`, `SKILL.md` present |
| identity | partial | `identity/README.md` present |
| core | partial | 24 core files present; root index missing |
| knowledge | covered for group-level proposal | `knowledge/README.md` and knowledge files present |
| research | covered for group-level proposal | `research/README.md`, source inventory, coverage matrix present |
| skills | covered for group-level proposal | `skills/index.md`, `skills/README.md`, skill map, skill cards present |
| workflows | covered for group-level proposal | `workflows/README.md` and workflow files present |
| runbooks | covered for group-level proposal | `runbooks/README.md` and runbooks present |
| memory | partial | boundary README only |
| state | partial | boundary README only |
| reports | partial | nested READMEs present; root index missing |
| evals | covered for group-level proposal | `evals/README.md` and eval files present |
| examples | covered for group-level proposal | `examples/README.md`, examples, blueprints, quickstarts, task packages present |
| checklists | partial | checklist files present; root index missing |
| governance | partial | governance files present; root index missing |
| templates | covered for group-level proposal | `templates/README.md` and templates present |

## Missing Asset Groups

| Group | Status | Impact |
| --- | --- | --- |
| `learning/` | missing optional | Not a blocker for dry-run; must remain a known gap before official writeback. |

## Empty-with-README Groups

| Group | Status | Impact |
| --- | --- | --- |
| `identity/` | boundary only | Needs fuller identity review before official manifest writeback. |
| `memory/` | boundary only | Correct public-safety posture; no private memory is indexed. |
| `state/` | boundary only | Correct public-safety posture; no runtime state is indexed. |

## No-index Groups

| Group | Status | Recommended fix |
| --- | --- | --- |
| `core/` | present without root index | Add a reviewed core README or index in a separate allowed round. |
| `checklists/` | present without root index | Add a reviewed checklist README or index in a separate allowed round. |
| `governance/` | present without root index | Add a reviewed governance README or index in a separate allowed round. |
| `reports/` | nested indexes only | Add a reviewed reports root README or index in a separate allowed round. |

## Human-review Groups

Human review remains required for:

- item-level summaries for core protocols;
- knowledge files;
- Pal Skill cards;
- workflow files;
- runbooks;
- evals;
- examples;
- templates;
- report indexes;
- whether optional `learning/` should remain missing or be introduced later.

## Safe For Future Official Writeback

Safe for future official manifest writeback: `no`

Reason: the dry-run proposal parses and has no blocking public-safety issue, but several groups still need index coverage and item-level human review before writing an official manifest.

## Blockers

No blockers for the dry-run proposal.

Current blockers for immediate official writeback:

- item-level review not complete;
- `learning/` optional gap unresolved;
- several present groups need stronger root index coverage;
- official writeback has not passed a dedicated approval gate.

## Recommended Fixes

1. Keep R115 as proposal-only.
2. Use R116 as an official writeback review / approval gate, not automatic writeback.
3. Before real writeback, consider adding reviewed indexes for `core/`, `checklists/`, `governance/`, and `reports/`.
4. Review whether to keep `learning/` as optional missing or create a public-safe learning boundary in a separate allowed round.
