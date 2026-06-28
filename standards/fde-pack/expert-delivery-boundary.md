# Expert Delivery Boundary

Date: 2026-06-28

## Purpose

This boundary explains what an FDE / Expert Delivery Pack can and cannot do.

An FDE Pack captures expert delivery knowledge as no-code assets. It does not perform the expert service by itself and does not replace professional judgement.

## Allowed

An FDE Pack may provide:

- delivery scope;
- expert profile;
- reusable public-safe checklists;
- reusable public-safe templates;
- process notes;
- judgement criteria;
- review questions;
- verification checklists;
- update policies;
- Pal, workflow, runbook, Org Pack, or Capability Inventory recommendations as AI judgement inputs.

## Not Allowed

An FDE Pack must not:

- execute work;
- call APIs;
- connect to customer systems;
- scan files or systems;
- validate live systems automatically;
- store credentials;
- store customer-private data;
- create a marketplace or hub program;
- install tools;
- modify central contacts;
- route by keyword;
- copy assets into external project `.agentpal/` by default.

## Expert Review Boundary

The pack can organize expert work, but the expert or approved reviewer remains responsible for final high-risk decisions.

For medical, legal, tax, accounting, financial, compliance, employment, insurance, safety, or regulated domains:

- require qualified human review;
- record jurisdiction or applicability limits where relevant;
- record source freshness;
- keep customer-specific facts in private records;
- treat missing or stale evidence as `requires-human-review`.

## Reusable vs Customer-Private Boundary

Reusable pack assets must be public-safe.

Customer-private details belong in private records, not in reusable pack files. When in doubt, mark content `private` or `requires-review` and keep it out of public examples.

## Routing Boundary

FDE Pack recommendations are AI judgement inputs only. They are not:

- hard routes;
- keyword routes;
- Pal assignments;
- task-domain route maps;
- automatic dispatch rules.

The current Brain / AI must judge ownership from the user request, central roster, project context, Org Pack, FDE Pack, Capability Inventory, Pal assets, risk, and evidence needs.
