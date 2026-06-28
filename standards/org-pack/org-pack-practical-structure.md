# Org Pack Practical Structure Standard

Date: 2026-06-28
Standard id: `agentpal-org-pack-practical-structure.v0.5`

## Purpose

This standard defines a practical, reusable Org Pack structure for AgentPal
v0.5.

An Org Pack is a reusable no-code AI organization asset package. It combines
organization work style, role recommendations, workflow candidates, runbooks,
governance rules, verification checklists, and Capability Inventory references
so a host Runtime or Brain can reason about a work system without turning the
pack into software.

## Scope

Use this structure for public-safe reusable organization packages, delivery
practice packs, FDE-adjacent delivery packs, and team-operation packages.

This standard does not create a FDE Pack by itself, does not modify central
contacts, does not register Pals, and does not change any official Pal asset.

## What An Org Pack Is

An Org Pack is:

- a reusable AI organization asset package;
- a no-code description of organization roles, workflows, governance,
  verification, and capability references;
- an input to AI judgement;
- a public-safe reusable package unless explicitly stored in an approved
  private location.

An Org Pack can recommend Pals, Pal Skills, workflows, runbooks, and Capability
Inventory records. Those recommendations are AI judgement inputs only.

## What An Org Pack Is Not

An Org Pack is not:

- a Pal Pack;
- a project directory;
- an installer;
- a marketplace or hub program;
- a connector;
- a scanner;
- a validator;
- a daemon;
- a database;
- a runtime;
- an auto-sync or auto-execution engine;
- a keyword router or deterministic semantic router.

Org Packs must not copy the central roster, copy official Pal bodies, modify
central contacts, generate official Pal manifests, or write assets into external
project `.agentpal/` directories by default.

## Relationship To PalSmith

PalSmith may create, audit, classify, maintain, and review Org Packs as no-code
governance work. PalSmith may propose central roster or Pal asset changes in a
separate task package, but it must not automatically modify central contacts,
official Pal bodies, `pal.json` files, or external project bindings.

## Reusable Assets Versus Customer-Private Assets

Reusable Org Pack assets must be public-safe and de-identified. They can include
generic organization patterns, role recommendations, workflow candidates,
runbooks, governance rules, verification checklists, and capability reference
policies.

Customer-private assets include real customer data, real account names,
credentials, private system identifiers, private project memory, customer
business rules, private evidence, and project reports. They do not belong in a
public reusable Org Pack. Store them in approved private project records or
customer-private evidence records.

## Practical Structure

A practical Org Pack uses this structure:

```text
ORG.md
org.json
README.md
roles/
workflows/
runbooks/
governance/
capability-inventory/
verification/
private-boundary.md
```

## Root Files

### `README.md`

Purpose: human-facing orientation for the Org Pack.

Belongs here:

- brief package purpose;
- file map;
- public-safe usage notes;
- boundary summary.

Does not belong here:

- private customer data;
- copied central roster;
- deterministic route maps;
- install or connector instructions.

Relationship to Pal assets: may point to Pal types or recommended Pals as
judgement inputs, but must not copy Pal bodies.

Relationship to project records: may explain where project-specific records
belong, but must not store them.

Public safety boundary: keep it publishable and de-identified.

### `ORG.md`

Purpose: organization-level role, workflow, and governance description.

Belongs here:

- reusable organization purpose;
- intended users;
- role model;
- operating principles;
- review and evidence expectations.

Does not belong here:

- Pal identity bodies;
- customer-specific facts;
- runtime execution claims;
- central roster edits.

Relationship to Pal assets: can describe which Pal perspectives may be useful,
but only as AI judgement inputs.

Relationship to project records: can describe how project records should be
created by a separate approved process.

Public safety boundary: keep organization patterns generic and reusable.

### `org.json`

Purpose: machine-readable package metadata and safety flags.

Belongs here:

- id, name, version, schema, type, description;
- recommended Pals as judgement inputs;
- safety flags and default false capabilities.

Required default false fields:

- `external_projects_copy_assets_by_default`
- `can_modify_central_roster`
- `keyword_routing_allowed`
- `credentials_allowed`
- `connector_included`
- `marketplace_program_included`

Does not belong here:

- copied central contacts;
- credentials;
- route maps;
- connector configuration;
- executable instructions.

Relationship to Pal assets: may reference Pal ids, but must not embed Pal
content.

Relationship to project records: may reference private-record policy, but must
not include private record content.

Public safety boundary: metadata must be safe to publish and parse.

## `roles/`

Purpose: reusable organization roles and role-collaboration notes.

Belongs here:

- role descriptions;
- responsibility boundaries;
- collaboration patterns;
- recommended Pal perspectives as judgement inputs.

Does not belong here:

- copied Pal Pack bodies;
- copied central roster files;
- fixed task-to-Pal assignments;
- private staff or customer names.

