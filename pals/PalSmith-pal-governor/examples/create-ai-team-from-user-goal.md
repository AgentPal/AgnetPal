# Example: Create AI Team From User Goal

This example shows the PalSmith path for turning a broad work goal into a bounded AI team design.

## Raw User Input

```text
/pal PalSmith I run a tiny cross-border ecommerce brand.
I want an AI team that helps me research products, write listings, answer customer questions, and review launch plans.
I do not want anything that automatically publishes or touches ad accounts.
```

## PalSmith Clarification

PalSmith asks:

1. Which marketplace and language pair matter first?
2. Do you already have product notes, supplier notes, or customer FAQ material?
3. Do you want one user-facing entry Pal or separate direct-call Pals?
4. What should require human approval?
5. Should the team be private, team-local, or public-shareable?

## Clarified Goal

- Market: US-facing ecommerce.
- Language: Chinese planning, English listing output.
- Team status: private draft.
- Human approval required: product claims, pricing, launch decisions, paid ads, supplier negotiation.
- Existing Pal reuse: no existing private team Pals.

## Capability Domains

| domain | reason |
| --- | --- |
| product research | compare market signals and customer pain points |
| listing copy | draft title, bullets, description, and claim-safe variants |
| customer support | convert FAQ and policy into response drafts |
| launch review | inspect plan risk, missing evidence, and approval gates |
| team coordination | keep scope, privacy, and handoff boundaries clear |

## Proposed Team

| Pal | Role | Non-role | Key assets |
| --- | --- | --- | --- |
| Harbor | Main Pal / leader / Conductor for this private team | does not make final business decisions | team README, context rules, launch workflow |
| Scout | product research Pal | does not claim verified market data without sources | research knowledge, source coverage template, product comparison evals |
| Luma | listing copy Pal | does not make unsupported product claims | listing templates, claim-safety workflow, listing examples |
| Ember | support reply Pal | does not approve refunds or alter orders | FAQ knowledge, response runbook, escalation evals |
| Quinn-review candidate | verification consultant when registered and available | does not own the team | review package and acceptance checklist |

Team members are candidate capability holders. They are not permanent route targets. Mira remains the default entry Pal for the AgentPal workspace unless this private team is separately installed and a confirmed team entry path is created.

## Draft Team Structure

```text
teams/cross-border-commerce-private/
  README.md
  context-sharing-rules.md
  launch-review-workflow.md
  examples/first-product-launch-flow.md
  evals/team-collaboration-boundary-eval.md
  reports/team-creation-report.md
  members/
    Harbor-main/
    Scout-research/
    Luma-listing/
    Ember-support/
```

## Material Classification

| source id | source | sensitivity | asset mapping | handling |
| --- | --- | --- | --- | --- |
| S1 | supplier product notes | private | Scout knowledge and Luma claim-safety examples | preserve uncertainty and source pointer |
| S2 | previous customer questions | private | Ember FAQ knowledge and examples | synthesize without customer identifiers |
| S3 | launch checklist | team-local | Harbor workflow and team evals | convert repeated decisions into workflow |
| S4 | pricing notes | excluded from public | private-only launch context | do not include in public examples |

## Team Flow Example

1. User asks Harbor to prepare a launch review for a product.
2. Harbor requests a context packet with product notes, target market, and approval boundary.
3. Harbor asks Scout for research assumptions and missing evidence, if Scout is available in the private team.
4. Harbor asks Luma for listing draft alternatives, bounded by approved product claims.
5. Harbor asks Ember for likely support questions and response drafts.
6. Harbor summarizes risks, missing evidence, launch checklist status, and human approval gates.

This flow is a team design pattern, not an active multi-agent runtime claim.

## Runtime Task Package Used

Use `templates/task-packages/create-ai-team-from-goal.md`.

Filled target:

```text
Team goal: cross-border ecommerce launch support
Target users: solo founder and assistant
Recurring work situations: product research, listing draft, FAQ replies, launch review
Preferred team size or maximum: 4 member Pals plus optional reviewer
Expected user-facing entry Pal: Harbor
Sensitive or private materials: supplier notes, customer questions, pricing notes
Target write path: approved private team draft directory
Public, team-local, or private use: private
May the runtime write files after showing the path list: yes
```

## Team Health Check

| check | result | evidence |
| --- | --- | --- |
| team purpose | pass | launch support is explicit |
| Main Pal / leader boundary | pass | Harbor coordinates but does not decide |
| member jobs | pass | each member has role and non-role |
| collaboration rules | pass with risks | needs stronger stop condition for unsupported claims |
| fixed route risk | pass | members are candidate capability holders |
| private leakage | pass | pricing and customer identifiers excluded |
| active runtime claim | pass | flow states no active multi-agent runtime |
| publish readiness | not ready | private draft and source sanitation incomplete |

## Repair Package

Issue list:

| id | severity | issue | repair |
| --- | --- | --- | --- |
| R1 | major | unsupported product-claim stop condition is thin | update `context-sharing-rules.md` and Luma claim-safety workflow |
| R2 | minor | Quinn review is only a candidate | add not-run note unless current contacts and registry evidence are checked |

Runtime repair instructions:

1. Update only the team context rules, Luma workflow, and team eval.
2. Do not write contacts or registry.
3. Return file list, parse results, and checks not run.

## Usage Examples

```text
/pal Harbor Prepare a launch review packet for this product note.
/pal Harbor Turn these supplier notes into research questions, listing risks, and support FAQ drafts.
/pal Harbor Check whether this listing draft makes unsupported claims.
```

Expected output:

- team task summary;
- domain contributions;
- missing evidence;
- privacy or claim risks;
- human approval gates;
- next repair or creation package.

## Not-Do List

The team must not publish listings, change prices, touch ad accounts, make unsupported claims, expose supplier notes publicly, or present its team flow as active Deep Conductor behavior. PalSmith must not register team members without a separate confirmed registration package.
