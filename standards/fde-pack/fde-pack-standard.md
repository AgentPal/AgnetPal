# FDE / Expert Delivery Pack Standard

Date: 2026-06-28
Standard id: `agentpal-fde-pack-standard.v0.5`

## Purpose

An FDE Pack is a reusable no-code expert delivery asset package for AgentPal.

FDE can be read as Field Delivery Pack, Functional Delivery Pack, or Expert Delivery Pack. The name is intentionally descriptive in this standard; it does not need to be final product branding.

FDE Packs help experts, consultants, operators, and industry practitioners turn experience into reusable, maintainable, and auditable delivery assets. They can contain professional judgement rules, delivery scopes, reusable checklists, workflow notes, handoff templates, verification criteria, update policies, and customer-private boundaries.

An FDE Pack is not a program. It is not a CLI, Web App, Desktop App, installer, scanner, validator, connector, database, marketplace/hub program, API client, auto sync engine, or auto execution engine.

## Intended Users

FDE Packs are for:

- independent experts who want to package their delivery method;
- consultants who repeat similar discovery, review, or advisory workflows;
- companies that want reusable public-safe delivery standards;
- AgentPal organizations that want no-code expert assets to support Pal, Org Pack, workflow, runbook, and verification work.

## Relationship To Org Pack

An FDE Pack may be referenced by an Org Pack or combined into a larger organization package.

Org Packs describe organization-level structure and governance. FDE Packs describe a specific expert delivery method, professional scope, reusable assets, and review obligations.

An FDE Pack may recommend Pals, Org Packs, workflows, runbooks, Capability Inventory records, or verification checklists. Recommendations are AI judgement inputs only. They are not routes, hard assignments, keyword maps, domain maps, role maps, or deterministic dispatch tables.

## Relationship To Pal Assets

An FDE Pack is not a Pal Pack. It does not create or modify a Pal identity.

An FDE Pack may recommend Pal perspectives or Pal Skill candidates, but it must not copy Pal bodies, write to official Pal directories, modify central contacts, or store runtime Agent Skills as Pal Skills.

## Required Structure

A minimal FDE Pack must include:

```text
FDE.md
fde.json
expert-profile.md
delivery-scope.md
reusable-assets.md
customer-private-boundary.md
update-policy.md
verification-checklist.md
```

Optional fuller packs may add public-safe examples, workflow candidates, runbook candidates, source notes, glossary files, evidence templates, or customer-private pointer files in approved private locations. Optional files must preserve the same boundaries as the required files.

## Required Files

| File | Purpose |
| --- | --- |
| `FDE.md` | Human-readable expert delivery pack entry, purpose, audience, and use boundary. |
| `fde.json` | Machine-readable public-safe metadata and boundary flags. |
| `expert-profile.md` | Expert role, experience scope, qualification assumptions, and non-responsibilities. |
| `delivery-scope.md` | What the pack can help deliver, what it cannot deliver, and required human review points. |
| `reusable-assets.md` | Public-safe reusable checklists, templates, judgement prompts, and delivery patterns. |
| `customer-private-boundary.md` | Rules that separate reusable pack assets from customer-private evidence, data, and records. |
| `update-policy.md` | Professional content maintenance, review cadence, source freshness, and high-risk update obligations. |
| `verification-checklist.md` | Checks that must pass before a pack is reused, customized, or published. |

## `fde.json` Required Fields

`fde.json` must parse as JSON and include public-safe metadata plus boundary flags.

Required default flags:

```json
{
  "credentials_allowed": false,
  "customer_private_assets_allowed_in_pack": false,
  "external_projects_copy_assets_by_default": false,
  "keyword_routing_allowed": false,
  "connector_included": false,
  "marketplace_program_included": false,
  "requires_human_review": true
}
```

Other recommended metadata:

- `schema`
- `id`
- `name`
- `pack_type`
- `version`
- `status`
- `domain`
- `risk_level`
- `intended_users`
- `recommended_pals`
- `recommended_workflows`
- `reusable_asset_paths`
- `customer_private_boundary`
- `update_policy`
- `verification_checklist`

## Reusable Assets

Reusable assets may include:

- de-identified delivery scopes;
- public-safe checklists;
- public-safe templates;
- professional judgement criteria;
- workflow candidates;
- runbook candidates;
- handoff templates;
- verification checklists;
- public-safe examples;
- update policies;
- source review requirements.

Reusable assets must be safe to publish and safe to copy into another AgentPal Workspace.

## Customer-Private Assets

Customer-private assets must not be stored in a reusable public FDE Pack.

Customer-private assets include:

- real customer data;
- real contracts;
- real invoices;
- real ledgers;
- real financial statements;
- tax filings;
- medical records;
- legal files;
- customer databases;
- credentials, tokens, API keys, cookies, passwords, and secrets;
- sensitive personal information;
- customer system identifiers;
- private project memory;
- private evidence;
- private reports;
- proprietary business rules that reveal customer operations.

Customer-private assets belong in approved private records, central project records, or customer-private delivery records. They must not be copied into examples, templates, or public reusable packs.

## High-Risk Domain Boundary

High-risk professional domains include medical, legal, tax, accounting, financial, compliance, employment, insurance, safety, and regulated industry advice.

FDE Packs in high-risk domains must:

- require human expert review;
- state jurisdiction, date, source, and applicability limits where relevant;
- preserve `unknown`, `not-run`, `missing`, and `requires-review`;
- include an update policy;
- include a verification checklist;
- avoid final professional determinations without qualified human approval;
- avoid customer-specific advice without customer-private review context.

## Update Policy Requirement

Every FDE Pack must define how professional content is maintained.

The update policy should state:

- owner or reviewer role;
- review cadence;
- source freshness requirements;
- known stale-content risks;
- high-risk update triggers;
- deprecation or replacement rules;
- how customer-private adaptations are kept separate from reusable pack updates.

## Verification Requirement

Every FDE Pack must include a verification checklist.

Verification must check:

- required files exist;
- `fde.json` parses;
- boundary flags are safe;
- reusable assets are public-safe;
- customer-private assets are excluded;
- high-risk human review is required;
- no connector, scanner, validator, marketplace, or auto execution behavior exists;
- no keyword routing map exists;
- no credentials or secrets exist.

## Prohibited Defaults

FDE Packs must not:

- include real customer credentials or secrets;
- include real customer private data;
- include real contracts, real financial privacy, customer databases, or sensitive personal information;
- copy assets into external project `.agentpal/` by default;
- modify central contacts or official Pal files;
- create keyword routes, `keyword_map`, `domain_map`, or `role_map`;
- act as a connector, API client, scanner, validator, installer, marketplace/hub program, CLI, app, daemon, database, auto sync engine, or auto execution engine;
- call external APIs or business systems;
- claim runtime actions happened without current runtime evidence.

## Completion Decision Terms

Use:

- `pass`
- `partial`
- `missing`
- `not-run`
- `blocked`
- `requires-human-review`

Do not convert `missing`, `not-run`, or `requires-human-review` into `pass`.