Relationship to Pal assets: roles may suggest Pals or Pal Skills to consider,
but actual Pal selection remains AI judgement through the central roster.

Relationship to project records: project-specific staffing or ownership belongs
in project records, not this reusable directory.

Public safety boundary: use generic roles and de-identified examples.

## `workflows/`

Purpose: reusable normal workflow candidates for the organization package.

Belongs here:

- workflow maps;
- stage descriptions;
- inputs and outputs;
- owner judgement considerations;
- verification needs.

Does not belong here:

- executable automation graphs;
- daemon jobs;
- connector workflows;
- keyword routing tables;
- project-private task logs.

Relationship to Pal assets: workflows may reference Pal Skills or runbooks as
candidates, but do not copy those assets.

Relationship to project records: project-specific workflow adaptations belong
in approved private project records.

Public safety boundary: keep workflows generic and reusable.

## `runbooks/`

Purpose: reusable exception-handling or concrete operation guides.

Belongs here:

- symptoms;
- checks;
- stop conditions;
- escalation notes;
- verification evidence requirements.

Does not belong here:

- broad strategy that belongs in workflows;
- CLI recipes as execution claims;
- connector secrets;
- customer-specific incident evidence.

Relationship to Pal assets: may point to Pal-owned runbooks as candidates, but
must not copy Pal-owned bodies.

Relationship to project records: customer incidents and private evidence belong
outside the reusable pack.

Public safety boundary: use public-safe examples and avoid sensitive systems.

## `governance/`

Purpose: reusable governance rules, decision records, review checkpoints, and
change-control guidance.

Belongs here:

- approval boundaries;
- review checklists;
- decision-record templates;
- escalation checkpoints;
- ownership and evidence rules.

Does not belong here:

- automatic central roster edits;
- legal approvals claimed as complete;
- private decision records;
- credentials or private evidence.

Relationship to Pal assets: governance can recommend PalSmith, Quinn, or other
Pals for review as AI judgement inputs only.

Relationship to project records: real governance decisions for a customer or
project belong in private records.

Public safety boundary: publish reusable policy, not private outcomes.

## `capability-inventory/`

Purpose: public-safe references to capability types, evidence expectations, and
availability states.

Belongs here:

- capability profile references;
- model / Runtime / Skill / plugin / MCP / business-system categories;
- evidence requirements;
- `unknown`, `not-run`, and `missing` handling rules.

Does not belong here:

- automatic scanners;
- connector configs;
- API credentials;
- live system discovery results;
- deterministic Runtime or Pal selection rules.

Relationship to Pal assets: capability references can inform Pal and Runtime
candidate judgement but must not become Pal contacts or Pal Skills.

Relationship to project records: project-specific capability evidence belongs
in central project records or approved private evidence records.

Public safety boundary: keep capability notes generic and non-secret.

## `verification/`

Purpose: reusable verification checklists and PalBench-style cases.

Belongs here:

- acceptance checks;
- boundary checks;
- evidence requirements;
- pass / fail / not-run / blocked / missing / unknown rules.

Does not belong here:

- false pass claims;
- private evidence;
- runtime logs containing secrets;
- executable validators.

Relationship to Pal assets: verification may reference Pal-owned evals as
candidates, but does not replace them.

Relationship to project records: project-specific verification results belong
in private project records or approved reports.

Public safety boundary: record reusable checks, not private proof.

## `private-boundary.md`

Purpose: explain what must stay out of the reusable Org Pack.

Belongs here:

- private data categories;
- approved private storage targets;
- de-identification policy;
- export and sharing cautions.

Does not belong here:

- the private data itself;
- credentials;
- customer system identifiers;
- private project memory.

Relationship to Pal assets: reminds authors not to copy Pal private memory or
Pal bodies into Org Packs.

Relationship to project records: points private facts to approved project or
customer-private records.

Public safety boundary: this file should be public-safe and policy-only.

## Required Safety Defaults

Every practical Org Pack metadata file should default to:

```json
{
  "external_projects_copy_assets_by_default": false,
  "can_modify_central_roster": false,
  "keyword_routing_allowed": false,
  "credentials_allowed": false,
  "connector_included": false,
  "marketplace_program_included": false
}
```

Recommended additional false flags:

- `scanner_included`
- `validator_included`
- `auto_execution`
- `auto_sync`
- `runtime_included`

## Completion Bar

A practical Org Pack is acceptable when it:

- has the required root files and directories;
- parses `org.json`;
- keeps recommended Pals as AI judgement inputs only;
- separates reusable assets from customer-private assets;
- avoids credentials, connectors, scanners, validators, marketplace programs,
  auto execution, and keyword routing;
- preserves thin binding and central roster boundaries;
- includes verification notes with explicit `not-run`, `missing`, and
  `unknown` handling.
