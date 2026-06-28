# Faye, Delivery Packs, And Deep Conductor Overview

## Purpose

AgentPal v0.5 adds Faye / 菲伊 as the AI Delivery Pal pattern because Org Pack and FDE Pack standards alone do not prove a business can move from a real request to a usable AI team delivery structure.

Faye closes that gap as a no-code delivery owner. Faye turns business goals into Delivery Packs, Pal Team Blueprints, Faye Build Requests, first Task Packages, acceptance criteria, training notes, and review records. Faye does not become an executor or a connector.

## Pack Relationships

| Asset | Meaning |
| --- | --- |
| Org Pack | Reusable AI organization package: roles, workflows, runbooks, governance, and capability references. |
| FDE Pack | Reusable expert delivery method and review boundary. |
| Delivery Pack | Concrete business delivery package for one project. |
| Pal Pack | A Pal identity and its no-code knowledge, skills, workflows, memory rules, output contract, and verification behavior. |

Org Packs and FDE Packs can inform a Delivery Pack. The Delivery Pack describes how one real business goal should be delivered. PalSmith uses the Faye Build Request to create or complete Pal Packs when approved.

## Faye And PalSmith

Faye owns the delivery question:

```text
How should this business goal be delivered?
```

PalSmith owns the Pal creation question:

```text
How should the required Pals be created, completed, reviewed, or upgraded?
```

Faye may recommend candidate Pal perspectives and Pal Skill needs, but those recommendations are AI judgement inputs only. They are not central roster changes, keyword routes, hard assignments, or deterministic dispatch.

## Delivery Pack Structure

Delivery Packs stay intentionally simple:

```text
Project
  -> Flow Pack
  -> Task Package
```

The required Delivery Pack surface is:

```text
DELIVERY.md
PROJECT.md
FLOWS/
TASKS/
PAL_TEAM.md
FAYE_BUILD_REQUEST.md
INTEGRATIONS/
ACCEPTANCE.md
TRAINING.md
REPORTS/
delivery-pack.json
```

## Near-Runnable Examples

R132 adds two public-safe near-runnable Delivery Pack examples:

- `examples/delivery-packs/video-growth-delivery-pack/`
- `examples/delivery-packs/sales-crm-delivery-pack/`

The video growth example demonstrates research, scripting, brand review, video QA, publishing review, and first task packages for product-video workflows.

The sales CRM example demonstrates lead import, customer segmentation, follow-up copy, sales reminder cadence, deal review, and first task packages for sales operations workflows.

Both examples use fictional or placeholder data only. Customer-private data belongs in private project records, not reusable public examples.

## Deep Conductor Governance Loop

For Delivery Packs, Deep Conductor remains a no-code protocol set:

- task judgement;
- missing-information handling;
- assumptions;
- Context Access List;
- workflow topology;
- Task Package;
- verification result;
- governance record;
- routing-memory candidate;
- reusable/private review.

It is not a runtime engine, scheduler, scanner, connector, automatic executor, or keyword router.

## Thin Binding Boundary

External projects remain thin-bound. AgentPal should not copy Faye, Delivery Pack, Org Pack, FDE Pack, Pal Pack, memory, report, governance, or capability records into an external project's `.agentpal/` directory by default.

Project-private evidence belongs in approved private project records or approved customer-private stores.

## Current Review Gate

R133 integrates R132-A/B/C/D shared navigation. R134 should review whether the chain truly works from:

```text
user raw request
-> missing information
-> assumptions
-> Delivery Pack
-> Pal Team Blueprint
-> Faye Build Request
-> PalSmith Build Request
-> first Task Package
-> governance loop
```

R134 should not add new cases or perform remote publication unless separately authorized.
