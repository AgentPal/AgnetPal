# De-identification Standard

Date: 2026-06-28
Standard id: `agentpal-deidentification-standard.v0.5`

## Purpose

This standard defines when customer-private or project-private material may be transformed into a public-safe reusable example, Org Pack asset, FDE Pack asset, Pal Asset example, eval, or template.

De-identification is a governed review process. It is not simple renaming.

## Core Rule

An asset is not de-identified just because names were changed.

De-identification must remove or generalize details that could identify the customer, user, project, account, system, contract, event, business state, or private relationship.

## What Must Be Removed Or Generalized

Remove or generalize:

- customer names, person names, team names, account names, vendor names, and partner names;
- exact dates, locations, schedules, contract terms, prices, invoices, finance figures, tax facts, medical facts, legal facts, and compliance facts;
- account identifiers, user identifiers, project identifiers, ticket IDs, internal URLs, database names, system names, repository names, and file paths that identify a real customer;
- screenshots or UI captures that show internal systems, people, records, or identifiers;
- unique process structures that make the customer recognizable;
- meeting speaker names, private attendee lists, transcript fragments, and unapproved action items;
- real credentials, tokens, cookies, API keys, passwords, private keys, connection strings, and secret-like values;
- private project memory, private evidence, and private business rules.

## What May Remain

After review, a reusable de-identified example may keep:

- the generic problem class;
- the generic workflow pattern;
- generic roles such as requester, reviewer, owner, approver, or delivery lead;
- non-sensitive decision logic;
- public-safe acceptance criteria;
- fake or generic sample values clearly marked as fictional;
- public-safe lessons learned;
- uncertainty and not-run states.

## Reversible Clues Are Forbidden

Do not keep clues that allow reconstruction, including:

- exact timeline plus industry plus unusual process;
- rare role names or internal project code names;
- unique system architecture details;
- distinctive metric combinations;
- customer-specific language copied verbatim;
- private URLs or path fragments;
- real error messages containing internal identifiers.

If the original customer could plausibly recognize the source, the example needs more generalization or must remain private.

## Credential Rule

Credentials cannot be de-identified into public reusable assets by masking only part of the value.

Do not publish:

- partial tokens;
- shortened cookies;
- redacted-but-recognizable passwords;
- real key prefixes with enough surrounding context to identify a system;
- connection strings with host names or account names.

Use generic placeholder labels such as `<credential-placeholder>` only when the surrounding example is otherwise public-safe and clearly fictional.

## High-risk Domains

High-risk domains always require human review before public reuse:

- finance;
- tax;
- medical;
- legal;
- employment and HR;
- education records;
- government identity;
- security incident response;
- contracts and procurement;
- customer support logs;
- private communications or meeting records.

For high-risk domains, prefer generic templates and fictional examples over de-identifying real customer material.

## De-identification Review Steps

1. Preserve the private source in an approved private location.
2. Identify the intended reusable lesson, pattern, checklist, workflow, runbook, or eval.
3. Remove direct identifiers.
4. Generalize indirect identifiers.
5. Replace real values with clearly fictional or generic values.
6. Remove credentials and secret-like material completely.
7. Check for reversible clues.
8. Mark remaining risk and uncertainty.
9. Require human review before publication.
10. Store the public derivative separately from the private source.

## Required Review Record

A de-identification review should record:

- source sensitivity;
- source storage location class, not private path content when unsafe;
- transformation summary;
- removed identifier classes;
- generalized identifier classes;
- credential check result;
- reversible clue check result;
- high-risk domain flag;
- reviewer decision;
- publish decision;
- follow-up notes.

## Fail Conditions

De-identification fails if:

- credentials remain;
- customer-private facts remain reconstructable;
- the source customer, project, or person remains recognizable;
- real screenshots remain;
- private meeting content remains;
- the reviewer cannot explain what was removed and generalized;
- the asset is marked publishable without human review.

## Boundary Statement

This standard does not automate de-identification. It defines the review requirements for AI judgement and human approval before any customer-derived material becomes a reusable public asset.
