# Task Package Example

## Purpose

This public-safe task package shows how the combined pack can produce a no-code
work package for a content operations workflow with accounting-adjacent review.

It is not a Runtime command, connector workflow, or automatic execution plan.

## Task Summary

Design a monthly collaboration workflow for a content team that includes:

- content planning;
- source and draft preparation;
- revenue-record handoff notes with empty placeholders;
- monthly retrospective prompts;
- human review for accounting-adjacent statements;
- private evidence writeback target placeholders.

## Owner / Candidate Pal Judgement

Selected owner in this example: `PalSmith`

Reason: the task is about reusable Org/FDE asset governance, public-safety
classification, and workflow/governance example boundaries.

Supporting candidate perspectives:

| Pal | Candidate Contribution |
| --- | --- |
| Mira | User-facing explanation, project framing, and progress summary. |
| Morgan | Document structure, package shape, and report organization. |
| Quinn | Verification checklist and readiness review. |
| Vega | Public-source research planning if the user requests external facts. |
| Harper | Editorial clarity for content-team workflow language. |

These are AI judgement inputs only. They are not keyword routes, domain routes,
role maps, or fixed assignments.

## Context Refs

- `examples/combined-packs/content-ops-with-accounting-advisor/combined-pack.json`
- `examples/combined-packs/content-ops-with-accounting-advisor/reusable-assets-map.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/customer-private-boundary.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/thin-binding-relationship.md`
- `examples/org-packs/content-ops-org-pack/`
- `examples/fde-packs/accounting-advisor-fde-pack/`
- `workspace/projects/<project-id>/`

## Steps

1. Confirm the user goal and whether any real project evidence is needed.
2. Explain the combined pack boundary and no-code status.
3. Build a context packet from reusable Org/FDE references.
4. Identify customer-private placeholders and forbidden public content.
5. Draft the monthly workflow stages.
6. Mark accounting-adjacent outputs as `requires-human-review`.
7. Prepare a verification checklist with `pass`, `missing`, `not-run`,
   `blocked`, and `requires-human-review` states.
8. Prepare a governance record shell for approval status and writeback target.
9. Summarize what was not executed.

## Expected Outputs

- workflow summary;
- context packet;
- task package;
- governance record;
- verification result;
- private evidence request list;
- human review checklist.

## Human Review Requirements

Human review is required before using any accounting, tax, payroll, audit,
compliance, or financial reporting conclusion with a real customer.

The reviewer field may be:

```text
human_reviewer: <qualified reviewer name or role, private project record only>
```

This public example does not name a real reviewer.

## Blocked Conditions

Use `blocked` or `requires-human-review` when:

- the user asks for a final accounting conclusion without qualified review;
- customer-private evidence is needed but unavailable;
- the proposed output includes real customer data in a public reusable file;
- the task would require a connector, API client, scanner, or external system
  operation;
- the current Runtime lacks evidence for an execution claim.

## Verification Checklist

| Check | Status | Evidence |
| --- | --- | --- |
| Combined pack selected | pass | `combined-pack.json` reference only |
| Recommended Pals remain AI judgement input | pass | no route table created |
| Private evidence target is placeholder only | pass | `workspace/projects/<project-id>/` |
| Human review retained | requires-human-review | accounting-adjacent outputs |
| External execution | not-run | no connector or API call |
| Customer-private data in public example | pass | none included |

## Memory / Report Writeback Target

For a real project, write task and verification records under:

```text
workspace/projects/<project-id>/tasks/
workspace/projects/<project-id>/reports/
workspace/projects/<project-id>/governance/
```

Do not write these records into the external project `.agentpal/` directory by
default.

## No External Execution Statement

This task package does not run a workflow, call a business system, inspect a
live project, connect to accounting software, store credentials, or approve
professional conclusions.
