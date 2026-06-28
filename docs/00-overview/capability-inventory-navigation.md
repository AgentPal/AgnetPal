# Capability Inventory Navigation

Capability Inventory is AgentPal's no-code profile layer for runtime, model, reasoning, Skill, plugin, MCP, business-system, and Pal capability notes.

It is not an automatic scanner, validator, installer, sync service, or keyword router. A host Runtime may provide evidence, and AgentPal records that evidence as Markdown / JSON assets.

## Current Sources

| Source type | Path | Role |
| --- | --- | --- |
| Standards | `standards/capability-inventory/` | Reusable rules, matrices, protocols, profile standards, Business System review flow, manual update evidence pack rules, manual writeback replay record rules, audit trail index rules, governance decision record rules, and change ledger rules. |
| Current organization records | `workspace/organization/capability-inventory/` | Public-safe current organization placeholders and maintained capability notes. |
| Examples | `examples/capability-inventory/` | Synthetic example profiles and task judgement examples, including public-safe Business System examples and review examples. |
| Templates | `templates/capability-inventory/` | Copyable profile templates, including `business-system-profile-template.json`, `business-system-profile-review-packet.md`, `business-system-profile-manual-update-evidence-pack.md`, `business-system-profile-manual-writeback-replay-record.md`, `business-system-profile-audit-trail-index.md`, `business-system-profile-governance-decision-record.md`, and `business-system-profile-change-ledger.md`. |
| Project record template | `workspace/projects/_template/capability-inventory/` | Template for per-project capability records under central project records. |
| Historical archive | `archive/migration-from-v0.3/root-legacy/capability-inventory/` | R78/R79/R80 migration evidence and archived legacy pointers. |

## Manual Profile Updates

Use `docs/03-user-guides/manual-capability-profile.md` when adding or updating a profile.

Manual profile rules:

- choose the profile type before writing
- copy a template from `templates/capability-inventory/`
- fill only confirmed information
- mark unconfirmed fields as `unknown`
- record source and confidence
- include limitations and not-run notes
- do not store credentials, private tokens, API keys, or secrets
- do not copy profile records into external user projects by default
- use Business System profiles only as external system governance inputs, not connectors or automatic write access

## Business System Profiles

Use `standards/capability-inventory/business-system-profile-standard.md` for the Business System profile rules. Use `templates/capability-inventory/business-system-profile-template.json` as the reusable JSON shape and `examples/capability-inventory/business-system-profiles/` for public-safe examples.

Business System records can describe GitHub, Feishu, Notion, CRM, Jira, Linear, OA, ERP, databases, and customer-specific tools, but only as governance notes and AI judgement inputs. They are not connectors, API clients, credential stores, permission grants, automatic scanners, background sync jobs, release tools, write access, or keyword routes.

Use `standards/capability-inventory/business-system-profile-review-flow.md` and `templates/capability-inventory/business-system-profile-review-packet.md` when project usage memory suggests an organization-level profile review. Review packets can recommend manual updates, but they must not auto-update organization truth, modify central Pal contacts, write into external project `.agentpal/reviews/`, create connectors, store credentials, or keyword route.

Use `standards/capability-inventory/business-system-profile-manual-update-evidence-pack.md` and `templates/capability-inventory/business-system-profile-manual-update-evidence-pack.md` after a review packet is approved for manual update. Evidence packs record the proposed manual change, user confirmation, host Runtime evidence, rollback note, writeback target, and second verification status. They still must not perform automatic writeback, modify central contacts, write into external project `.agentpal/evidence/`, create connectors, store credentials, or keyword route.

Use `standards/capability-inventory/business-system-profile-manual-writeback-replay-record.md` and `templates/capability-inventory/business-system-profile-manual-writeback-replay-record.md` after a manual writeback has happened. Replay records audit changed fields, previous and updated snapshots, rollback record, and second verification result. They still must not execute writeback, auto-rollback, modify central contacts, write into external project `.agentpal/replay/`, `.agentpal/rollback/`, or `.agentpal/verification/`, create connectors, store credentials, or keyword route.

Use `standards/capability-inventory/business-system-profile-audit-trail-index.md` and `templates/capability-inventory/business-system-profile-audit-trail-index.md` when several review, evidence, replay, rollback, or second verification records need an organization-level summary. Audit trail indexes summarize paths, statuses, open unknowns, not-run checks, missing evidence, risks, and next manual action suggestions. They still must not execute actions, auto-call external APIs, auto-close missing evidence, modify central contacts, write into external project `.agentpal/audit-trail/`, create connectors, store credentials, or keyword route.

