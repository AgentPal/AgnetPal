# Verification Result Example

## Purpose

This public-safe verification result shows how to record evidence for the
workflow/governance example without turning missing or unreviewed evidence into
a pass.

It is not an automatic validator and does not run checks against customer
systems.

## Verification Result

| Checklist Item | Status | Evidence | Missing Evidence | Human Review Required |
| --- | --- | --- | --- | --- |
| Workflow usage example exists | pass | `workflow-usage-example.md` | none | no |
| Context packet example exists | pass | `context-packet.example.md` | none | no |
| Task package example exists | pass | `task-package.example.md` | none | no |
| Governance record example exists | pass | `governance-record.example.md` | none | no |
| Verification result example exists | pass | `verification-result.example.md` | none | no |
| Combined pack metadata parses | not-run | example record does not run parser | local validation result | no |
| Recommended Pals remain AI judgement input | pass | example text says recommendations are not routes | none | no |
| Customer-private evidence excluded | pass | placeholders only | real project review if adapted | yes for real customer use |
| Credentials excluded | pass | no credential values included | real project secret scan if adapted | yes for real customer use |
| External execution | not-run | no connector, API client, scanner, validator, or workflow engine used | runtime evidence if a future task executes | yes before real execution |
| Accounting-adjacent conclusion | requires-human-review | FDE boundary requires qualified review | reviewer sign-off in private record | yes |

## Status Semantics

- `pass`: current evidence directly supports the checklist item.
- `fail`: current evidence contradicts the checklist item.
- `missing`: required evidence is absent.
- `not-run`: the check was not executed.
- `blocked`: progress cannot continue without required input or approval.
- `requires-human-review`: qualified review is required before real customer use.

`not-run` is not a pass. `missing` is not a pass. `requires-human-review` is not
automatic approval.

## No Automatic Professional Decision

This example does not approve accounting, tax, payroll, audit, compliance, or
financial reporting conclusions. It records the need for qualified human review
and the private location where real evidence would be reviewed.

## Public-safe Evidence Boundary

The public example may keep:

- file existence evidence;
- generic workflow notes;
- generic checklist states;
- placeholder project-record paths.

The public example must not keep:

- real customer data;
- real financial records;
- private reviewer identities tied to customers;
- credentials or secret-like values;
- external system logs;
- connector configuration;
- screenshots or exports from private systems.
