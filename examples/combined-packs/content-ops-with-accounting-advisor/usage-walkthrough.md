# Usage Walkthrough

## Purpose

This walkthrough explains how to read and use the Content Ops with Accounting
Advisor Combined Pack as a public-safe no-code example.

It does not execute work, call APIs, connect to accounting systems, install
tools, scan files, validate systems automatically, publish marketplace entries,
store credentials, or route by keyword.

## Step 1: Start With The Combined Metadata

Read:

```text
combined-pack.json
```

The key references are:

- `org_pack_ref`: `examples/org-packs/content-ops-org-pack/`
- `fde_pack_refs`: `examples/fde-packs/accounting-advisor-fde-pack/`

The metadata also records that recommended Pals are AI judgement inputs only
and that credentials, connectors, marketplace programs, scanners, validators,
automatic execution, and keyword routing are not included.

## Step 2: Understand The Content Ops Org Pack

The content operations Org Pack contributes:

- reusable intake and coordination structure;
- source-pack and draft-review workflow candidates;
- publishing readiness review expectations;
- Pal recommendations as judgement inputs;
- private-boundary reminders for content work.

It does not publish content, operate accounts, call systems, or decide owner
Pals by keyword.

## Step 3: Understand The Accounting Advisor FDE Pack

The accounting advisor FDE Pack contributes:

- advisory discovery checklist;
- monthly close readiness checklist;
- bookkeeping hygiene review checklist;
- management-report preparation outline;
- update policy notes;
- high-risk human review boundary.

It does not provide final tax, audit, payroll, compliance, or financial
reporting conclusions for real customers.

## Step 4: Use Recommended Pals As Judgement Inputs

The combined pack recommends Mira, PalSmith, Morgan, Quinn, Vega, and Harper as
possible perspectives.

These recommendations are not a route map. They are not:

- keyword routes;
- domain routes;
- role maps;
- fixed assignments;
- central roster edits;
- automatic dispatch rules.

The current AI must still judge the owner Pal from the user request, central
roster, project context, risk, evidence needs, and deliverable.

## Step 5: Use The PalSmith Audit Note

Read:

```text
palsmith-audit-note.md
```

Use it to confirm:

- the composition is valid as a public-safe example;
- no blocking metadata field is missing;
- reusable/private boundaries are explicit;
- no connector, credential, keyword route, marketplace, scanner, or validator
  program is included;
- human review is required.

## Step 6: Apply The Customer-private Boundary

Read:

```text
customer-private-boundary.md
```

Keep real customer books, invoices, contracts, tax materials, ledgers, payroll
records, bank statements, account names, screenshots, private project context,
and credentials out of this reusable example.

Private material belongs in:

```text
workspace/projects/<project-id>/
```

or an approved customer-private delivery / evidence record.

## Step 7: Apply The Thin Binding Relationship

Read:

```text
thin-binding-relationship.md
```

An external project may point back to AgentPal through thin binding files, but
the combined pack itself remains in the AgentPal Workspace. Do not copy Org Pack
assets, FDE Pack assets, Pal assets, workflows, memory, reports, capability
inventory, or business-system records into project-local `.agentpal/` by
default.

## Step 8: Verify Before Reuse

Read:

```text
verification-checklist.md
```

Before reuse, confirm JSON parse, referenced packs, private boundary, thin
binding, recommended Pal non-routing status, central roster boundary, official
Pal boundary, and human review status.