Use `standards/capability-inventory/business-system-profile-governance-decision-record.md` and `templates/capability-inventory/business-system-profile-governance-decision-record.md` after review, evidence, replay, and audit trail review when a human governance decision must be recorded. Governance decision records can approve a bounded manual profile update, reject it, block it for missing evidence, require user confirmation, require host Runtime evidence, require second verification, or supersede an earlier decision. They still must not execute writeback, auto-close missing evidence, convert not-run to pass, modify central contacts, write into external project `.agentpal/governance-decisions/`, create connectors, store credentials, or keyword route.

Use `standards/capability-inventory/business-system-profile-change-ledger.md` and `templates/capability-inventory/business-system-profile-change-ledger.md` after governance decision and manual change review when field-level Business System Profile changes need a human-governed ledger. Change ledgers record old/new public-safe summaries, source decision, evidence, replay, audit trail, rollback reference, second verification status, superseded entries, retained unknowns, retained not-run checks, retained missing evidence, and next manual review date. They still must not execute writeback, auto-update organization truth, auto-call external APIs, auto-close missing evidence, convert not-run to pass, modify central contacts, write into external project `.agentpal/change-ledger/`, create connectors, store credentials, schedule automatic tasks, or keyword route.

Current Business System examples:

- `examples/capability-inventory/business-system-profiles/manual-github-profile-walkthrough.md`
- `examples/capability-inventory/business-system-profiles/manual-notion-profile-walkthrough.md`
- `examples/capability-inventory/business-system-profiles/github-project-record-reference.example.md`
- `examples/capability-inventory/business-system-profiles/unknown-not-run-missing-examples.md`
- `examples/capability-inventory/business-system-profiles/non-verifiable-business-system-fields.md`
- `examples/capability-inventory/business-system-profiles/github-public-governance-profile.example.json`
- `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json`
- `examples/capability-inventory/business-system-profiles/generic-crm-public-governance-profile.example.json`
- `examples/failures/business-system-profile-as-connector.md`

Public-safe central project record reference examples live under:

```text
examples/project-records/business-system-profile-references/
```

These examples show how `content-ops-demo` and `sales-ops-demo` reference organization Business System profile examples without becoming real private `workspace/projects/<project-id>` records.

Public-safe review flow examples live under:

```text
examples/capability-inventory/business-system-profile-reviews/
```

They show review packets that preserve `unknown`, `not-run`, and `missing` until user confirmation and reviewable host Runtime evidence are available.

The manual update evidence example lives at:

```text
examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-update-evidence.example.md
```

It shows an approved-review premise and keeps second verification as `second_verification_not_run` until manual writeback and verification actually run.

The manual writeback replay example lives at:

```text
examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-writeback-replay.example.md
```

It shows a completed manual writeback premise while keeping second verification as `second_verification_not_run` because no real writeback or verification ran in the example.

The audit trail index example lives at:

```text
examples/capability-inventory/business-system-profile-reviews/notion-read-access-audit-trail-index.example.md
```

It summarizes the public-safe Notion read access review, evidence pack, replay record, rollback summary, second verification status, open unknowns, missing evidence, and next manual action suggestions without executing actions or modifying organization truth.

The governance decision example lives at:

```text
examples/capability-inventory/business-system-profile-reviews/notion-read-access-governance-decision.example.md
```

It records `needs_second_verification` and keeps `manual_update_allowed: false` while second verification evidence is missing, without executing actions or modifying organization truth.

The change ledger example lives at:

```text
examples/capability-inventory/business-system-profile-reviews/notion-read-access-change-ledger.example.md
```

It shows a public-safe field-level `read_access` change summary from `unknown` to `user_confirmed` as an example premise while keeping `second_verification_not_run`, retained unknowns, retained missing evidence, and no automatic action.

## External Project Boundary

External user projects remain thin-bound. Do not copy standards, examples, templates, Pal Packs, central contacts, memory, reports, workflows, capability inventory directories, or business-system directories into the external project by default.

Project-specific capability findings belong under:

```text
workspace/projects/<project-id>/capability-inventory/
```

The template for that central project record area is:

```text
workspace/projects/_template/capability-inventory/
```

The external project should keep only binding entrypoints such as `.agentpal/project.json`, `.agentpal/AGENTPAL.md`, and protected root instruction blocks. It should not receive `.agentpal/capability-inventory/`, `.agentpal/business-systems/`, `.agentpal/governance-decisions/`, or `.agentpal/change-ledger/` by default.

## Routing Boundary

Capability Inventory profiles can inform AI judgement. They must not become fixed routes.

Forbidden active behavior:

- `keyword_map`
- `domain_map`
- `role_map`
- deterministic task-domain-to-Pal routing
- automatic runtime selection without current evidence

