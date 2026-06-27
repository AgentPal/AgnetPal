# Capability Inventory Navigation

Capability Inventory is AgentPal's no-code profile layer for runtime, model, reasoning, Skill, plugin, MCP, business-system, and Pal capability notes.

It is not an automatic scanner, validator, installer, sync service, or keyword router. A host Runtime may provide evidence, and AgentPal records that evidence as Markdown / JSON assets.

## Current Sources

| Source type | Path | Role |
| --- | --- | --- |
| Standards | `standards/capability-inventory/` | Reusable rules, matrices, protocols, and profile standards. |
| Current organization records | `workspace/organization/capability-inventory/` | Public-safe current organization placeholders and maintained capability notes. |
| Examples | `examples/capability-inventory/` | Synthetic example profiles and task judgement examples, including public-safe Business System examples. |
| Templates | `templates/capability-inventory/` | Copyable JSON profile templates, including `business-system-profile-template.json`. |
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

The external project should keep only binding entrypoints such as `.agentpal/project.json`, `.agentpal/AGENTPAL.md`, and protected root instruction blocks. It should not receive `.agentpal/capability-inventory/` or `.agentpal/business-systems/` by default.

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

## Legacy Path Notes

R79 archived the old root `capabilities/`, `runtime/`, `models/`, and `plugins/` pointer directories under:

```text
archive/migration-from-v0.3/root-legacy/capability-inventory/root-pointers/
```

R80 renamed the old template tree from `templates/capabilities/` to `templates/capability-inventory/` and moved the old `examples/runtime/README.md` navigation into `examples/runtime-adapters/README.md`.
