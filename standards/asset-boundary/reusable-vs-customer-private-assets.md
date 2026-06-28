# Reusable Vs Customer-private Asset Boundary Standard

Date: 2026-06-28
Standard id: `agentpal-reusable-private-asset-boundary.v0.5`

## Purpose

This standard defines the boundary between reusable AgentPal organization assets and customer-private assets.

It applies to Org Packs, FDE / expert delivery packs, PalSmith asset classification work, Pal Assets, examples, templates, evals, validation records, and release-support notes.

This standard is no-code governance. It is not a scanner, validator, connector, installer, marketplace program, route map, or execution engine.

## Core Rule

Reusable assets must be safe to publish, safe to copy into another AgentPal Workspace, and safe to use as a public example.

Customer-private assets must stay out of public reusable packs unless they have been reviewed, de-identified, and explicitly approved as public-safe examples.

Unknown sensitivity is not public-safe.

## Definitions

### Reusable Asset

A reusable asset is a public-safe organization, Pal, workflow, governance, verification, or delivery pattern that can be reused across customers without revealing customer-private facts.

Reusable assets can include:

- generic workflows;
- generic checklists;
- generic runbooks;
- generic Pal Skill patterns;
- de-identified examples;
- empty templates;
- public-source summaries;
- generic governance rules;
- public-safe verification cases;
- reusable memory policy;
- reusable customer-private handling policy.

Reusable assets may live in public standards, templates, examples, evals, release-support notes, Org Packs, FDE Packs, Pal Assets, or approved public-safe organization records.

### Customer-private Asset

A customer-private asset contains information that belongs to a specific customer, user, project, business, meeting, system, contract, account, or operational context and is not approved for public reuse.

Customer-private assets include:

- real customer names, account names, contracts, invoices, finance records, tax records, medical records, legal materials, or compliance materials;
- customer system credentials;
- private project context;
- unapproved meeting minutes, call transcripts, or notes;
- real business data;
- personal sensitive information;
- internal system screenshots;
- tokens, cookies, API keys, passwords, private keys, or other secrets;
- private business rules;
- private evidence;
- private project reports;
- source files, datasets, prompts, examples, or workflows that reveal a customer's internal facts.

### Project-private Record

A project-private record belongs to one active external user project or one central AgentPal project record.

Default storage should be a private project location such as:

```text
workspace/projects/<project-id>/
```

or an approved customer-private evidence store. It must not be promoted into a public reusable pack by default.

### Organization-internal Record

An organization-internal record is internal to the AgentPal organization or a user's private organization workspace. It may be useful across internal work but is not necessarily publishable.

Organization-internal records can include private governance notes, internal readiness reports, private delivery notes, or non-public memory. They require review before becoming reusable public assets.

### Public Example

A public example is intentionally safe to publish. It uses fake, generic, or public facts and does not contain real customer-private material.

Public examples may show:

- fake company names clearly marked as fictional;
- generic workflows;
- empty template fields;
- public-source facts with citation expectations;
- non-sensitive demonstration data.

### De-identified Example

A de-identified example is derived from sensitive or customer-specific material only after all identifying and reconstructable details have been removed or generalized.

De-identification requires review. It is not simple renaming.

### Forbidden Public Asset

A forbidden public asset is any content that must not be stored in public standards, templates, examples, evals, release notes, reusable Org Packs, reusable FDE Packs, public Pal Assets, or public completion reports.

Forbidden public assets include credentials, real customer private data, private project evidence, unapproved meeting notes, screenshots with internal system information, and route maps that encode deterministic customer-specific dispatch rules.

## Default Storage

| Asset classification | Default storage |
| --- | --- |
| reusable asset | public reusable area after review, such as `standards/`, `templates/`, `examples/`, `evals/`, or approved Org Pack / FDE Pack paths |
| customer-private asset | private central project record or approved private evidence location |
| project-private record | `workspace/projects/<project-id>/` or active project docs when explicitly requested |
| organization-internal record | internal organization workspace or internal documentation area |
| public example | `examples/` after public-safety review |
| de-identified example | `examples/` only after de-identification and human review |
| unknown sensitivity | review queue; not public |

External project `.agentpal/` directories remain thin-binding entry points by default and must not receive reusable Org Pack, Pal Pack, Pal Asset, memory, report, workflow, eval, or capability-inventory payloads by default.

## Publish Rules

An asset may be publishable only when all of these are true:

- it is not customer-private;
- it contains no credentials or secret-like material;
- it contains no real customer data;
- it contains no private project context;
- it contains no unapproved meeting content;
- it contains no reversible identifying details;
- it does not copy central Pal contacts or official Pal bodies into an external project;
- it does not introduce keyword routing, domain routing, role routing, or deterministic dispatch;
- it does not introduce connector, scanner, marketplace, installer, daemon, database, auto-sync, or auto-execution behavior;
- human review is complete for any asset derived from user, customer, meeting, project, or operational material.

## Org Pack And FDE Pack Boundary

Org Packs and FDE Packs may include reusable patterns, recommended Pals, recommended Pal Skill patterns, workflow candidates, runbook candidates, capability references, governance policy, memory policy, and verification checklists.

They must not include customer-private facts by default.

Recommendations are AI judgement inputs only. They are not route maps, assignments, contact edits, or automatic dispatch rules.

## PalSmith And Pal Asset Boundary

PalSmith may classify user-provided material, propose target storage, and produce review records.

PalSmith must preserve sensitivity state and must not silently turn customer-private material into public knowledge, public examples, reusable Org Pack content, or Pal-owned public assets.

If sensitivity is unknown, PalSmith should use review/unclassified or private project records until the user or a reviewer approves a safer target.

## Refusal And Escalation

If a proposed reusable asset includes customer-private data, the correct result is not to polish it into a public pack. The correct result is:

1. mark it customer-private or unknown;
2. move it to a private record or review queue;
3. propose a de-identification plan when appropriate;
4. require human review before publication;
5. keep public reusable packs clean.

## Boundary Statement

This standard does not perform automated detection. It gives PalSmith, Mira, specialist Pals, and host runtimes a shared governance boundary for AI judgement and evidence-based review.