Explicit `/pal Name` and `@Name` mentions are user intent signals, not keyword routes.

## Compliance Eval

The Manual Profile Guide compliance regression lives at:

```text
evals/palbench/capability-inventory/r82-manual-profile-guide-compliance.md
```

It checks the manual guide, Business System template, project record template, and metadata for no auto scan, no keyword routing, no credentials, unknown-stays-unknown, organization/project separation, and thin external project boundaries.

The Business System project relationship regression lives at:

```text
evals/palbench/capability-inventory/r83-project-record-relationship-boundary.md
```

It checks the Business System standard, public-safe GitHub example, organization/project record relationship, thin binding boundary, no connector, no credentials, and no keyword routing.

The Business System manual walkthrough regression lives at:

```text
evals/palbench/capability-inventory/r84-business-system-manual-walkthrough-boundary.md
```

It checks the manual walkthrough, project record reference, unknown / not-run / missing examples, forbidden failure example, no credentials, no connector, no automatic scanner, no keyword routing, and no external project pollution.

The non-GitHub Business System boundary regression lives at:

```text
evals/palbench/capability-inventory/r85-non-github-business-system-boundary.md
```

It checks the Notion example, CRM example, non-code walkthrough, non-verifiable fields note, no credentials, no connector, no automatic scanner, no keyword routing, unknown / not-run / missing preservation, and no external project pollution.

The project record Business System reference regression lives at:

```text
evals/palbench/capability-inventory/r86-project-record-business-system-reference-boundary.md
```

It checks the content-ops and sales-ops project record examples, project usage memory boundary, central roster boundary, no connector, no credentials, no automatic scanner, no keyword routing, and no external project pollution.

The Business System profile review flow regression lives at:

```text
evals/palbench/capability-inventory/r87-business-system-profile-review-flow-boundary.md
```

It checks the review flow standard, review packet template, public-safe review example, project usage memory upgrade boundary, central roster boundary, no connector, no credentials, no automatic scanner, no keyword routing, and no external project `.agentpal/reviews/` writes.

The Business System profile manual update evidence regression lives at:

```text
evals/palbench/capability-inventory/r88-business-system-profile-manual-update-evidence-boundary.md
```

It checks the manual update evidence standard, evidence pack template, public-safe evidence example, approved-review relationship, rollback note, second verification, central roster boundary, no connector, no credentials, no automatic scanner, no keyword routing, and no external project `.agentpal/evidence/` writes.

The Business System profile manual writeback replay regression lives at:

```text
evals/palbench/capability-inventory/r89-business-system-profile-manual-writeback-replay-boundary.md
```

It checks the replay record standard, replay template, public-safe replay example, manual update evidence relationship, rollback record, honest second verification, central roster boundary, no connector, no credentials, no automatic scanner, no keyword routing, and no external project `.agentpal/replay/`, `.agentpal/rollback/`, or `.agentpal/verification/` writes.

The Business System profile audit trail index regression lives at:

```text
evals/palbench/capability-inventory/r90-business-system-profile-audit-trail-index-boundary.md
```

It checks the audit trail standard, audit trail template, public-safe audit trail example, review / evidence / replay references, next manual action boundary, not-run and missing evidence preservation, central roster boundary, no connector, no credentials, no automatic scanner, no external API call, no keyword routing, and no external project `.agentpal/audit-trail/` writes.

The Business System profile governance decision regression lives at:

```text
evals/palbench/capability-inventory/r91-business-system-profile-governance-decision-boundary.md
```

It checks the governance decision standard, decision template, public-safe decision example, audit trail / review / evidence / replay references, `needs_second_verification` blocking manual update, unknown / not-run / missing preservation, central roster boundary, no connector, no credentials, no automatic scanner, no keyword routing, and no external project `.agentpal/governance-decisions/` writes.

The Business System profile change ledger regression lives at:

```text
evals/palbench/capability-inventory/r92-business-system-profile-change-ledger-boundary.md
```

It checks the change ledger standard, template, public-safe example, governance decision / evidence / replay / audit trail references, old/new summary honesty, second verification not-run preservation, missing evidence preservation, next review date as a manual note, central roster boundary, no connector, no credentials, no automatic scanner, no external API call, no keyword routing, and no external project `.agentpal/change-ledger/` writes.

## Legacy Path Notes

R79 archived the old root `capabilities/`, `runtime/`, `models/`, and `plugins/` pointer directories under:

```text
archive/migration-from-v0.3/root-legacy/capability-inventory/root-pointers/
```

R80 renamed the old template tree from `templates/capabilities/` to `templates/capability-inventory/` and moved the old `examples/runtime/README.md` navigation into `examples/runtime-adapters/README.md`.
