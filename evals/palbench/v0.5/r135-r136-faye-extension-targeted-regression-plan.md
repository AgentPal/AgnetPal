# R135 / R136 Faye Extension Targeted Regression Plan

Status: planning record for R136 execution.

## Purpose

Run targeted regression over the Faye / Delivery Pack / Deep Conductor extension
that entered the v0.5 package after R130 local completion and R131 local release
preflight.

R136 should determine whether the extended v0.5 scope is ready for a refreshed
completion and preflight round.

## Scope

R136 covers:

- Faye / Delivery Pack standards and templates;
- video growth Delivery Pack chain;
- sales CRM Delivery Pack chain;
- Faye to PalSmith handoff;
- Deep Conductor governance loop;
- safety and boundary preservation;
- shared entry and navigation;
- baseline preservation for R130/R131 and the pre-existing v0.5 package.

## Out Of Scope

R136 must not:

- add new features, cases, business systems, connectors, scanners, validators,
  marketplace programs, installers, or runtime engines;
- create or modify official Pal contacts;
- add official Pals;
- add executable code;
- write to external project `.agentpal` directories;
- run push, pull, fetch, tag creation, GitHub Release creation, or remote
  publication.

## Test Groups

| Group | Name | Intent |
| --- | --- | --- |
| F1 | Faye / Delivery Pack Standards | Verify standards, base template, and base example are coherent and no-code. |
| F2 | Video Growth Delivery Pack Chain | Verify the video growth example is complete, public-safe, and standards-aligned. |
| F3 | Sales CRM Delivery Pack Chain | Verify the sales CRM example is complete, public-safe, and standards-aligned after R134 fix. |
| F4 | Faye -> PalSmith Handoff | Verify handoff artifacts preserve PalSmith review boundaries. |
| F5 | Deep Conductor Governance Loop | Verify no-code governance loop, Context Access List, templates, examples, and routing-memory record boundaries. |
| F6 | Boundary / Safety | Verify no runtime expansion, keyword routing, connectors, credentials, customer-private data, or remote-publication claim. |
| F7 | Shared Entry / Navigation | Verify README, README.zh-CN, RESOURCE_INDEX, and agentpal metadata surface the extension accurately. |
| F8 | Baseline Preservation | Verify R130/R131 status is preserved as pre-extension evidence and official roster/Pal files remain unchanged. |

## Pass Criteria

R136 passes only if:

- all required R132-R135 files exist;
- all visible JSON parses successfully;
- Delivery Pack JSON files parse successfully;
- routing-memory-record JSON parses successfully;
- `agentpal.json` parses successfully;
- central contacts parse successfully and still contain 9 registered / active
  official Pals;
- official Pal directory count remains 9;
- all official `pal.json` files parse successfully;
- official asset manifest count remains 1 and only PalSmith has it;
- `routing_policy` remains `ai_judgement_only`;
- `keyword_routing_allowed` remains false where applicable;
- central contacts and official Pal `pal.json` files are unchanged by R135/R136;
- no active route maps, connector program, scanner, validator, marketplace
  program, credential, customer-private asset, executable code, external
  project `.agentpal/delivery-pack`, or hidden remote-publication claim is
  introduced;
- clean-copy validation passes.

## Severity

| Severity | Meaning | R136 Action |
| --- | --- | --- |
| Blocker | Public package becomes unsafe, unparsable, or misleading. | Stop and require fix round. |
| High | Boundary or navigation failure could mislead users. | Fix before refreshed completion claim. |
| Medium | Important completeness or consistency issue. | Fix or explicitly defer before completion refresh. |
| Low | Minor wording or traceability issue. | May defer with note if public safety is unaffected. |
| Note | Observation only. | Record without blocking. |

## Expected Output

R136 should produce:

- targeted regression results;
- issue table;
- local validation record;
- readiness decision for refreshed v0.5 completion / preflight or a focused fix
  round.
