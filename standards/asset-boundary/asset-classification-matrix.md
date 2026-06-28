# Asset Classification Matrix

Date: 2026-06-28
Standard id: `agentpal-asset-classification-matrix.v0.5`

## Purpose

This matrix gives PalSmith, Org Pack authors, FDE Pack authors, Pal Asset maintainers, and reviewers a shared way to classify assets before storing, publishing, reusing, or deriving examples from them.

Classification is AI judgement plus human review when sensitivity, privacy, publication, or customer derivation is involved. It is not keyword routing and not an automated scanner.

## Matrix Fields

Every classification result should record:

- `asset_type`
- `reusable_allowed`
- `customer_private`
- `can_be_deidentified`
- `default_storage`
- `publish_allowed`
- `requires_human_review`
- `examples`
- `forbidden_examples`

Unknown sensitivity must be treated as not publishable until reviewed.

## Classification Matrix

| asset_type | reusable_allowed | customer_private | can_be_deidentified | default_storage | publish_allowed | requires_human_review | examples | forbidden_examples |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| empty template | yes | no | not needed | `templates/` or reusable pack templates | yes after review | yes | blank checklist, empty org.json shell | template prefilled with a real customer's system names |
| generic workflow | yes | no | not needed | `standards/`, `templates/`, Org Pack / FDE Pack reusable areas | yes after review | yes | generic intake-review-delivery workflow | workflow that exposes a real customer's approval chain |
| generic checklist | yes | no | not needed | `templates/`, `examples/`, `evals/` | yes after review | yes | public-safety checklist | checklist containing a customer's private compliance controls |
| generic runbook | yes | no | not needed | `runbooks/`, Org Pack / FDE Pack reusable areas | yes after review | yes | general release readiness runbook | step list using a real internal dashboard URL |
| generic Pal Skill pattern | yes | no | not needed | PalSmith / Pal Asset reusable patterns | yes after review | yes | no-code review skill pattern | Pal Skill copied from a private customer process without review |
| public-source summary | yes | no when sourced from public material | sometimes | `knowledge/`, `research/`, public examples | yes with citation/review | yes | summary of public documentation | paid/private document summary or copied article body |
| de-identified case | yes after review | originally yes, after approved de-identification no | yes | public examples after review | yes after review | yes | fictionalized delivery scenario | renamed customer case that preserves dates, structure, and unique facts |
| fake public example | yes | no | not needed | `examples/` | yes after review | yes | clearly fictional company and data | fake secret-looking value that could be mistaken for a real credential |
| project requirement | no by default | often yes | sometimes | active project docs or central project record | no by default | yes | private product requirement | public reusable pack containing real customer roadmap |
| meeting minutes | no by default | yes unless public/approved | sometimes | private project record or approved minutes store | no by default | yes | private action notes | unapproved transcript excerpt in a public example |
| business data | no by default | yes | sometimes aggregate only | private project record or customer-approved data area | no by default | yes | anonymized aggregate pattern | customer revenue, invoices, tax, medical, legal, or account records |
| system screenshot | no by default | yes | rarely | private evidence store | no by default | yes | redrawn generic UI diagram | screenshot showing internal URLs, names, IDs, or account data |
| credential or secret | never | yes | no | approved secret manager outside public pack | never | yes | placeholder field name only | token, cookie, API key, password, private key, connection string |
| internal governance note | maybe | organization-internal | sometimes | internal docs or approved public standard after review | no by default | yes | generalized policy | private escalation decision naming a customer |
| central Pal roster | no copy | organization asset | no | `workspace/organization/contacts/` | no as copied payload | yes | reference path only | copied roster embedded in project or public Org Pack |
| official Pal Pack body | no copy | organization asset | no | `official/pals/` | no as copied payload | yes | reference to a Pal path | copied Pal body inside external project `.agentpal/pals/` |
| Capability Inventory reference | yes as reference | maybe | sometimes | capability inventory area or Org Pack reference | yes after review if public-safe | yes | public-safe capability profile reference | automatic scanner output or connector config |
| FDE delivery note | maybe | often customer-private | yes if generalized | private FDE record or reusable FDE Pack after review | no by default | yes | generalized delivery pattern | real customer delivery notes with names or metrics |

## Default Decisions

Use these defaults unless stronger evidence exists:

- `publish_allowed=false`
- `requires_human_review=true`
- `contains_credentials=false` only when inspection found no credential-like material
- `customer_private=false` only after review confirms no customer-private content
- `deidentified=false` until a de-identification review is complete
- `external_project_write_allowed=false`

## Classification Outcomes

### Public Reusable

Use when the asset is generic, public-safe, reviewed, and safe to reuse.

### Private Or Project-private

Use when the asset contains customer facts, project details, private evidence, private memory, or uncertain sensitivity.

### De-identification Candidate

Use when a useful pattern exists but the source contains private or identifying details. The source remains private until review approves a de-identified derivative.

### Forbidden Public

Use when the asset contains credentials, real customer private data, private screenshots, unapproved meeting content, private legal/finance/medical/tax materials, or other sensitive facts that must not enter public reusable packs.

## Review Questions

Before marking an asset reusable, ask:

1. Could a customer, person, account, system, contract, project, or private event be reconstructed from this asset?
2. Does it contain or imply credentials, tokens, cookies, API keys, passwords, internal URLs, unique IDs, or account identifiers?
3. Does it preserve a real customer's process, metric, schedule, or business rule in a recognizable way?
4. Is it safe to publish and safe to copy into another AgentPal Workspace?
5. Is it only a recommendation or judgement input, rather than a route map or automatic assignment?
6. Has human review approved publication if the source came from user, customer, meeting, project, or operational material?

If any answer is uncertain, do not publish.
