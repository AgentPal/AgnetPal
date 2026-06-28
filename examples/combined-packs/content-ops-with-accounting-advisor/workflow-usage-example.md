# Workflow Usage Example

## Purpose

This public-safe example shows how the Content Ops with Accounting Advisor
Combined Pack can shape a no-code workflow for a content team that wants a
repeatable content plan, revenue-record review rhythm, and monthly retrospective
structure.

This example does not execute work, call APIs, connect to accounting systems,
install tools, scan files, validate live systems automatically, publish a
marketplace entry, store credentials, or route by keyword.

## Example User Request

```text
We run a content team. Help us design a monthly workflow that combines content
planning, revenue-record handoff notes, and a monthly review so our editor,
operations lead, and accounting reviewer can stay aligned.
```

This request is fictional and generic. It does not name a real customer, real
account, real amount, real contract, real invoice, real platform account, or
private project path.

## Mira Explanation

Mira may explain the combined pack like this:

```text
Mira: This request can use the Content Ops with Accounting Advisor Combined
Pack as a no-code reference. The Org Pack gives reusable content operations
structure. The FDE Pack gives accounting-adjacent review boundaries and human
review expectations. The pack does not execute systems or decide Pals by
keyword.
```

Mira may identify candidate Pal perspectives from the combined pack, central
roster, project context, user intent, risk, and expected output. Those
perspectives are AI judgement inputs only.

## Candidate Pal Judgement Input

| Candidate | Why The Current AI May Consider Them |
| --- | --- |
| Mira | Explain the workflow, maintain project framing, and summarize progress. |
| PalSmith | Review reusable/private classification and combined-pack governance. |
| Morgan | Shape the context packet, task package, and final workflow document. |
| Quinn | Review verification states, missing evidence, and acceptance criteria. |
| Vega | Plan public-source research only if the user requests external facts. |
| Harper | Improve wording, editorial rhythm, and content-team language. |

These rows are not a route map. The current AI must still judge ownership
case-by-case. `/pal Name` remains an explicit user mention, not a keyword match.

Forbidden routing shape:

```text
content -> Harper
accounting -> accounting advisor
review -> Quinn
```

## PalSmith Review

PalSmith may review the proposed workflow as asset governance:

- confirm the workflow is public-safe and generic;
- confirm `combined-pack.json` is still the selected metadata source;
- confirm Org Pack and FDE Pack references remain references, not copied
  private adaptations;
- confirm recommended Pals are AI judgement inputs only;
- confirm human review remains required for accounting, tax, payroll, audit,
  compliance, and financial reporting outputs;
- produce issue notes, classification notes, or approval checklist items.

PalSmith must not automatically approve high-risk professional conclusions,
modify central contacts, write external project files, call external systems, or
publish reusable assets.

## Org Pack Context

The Org Pack reference is:

```text
examples/org-packs/content-ops-org-pack/
```

Reusable Org context for this example:

- intake rhythm for monthly content planning;
- source-pack preparation for content ideas and source material;
- draft review and publishing readiness checkpoints;
- learning review notes after publication;
- private-boundary reminders for real content, campaign, customer, and project
  evidence.

The Org Pack does not publish content, assign Pals by keyword, or store private
project facts.

## FDE Pack Context

The FDE Pack reference is:

```text
examples/fde-packs/accounting-advisor-fde-pack/
```

Reusable FDE context for this example:

- advisory discovery questions;
- monthly close readiness prompts;
- bookkeeping hygiene review prompts;
- management-report preparation outline;
- high-risk human review boundary.

The FDE Pack does not provide final accounting, tax, payroll, audit, compliance,
or financial reporting conclusions for real customers.

## Workflow Stages

| Stage | No-code Activity | Output |
| --- | --- | --- |
| 1. Intake | Capture the user goal and current project boundary. | User goal summary and missing-context list. |
| 2. Pack fit | Explain why the combined pack is relevant. | Combined-pack fit note. |
| 3. Context packet | Package Org/FDE refs, allowed context, forbidden context, and review needs. | `context-packet.example.md` shape. |
| 4. Task package | Define owner judgement, supporting perspectives, steps, outputs, blockers, and writeback target. | `task-package.example.md` shape. |
| 5. Human review | Keep accounting-adjacent professional review explicit. | `requires-human-review` or approved status. |
| 6. Project record | Point private facts to `workspace/projects/<project-id>/`. | Private record placeholder only. |
| 7. Verification | Record pass, missing, not-run, blocked, and human-review states. | Verification result example. |
| 8. Governance | Record decision, evidence, approval boundary, and rejected writes. | Governance record example. |

## Customer-private Boundary

Private content belongs in:

```text
workspace/projects/<project-id>/
```

or another approved customer-private evidence location.

Do not put real customer names, invoices, contracts, ledgers, revenue reports,
platform exports, tax materials, payroll records, bank statements, screenshots,
private meeting notes, credentials, tokens, cookies, passwords, API keys,
connection strings, or secrets into this reusable example.

External project `.agentpal/` remains thin binding metadata only. It must not
receive `.agentpal/org-pack/`, `.agentpal/fde-pack/`, `.agentpal/pals/`,
`.agentpal/workflows/`, `.agentpal/memory/`, `.agentpal/reports/`,
`.agentpal/capability-inventory/`, or `.agentpal/business-systems/` by default.

## Human Review

Human review is retained for:

- accounting-adjacent interpretations;
- revenue-record language;
- month-end readiness statements;
- compliance-sensitive statements;
- any final customer-facing claim based on private records.

Missing evidence remains `missing`. Unreviewed professional conclusions remain
`requires-human-review`. A `not-run` check is not a pass.

## Output Package

A public-safe output package may include:

- a monthly content planning rhythm;
- a revenue-record handoff note template with empty placeholders;
- a monthly retrospective structure;
- a list of private evidence needed from the project record;
- a human review checklist;
- a verification result with explicit `not-run`, `missing`, and
  `requires-human-review` states.

## What Is Not Executed

This example does not:

- inspect the active project;
- scan files or systems;
- call external APIs;
- connect to accounting software;
- generate real revenue records;
- approve accounting conclusions;
- publish content;
- modify central roster files;
- modify official Pal files;
- write customer-private facts into reusable packs;
- write thick assets into external project `.agentpal/`.
