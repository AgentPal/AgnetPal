# R119-A Org Pack Practical Structure Boundary

Date: 2026-06-28

## Purpose

This eval checks that R119-A adds a practical Org Pack v0.5 standard, template,
and public-safe example without changing shared entries, central contacts, or
official Pal assets.

## Pass Criteria

- `standards/org-pack/org-pack-practical-structure.md` exists.
- Practical template files exist:
  - `templates/org-pack/practical-org-pack/README.md`
  - `templates/org-pack/practical-org-pack/ORG.md`
  - `templates/org-pack/practical-org-pack/org.json`
  - `templates/org-pack/practical-org-pack/roles/README.md`
  - `templates/org-pack/practical-org-pack/workflows/README.md`
  - `templates/org-pack/practical-org-pack/runbooks/README.md`
  - `templates/org-pack/practical-org-pack/governance/README.md`
  - `templates/org-pack/practical-org-pack/capability-inventory/README.md`
  - `templates/org-pack/practical-org-pack/verification/README.md`
  - `templates/org-pack/practical-org-pack/private-boundary.md`
- Public-safe content ops example files exist:
  - `examples/org-packs/content-ops-org-pack/README.md`
  - `examples/org-packs/content-ops-org-pack/ORG.md`
  - `examples/org-packs/content-ops-org-pack/org.json`
  - `examples/org-packs/content-ops-org-pack/recommended-pals.md`
  - `examples/org-packs/content-ops-org-pack/workflow-map.md`
  - `examples/org-packs/content-ops-org-pack/private-boundary.md`
- Template and example `org.json` parse.
- Template and example `org.json` set these fields to `false`:
  - `external_projects_copy_assets_by_default`
  - `can_modify_central_roster`
  - `keyword_routing_allowed`
  - `credentials_allowed`
  - `connector_included`
  - `marketplace_program_included`
- Recommended Pals are AI judgement inputs only.
- No central roster copy is introduced.
- No external project `.agentpal/org-pack` write is required or created.
- No keyword routing, deterministic semantic routing, route map, domain map, or
  role map is introduced.
- No connector, scanner, validator program, installer, marketplace, hub,
  daemon, database, auto-sync, or auto-execution behavior is introduced.
- No credentials, tokens, cookies, passwords, API keys, secrets, customer data,
  private project memory, private reports, or customer-private evidence are
  introduced.
- `private-boundary.md` exists in template and example.
- `README.md`, `README.zh-CN.md`, `RESOURCE_INDEX.md`, `agentpal.json`,
  `workspace/organization/contacts/**`, and `official/pals/**` are unchanged.
- Clean-copy validation passes.

## Fail Conditions

- Required standard, template, example, eval, validation, or integration-note
  files are missing.
- Any shared entry, central contact, or official Pal file changes.
- `org.json` fails to parse.
- Required false safety flags are missing or true.
- The example contains real customer data or credentials.
- Recommended Pals become hard routes or fixed assignments.
- Any connector, scanner, validator, installer, marketplace, hub, auto-sync, or
  auto-execution behavior is introduced.

## Required Evidence

Record evidence in:

- `release/fresh-clone-checks/r119a-local-org-pack-practical-structure-validation.md`
- `release/integration-notes/r119a-index-update-notes.md`
