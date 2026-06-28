# Org + FDE Combined Pack Usage Scenario

## Scenario Summary

This scenario shows how a user can understand and use the public-safe Content
Ops with Accounting Advisor Combined Pack:

- combined pack: `examples/combined-packs/content-ops-with-accounting-advisor/`
- Org Pack reference: `examples/org-packs/content-ops-org-pack/`
- FDE Pack reference: `examples/fde-packs/accounting-advisor-fde-pack/`

The example is a no-code asset workflow. It is not a marketplace, connector,
installer, scanner, validator, external API client, automatic executor, or
keyword router.

## Who This Is For

Use this scenario when a contributor, maintainer, or user wants to understand
how reusable organization assets, expert delivery assets, Pal judgement, and
central project records fit together.

The scenario is public-safe and generic. It does not describe a real customer,
real project, real invoice, real accounting system, real contract, real tax
material, private screenshot, credential, token, password, API key, cookie, or
secret.

## What The Combined Pack Contains

The combined pack contains:

- `combined-pack.json`, which references the Org Pack and FDE Pack;
- composition notes that explain how the references work;
- recommended Pals as AI judgement inputs only;
- PalSmith audit notes;
- reusable/private boundary notes;
- thin binding relationship notes;
- verification notes.

The Org Pack describes reusable content operations structure. The FDE Pack
describes reusable accounting advisor delivery assets and high-risk human
review requirements.

## What It Does Not Do

The combined pack does not:

- execute work;
- connect to customer systems;
- store credentials;
- scan files or systems;
- validate external systems automatically;
- install anything;
- publish to a marketplace;
- route work by keyword;
- copy Org Pack, FDE Pack, Pal assets, memory, reports, workflows, governance,
  or capability records into an external project `.agentpal/` directory;
- store customer-private data in the reusable example.

## Step 1: User Chooses The Combined Pack

A user chooses the combined pack when they need a reusable pattern for content
operations work that may include accounting-adjacent review or reporting
language.

The user should treat the pack as a reference set, not as a program. The safe
starting point is:

```text
examples/combined-packs/content-ops-with-accounting-advisor/README.md
```

The user can then inspect:

- `combined-pack.json`
- `ORG-FDE-COMPOSITION.md`
- `recommended-pals.md`
- `customer-private-boundary.md`
- `thin-binding-relationship.md`
- `palsmith-audit-note.md`

## Step 2: Mira Explains The Pack

Mira may explain the pack as the default entry Pal. A safe explanation is:

```text
Mira can explain that this combined pack joins a reusable content operations
organization pattern with a reusable accounting advisor delivery pattern.
Mira can help the user decide whether the pack is relevant, what context is
missing, and what must stay private.
```

Mira must not turn the recommendation list into a route map. She may say that
Mira, PalSmith, Morgan, Quinn, Vega, and Harper are possible judgement inputs,
but the current AI still chooses any owner Pal case-by-case from the user goal,
central roster, risk, project context, and evidence needs.

## Step 3: PalSmith Reviews The Pack

PalSmith may review or re-check the pack as no-code asset governance.

PalSmith can:

- confirm `combined-pack.json` parses;
- confirm the Org Pack and FDE Pack references exist;
- classify reusable versus customer-private assets;
- confirm recommended Pals are AI judgement inputs only;
- check missing fields;
- produce an issue list;
- produce an approval checklist;
- retain human review requirements.

PalSmith cannot automatically modify central contacts, write an external
project, call an API, publish a marketplace entry, or turn customer-private
material into reusable content.

## Step 4: User Binds An External Project Through Thin Binding

If a user wants to use AgentPal with an external project, the project remains
thin-bound.

Allowed project-local binding files are:

```text
.agentpal/project.json
.agentpal/AGENTPAL.md
AGENTS.md protected block
CLAUDE.md protected block
.claude/settings.local.json
.gitignore entry
```

Forbidden default project-local directories are:

```text
.agentpal/org-pack/
.agentpal/fde-pack/
.agentpal/pals/
.agentpal/workflows/
.agentpal/memory/
.agentpal/reports/
.agentpal/capability-inventory/
.agentpal/business-systems/
```

The external project's `.agentpal/` directory points back to the AgentPal
Workspace. It does not become the storage location for reusable packs or
customer-private records by default.

## Step 5: AgentPal Records Project-private Facts In Central Project Records

Private project facts belong in a central project record such as:

```text
workspace/projects/<project-id>/
```

This scenario does not create a real project record. The path is a placeholder
for an approved private record.

Use the central project record for:

- `source-map/`, for public-safe indexes of project files and user-provided
  docs;
- `derived-knowledge/`, for structured summaries derived from project material;
- `memory/`, for project memory and decisions;
- `reports/`, for task and verification reports;
- `governance/`, for project-specific governance notes;
- `capability-inventory/`, for project-level capability evidence and unknown /
  not-run / missing states.

Do not store these private facts in the reusable combined pack or in external
project `.agentpal/` by default.

## Step 6: Org Pack / FDE Pack / Pal Assets Are Used As AI Judgement Input

The Org Pack contributes reusable content operations structure. The FDE Pack
contributes public-safe accounting advisor delivery assets.

Pal assets contribute judgement perspectives through the central roster.
Recommendations are AI judgement inputs only. They are not fixed assignments,
keyword maps, domain maps, role maps, or automatic dispatch rules.

## Step 7: Human Review And Verification

Accounting, tax, payroll, audit, compliance, and financial reporting outputs
require qualified human review before real customer use.

Verification should keep these states explicit:

- `pass`
- `missing`
- `not-run`
- `blocked`
- `requires-human-review`

Do not convert missing evidence or unreviewed customer facts into `pass`.

For a concrete workflow and governance usage example, see:

```text
examples/combined-packs/content-ops-with-accounting-advisor/workflow-usage-example.md
examples/combined-packs/content-ops-with-accounting-advisor/context-packet.example.md
examples/combined-packs/content-ops-with-accounting-advisor/task-package.example.md
examples/combined-packs/content-ops-with-accounting-advisor/governance-record.example.md
examples/combined-packs/content-ops-with-accounting-advisor/verification-result.example.md
```

## What Remains Reusable

Reusable content includes:

- generic Org/FDE composition notes;
- public-safe checklists;
- public-safe boundary language;
- PalSmith audit patterns;
- verification checklist shapes;
- thin binding explanations.

## What Must Stay Customer-private

Customer-private content includes:

- real customer names;
- real invoices, contracts, tax materials, ledgers, payroll records, bank
  statements, or financial statements;
- private project facts;
- private project memory;
- private reports;
- private governance notes;
- customer system identifiers;
- screenshots;
- credentials, tokens, cookies, passwords, API keys, private keys, connection
  strings, or secrets.

## What Is Forbidden

Do not use this usage scenario to:

- publish a marketplace item;
- create a connector or API client;
- install software;
- scan or validate live systems automatically;
- create keyword routing;
- copy Pal assets or central contacts into external projects;
- create a real customer project record in public examples;
- store customer-private evidence in the reusable combined pack.
