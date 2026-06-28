# Sales CRM Delivery Pack

## Delivery Goal

Help a fictional B2B sales team organize leads, classify customer priority, draft follow-up messages, plan reminder cadence, and review deal progress through a no-code AI team workflow.

This pack is designed by Faye as a Delivery Pack blueprint and can be handed to PalSmith as a Pal team build request.

## What This Pack Proves

Faye can work beyond content operations. A sales CRM Delivery Pack can express:

- lead intake from a manually provided export summary;
- customer segmentation logic;
- follow-up copy variants;
- sales reminder cadence;
- deal review and next-step planning;
- human review and compliance boundaries;
- customer-private storage rules.

## Faye Review Chain

### Raw User Request

A fictional B2B sales team asks Faye to help organize lead summaries, classify customer priority, draft follow-up messages, plan reminder cadence, and review deal progress without connecting to the team's real CRM.

### Missing Information

- real CRM field list: `missing`;
- approved sales voice examples: `missing`;
- compliance review owner: `missing`;
- current sales-stage definitions: `missing`;
- real lead evidence: blocked from reusable pack;
- CRM access and credentials: blocked from reusable pack;
- automatic reminder execution: `not-run`.

### Assumptions

- use fictional lead placeholders only;
- keep all CRM data de-identified and public-safe;
- treat integrations as manual handoff profiles;
- require human review for customer-facing copy;
- keep candidate Pals as AI judgement inputs, not route rules.

### Delivery Chain

```text
raw user request
-> missing information
-> assumptions
-> Delivery Pack
-> Pal Team Blueprint
-> Faye Build Request
-> PalSmith Build Request
-> first task package
-> acceptance and report placeholders
```

This chain is no-code. It does not authorize connector execution, external project writes, central roster mutation, official Pal edits, or customer-private storage in reusable examples.

## Operating Model

The pack uses the simple structure:

```text
Project
  -> Flow Pack
  -> Task Package
```

Faye owns delivery design. PalSmith owns Pal team creation or Pal Pack upgrade work when explicitly approved. Candidate Pals provide judgement perspectives only after the Brain / AI reads current context and central roster.

## Non-goals

This pack does not:

- connect to a CRM;
- call external APIs;
- import real CRM files;
- send messages;
- schedule reminders automatically;
- store customer-private data;
- create a scanner, validator, connector, app, marketplace, or execution engine;
- change central contacts;
- copy Pal assets into an external project.

## Required Human Review

Sales copy, customer segmentation criteria, compliance risk, and any customer-facing message require human review before use.

`not-run` is not `pass`.
