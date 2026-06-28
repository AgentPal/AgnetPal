# Governance Record Example

## Purpose

This public-safe governance record shows how a real project could document
human review and reusable/private boundaries for an Org/FDE workflow.

It is a template-like example. It does not create a real project record and does
not include customer-private evidence.

## Governance Decision

```yaml
decision_id: org-fde-content-ops-accounting-advisor-governance-example
status: example_requires_human_review_before_real_use
decision: >
  The combined pack may be used as a no-code reference for a monthly content
  operations workflow with accounting-adjacent review, provided that real
  customer evidence stays in the central project record and professional
  conclusions receive qualified human review.
```

## Review Evidence

| Evidence | Status | Notes |
| --- | --- | --- |
| Combined pack metadata parses | pass | Public example metadata only. |
| Org Pack reference exists | pass | `examples/org-packs/content-ops-org-pack/` |
| FDE Pack reference exists | pass | `examples/fde-packs/accounting-advisor-fde-pack/` |
| Recommended Pals are AI judgement inputs | pass | Not a route map. |
| Customer-private evidence included | pass | No private evidence included. |
| External execution | not-run | No connector, API client, scanner, or workflow engine. |
| Professional conclusion approved | requires-human-review | Real customer use needs qualified review. |

## Reusable / Private Classification

| Asset | Classification | Target |
| --- | --- | --- |
| Generic monthly workflow shape | reusable | combined example docs |
| Context packet shell | reusable | combined example docs |
| Task package shell | reusable | combined example docs |
| Verification result shell | reusable | combined example docs |
| Real customer revenue records | customer-private | `workspace/projects/<project-id>/source-map/` or approved private store |
| Real review decision | customer-private | `workspace/projects/<project-id>/governance/` |
| Real task report | customer-private | `workspace/projects/<project-id>/reports/` |
| Credentials or system exports | excluded from public example | approved private security process only |

## Human Reviewer

```yaml
human_reviewer: <qualified reviewer role, stored in private project record>
review_date: <YYYY-MM-DD, private project record only>
review_scope:
  - accounting-adjacent language
  - revenue-record interpretation
  - month-end readiness statements
  - customer-facing professional claims
```

This public example does not name a real reviewer.

## Approval Status

Use one of:

- `approved_for_public_reusable_example`
- `approved_for_private_project_use`
- `requires-human-review`
- `blocked`
- `rejected`

For this example:

```text
approval_status: requires-human-review
```

## Rejected / Blocked Conditions

Reject or block the workflow if:

- real customer data appears in reusable example files;
- credentials, tokens, cookies, passwords, API keys, private keys, connection
  strings, or secrets appear in public files;
- a reviewer tries to convert `not-run` or `missing` into `pass`;
- the workflow claims to operate a business system automatically;
- recommended Pals are rewritten as keyword routes;
- external project `.agentpal/` is used as a thick store for Org/FDE/Pals,
  memory, reports, governance, or capability inventory.

## Central Project Record Writeback Target

For a real project, governance records belong under:

```text
workspace/projects/<project-id>/governance/
```

Related verification records may belong under:

```text
workspace/projects/<project-id>/tasks/verification-records/
workspace/projects/<project-id>/reports/verification-reports/
```

## What Cannot Be Written To The Reusable Pack

Do not write these into the reusable combined pack:

- real reviewer names tied to a private customer;
- real accounting, tax, payroll, audit, compliance, or financial records;
- real customer meeting notes or screenshots;
- private project memory;
- private governance decisions;
- credentials or secret-like values;
- connector settings or external API configuration.
