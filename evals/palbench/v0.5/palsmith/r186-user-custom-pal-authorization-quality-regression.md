# R186 User Custom Pal Authorization Quality Regression

date: 2026-06-30
workspace: `J:\开发\AgentPal`
owner: PalSmith
result: `pass`

## Reviewed Assets

- `official/pals/PalSmith-pal-governor/core/user-custom-pal-discovery-authorization-protocol.md`
- `docs/06-palsmith/user-custom-pal-discovery-authorization.md`
- `prompts/palsmith/authorize-user-custom-pal-discovery.md`
- `templates/palsmith/user-custom-pal-authorization-record.md`
- `templates/palsmith/user-custom-pal-discovery-policy.md`
- `evals/palbench/v0.5/palsmith/r185-user-custom-pal-discovery-authorization-design.md`
- `evals/palbench/v0.5/palsmith/r185-user-custom-pal-authorization-boundary-cases.md`
- `evals/palbench/v0.5/palsmith/r185-quinn-authorization-flow-review.md`

## Authorization Model Check

| Permission | Separated | Default |
| --- | --- | --- |
| discovery | pass | disabled |
| invocation | pass | disabled unless explicit user invocation is recorded |
| delegation | pass | disabled |
| contacts_registration | pass | disabled |
| marketplace_draft | pass | none or draft-only |
| marketplace_public_request | pass | disabled |

Checks:

- enabling discovery does not enable invocation: pass
- enabling invocation does not enable delegation: pass
- delegation requires named callers, task scope, expiry or review: pass
- contacts registration is separate: pass
- Marketplace draft is not public listing: pass
- user custom Pal remains non-official: pass

## Template Check

`templates/palsmith/user-custom-pal-authorization-record.md` includes the required fields:

- `pal_id`
- `pal_name`
- `pal_path`
- `pal_type`
- `authorization_status`
- `requested_by`
- `approved_by`
- `approved_at`
- `expires_at`
- `review_after`
- `scope.discovery`
- `scope.invocation`
- `scope.delegation`
- `scope.contacts_registration`
- `scope.marketplace`
- `allowed_callers`
- `allowed_tasks`
- `denied_tasks`
- `data_access`
- `memory_access`
- `revocation`
- `audit_notes`

Default safety:

- `authorization_status: proposed`
- `scope.discovery: false`
- `scope.invocation: false`
- `scope.delegation: false`
- `scope.contacts_registration: false`
- `scope.marketplace: none`
- `memory_access.default: minimal`
- `memory_access.private_memory_allowed: false`

## Prompt Check

`prompts/palsmith/authorize-user-custom-pal-discovery.md` covers:

- up to three focused questions;
- scope, caller, task, expiry, data, and memory boundary;
- refusal of all-Pal automatic use;
- Marketplace draft vs public request boundary;
- company contacts / organization-level policy separation;
- no write before explicit confirmation.

## Decision

R186 quality regression result: `pass`.
