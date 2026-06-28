# R106-D Official Pal Skills Index Issue Template

Use one entry per integration finding. Keep the issue public-safe and avoid copying private data, credentials, raw logs, full reports, raw research dumps, or customer material.

```yaml
issue_id:
affected_pal:
affected_path:
severity:
finding:
expected:
actual:
recommended_fix:
safe_to_fix_integration_round:
requires_human_review:
status:
```

## Field Guidance

| Field | Guidance |
| --- | --- |
| `issue_id` | Stable local id, for example `R106-INT-001`. |
| `affected_pal` | Pal display name or `workspace` / `integration` when not Pal-specific. |
| `affected_path` | Exact path, or `missing` if no path exists. |
| `severity` | `blocker`, `high`, `medium`, `low`, or `info`. |
| `finding` | Concise statement of the problem. |
| `expected` | What the R106-D gate or source thread required. |
| `actual` | What current evidence shows. Use `not-run` when not checked. |
| `recommended_fix` | Smallest safe repair or escalation. |
| `safe_to_fix_integration_round` | `yes`, `no`, or `unknown`. |
| `requires_human_review` | `yes`, `no`, or `unknown`. |
| `status` | `open`, `fixed`, `accepted-risk`, `not-reproducible`, or `deferred`. |

## Severity Guide

| Severity | Use When |
| --- | --- |
| `blocker` | central roster changed, `pal.json` changed, official manifest generated, credential leaked, external project asset copy happened, Agent Skill files were copied into Pal `skills/`, report bodies were copied into memory, raw research was promoted directly to knowledge, or required evidence is missing for acceptance. |
| `high` | selected Pal README / skills index is missing, wrong path was changed, or root entry / `pal.json` loadability is uncertain. |
| `medium` | wording may imply behavior change, Pal Skill / Agent Skill boundary is unclear, or R106-B/C overlap needs repair. |
| `low` | formatting, heading, or minor evidence-field issue that does not affect the gate decision. |
| `info` | observation for a future thread; no current repair required. |

## Example

```yaml
issue_id: R106-INT-001
affected_pal: Quinn
affected_path: official/pals/Quinn-quality/skills/index.md
severity: high
finding: Expected skills index is not present, and the R106-B validation does not record an equivalent file or deliberate no-write decision.
expected: R106-B either creates the approved skills index, identifies an approved equivalent, or records a no-write decision.
actual: File missing; decision evidence missing.
recommended_fix: Ask R106-B owner for validation evidence or create a scoped integration repair issue.
safe_to_fix_integration_round: unknown
requires_human_review: yes
status: open
```
