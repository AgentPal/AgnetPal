# Example: Create First Professional Pal

This example shows the end-to-end PalSmith path for creating one professional Pal from a user's plain-language goal and small material set.

## Raw User Input

```text
/pal PalSmith I want a Pal that helps my small Shopify store handle customer support replies.
It should answer refund, shipping, sizing, and damaged-item messages.
I have a policy note and some previous replies.
I want it private for now.
```

## PalSmith Clarification

PalSmith asks only for missing high-impact details:

1. What is the store policy for refunds after delivery?
2. Which previous replies are approved for private ingestion?
3. Should the Pal escalate legal, chargeback, and angry VIP cases?
4. Preferred tone: warm, concise, brand-polished, or strict policy voice?
5. Target write path for the draft Pal?

## Clarified Scope

- Pal name: StoreCare
- Pal id: `storecare-support-pal`
- Job: draft customer support replies for a small Shopify store.
- Target users: store owner and part-time support assistant.
- Non-responsibilities: legal advice, final refund approval, payment disputes, and live account changes.
- Privacy: private draft only.
- Source material: approved policy note and previous replies.

## Draft Identity Summary

StoreCare is a customer support reply Pal. It turns a customer message and order context into a reply draft, escalation note, and policy citation. It should be warm and concise, but it must not pretend to have changed an order or issued a refund.

## Draft Structure

```text
pals/StoreCare-support/
  PAL.md
  pal.json
  SKILL.md
  README.md
  core/output-contract.md
  knowledge/refund-shipping-sizing-policy.md
  skills/support-reply-drafting-skill.md
  workflows/customer-message-triage-workflow.md
  runbooks/damaged-item-response-runbook.md
  templates/customer-reply-template.md
  examples/refund-delay-reply.md
  examples/damaged-item-reply.md
  evals/support-reply-boundary-eval.md
  reports/creation-report.md
```

## User Material Classification

| source id | source | sensitivity | asset mapping | handling |
| --- | --- | --- | --- | --- |
| S1 | refund and shipping policy note | private | `knowledge/refund-shipping-sizing-policy.md` | summarize policy rules and preserve source pointer |
| S2 | previous warm reply examples | private | examples and output contract tone notes | synthesize examples without customer names |
| S3 | damaged item procedure | private | runbook and workflow | convert steps into escalation-aware runbook |
| S4 | customer names and order ids | excluded | none | do not write into assets |

## Key File Summaries

- `PAL.md`: explains StoreCare's job, user, boundaries, and escalation behavior.
- `pal.json`: stores id, display name, owner scope, version status, and contact eligibility as draft only.
- `core/output-contract.md`: requires reply draft, policy basis, escalation flag, missing information, and confidence.
- `knowledge/refund-shipping-sizing-policy.md`: captures approved store policy with uncertainty notes.
- `skills/support-reply-drafting-skill.md`: defines the repeatable capability of drafting support replies from message plus context.
- `workflows/customer-message-triage-workflow.md`: separates standard reply, missing-info request, escalation, and refusal.
- `runbooks/damaged-item-response-runbook.md`: gives step-by-step response handling.
- `evals/support-reply-boundary-eval.md`: tests refund promise, legal dispute, missing order details, and privacy leakage.

## Runtime Task Package Used

Use `templates/task-packages/create-first-professional-pal.md`.

Filled target:

```text
Requested Pal job: Shopify customer support reply drafting
Target users: store owner and support assistant
3-5 example tasks: refund delay, shipping update, size exchange, damaged item, angry customer
Tasks this Pal must not do: issue refunds, edit orders, give legal advice, reveal private customer data
Source materials approved for reading: policy note, previous replies
Sensitive or private materials: customer names, order ids, private policy note
Target write path: approved private Pal draft directory
Public, team-local, or private use: private
May the runtime write files after showing the path list: yes
```

## Health Check Result

| check | result | evidence |
| --- | --- | --- |
| PAL clarity | pass | job and non-job are explicit |
| `pal.json` parse | pass | JSON parser succeeded |
| real knowledge | pass with risks | policy note covered, but sizing details are thin |
| Skills and workflows | pass | drafting Skill and triage workflow are scenario-specific |
| examples | pass | refund and damaged-item examples exist |
| evals | pass with risks | needs one chargeback escalation eval |
| private leakage | pass | customer names and order ids excluded |
| publish readiness | not ready | private draft, no public sanitization |

## Repair Package

Issue list:

| id | severity | issue | repair |
| --- | --- | --- | --- |
| R1 | minor | sizing policy is thin | ask user for size chart rule or mark missing context |
| R2 | major | chargeback escalation eval missing | add eval case for payment dispute refusal and escalation |

Runtime repair instructions:

1. Update only `knowledge/refund-shipping-sizing-policy.md` and `evals/support-reply-boundary-eval.md`.
2. Do not add customer names or order ids.
3. Return changed files and not-run checks.

## Usage Examples

```text
/pal StoreCare Draft a reply to this customer asking why their refund has not arrived.
/pal StoreCare Triage this damaged-item message and tell me whether to escalate.
/pal StoreCare Rewrite this shipping-delay reply in our warm but concise support tone.
```

Expected output:

- reply draft;
- policy basis;
- escalation flag;
- missing information;
- confidence and risks.

## Not-Do List

StoreCare must not approve refunds, edit orders, access Shopify, make legal claims, or reveal customer data. PalSmith must not register StoreCare or call it publish-ready until a separate registration and readiness package passes.
