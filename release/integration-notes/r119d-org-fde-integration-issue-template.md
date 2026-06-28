# R119-D Org Pack / FDE Pack Integration Issue Template

Use one entry per integration finding. Keep the issue public-safe and avoid copying customer-private data, credentials, raw logs, full reports, raw research dumps, or business secrets.

```yaml
issue_id:
affected_thread:
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
| `issue_id` | Stable local id, for example `R119-INT-001`. |
| `affected_thread` | `R119-A`, `R119-B`, `R119-C`, `R119-D`, `R120`, or `unknown`. |
| `affected_path` | Exact path, or `missing` if no path exists. |
| `severity` | `blocker`, `high`, `medium`, `low`, or `info`. |
| `finding` | Concise statement of the problem. |
| `expected` | What the R119-D gate or source thread required. |
| `actual` | What current evidence shows. Use `not-run` when not checked. |
| `recommended_fix` | Smallest safe repair or escalation. |
| `safe_to_fix_integration_round` | `yes`, `no`, or `unknown`. |
| `requires_human_review` | `yes`, `no`, or `unknown`. |
| `status` | `open`, `fixed`, `accepted-risk`, `not-reproducible`, or `deferred`. |

## Severity Guide

| Severity | Use When |
| --- | --- |
| `blocker` | credential leak, customer-private leak, central roster change, official Pal change, keyword routing, connector, scanner, marketplace program, external project thick binding, or invalid JSON blocks acceptance. |
| `high` | required A/B/C output missing, validation missing, template/example parse failure, public/private boundary unclear, or index update notes missing. |
| `medium` | wording may imply runtime behavior, Org Pack vs Pal Pack boundary is unclear, FDE Pack scope is ambiguous, or shared entry update plan is incomplete. |
| `low` | formatting, heading, or minor evidence-field issue that does not affect the gate decision. |
| `info` | observation for a future thread; no current repair required. |

## Example

```yaml
issue_id: R119-INT-001
affected_thread: R119-C
affected_path: standards/asset-boundary/reusable-private-boundary.md
severity: high
finding: Reusable/private boundary file is missing.
expected: R119-C provides a reusable vs customer-private asset boundary record.
actual: File missing; no equivalent validation evidence found.
recommended_fix: Ask R119-C owner for evidence or create a scoped R120 repair issue.
safe_to_fix_integration_round: unknown
requires_human_review: yes
status: open
```
