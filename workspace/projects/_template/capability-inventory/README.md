# Capability Inventory

This directory is the project-level Capability Inventory template.

Use it when creating a central project record under:

```text
workspace/projects/<project-id>/capability-inventory/
```

## Relationship To Organization Records

Organization capability inventory:

```text
workspace/organization/capability-inventory/
```

Project capability inventory:

```text
workspace/projects/<project-id>/capability-inventory/
```

External project binding:

```text
<project>/.agentpal/project.json
```

Organization records describe public-safe capabilities that can apply across the AgentPal organization. Project records describe capabilities that are available, used, limited, or relevant for one bound project.

Project records may reference organization records. Project records may supplement organization records for that project, such as when a project uses a restricted plugin, a customer-specific business system, or a different Runtime setup.

Project records should describe only project-scope availability, limits, business-system constraints, task usage experience, and verification notes. They do not replace organization-level records.

Project records must not modify the central Pal roster. Pal contacts remain under:

```text
workspace/organization/contacts/
```

## Boundary

The external user project should not receive a default `.agentpal/capability-inventory/` or `.agentpal/business-systems/` directory.

Real project records under `workspace/projects/<project-id>/` are private by default and ignored unless explicitly promoted as public-safe examples.

This is a no-code record. It does not imply automatic scanning, automatic discovery, automatic execution, automatic scoring, connector setup, API client setup, background sync, release automation, or keyword routing.

Do not store credentials, private tokens, API keys, session cookies, or project secrets here.

Unknown or unconfirmed fields must stay `unknown`, `not-run`, `not-confirmed`, or empty until the user or current host Runtime provides evidence.

Project usage memory records what happened in one project. It is not organization truth, and it must not silently update organization capability profiles, central Pal contacts, or no-keyword-routing policy. Public-safe examples of this relationship live under `examples/project-records/business-system-profile-references/`.

## Recommended Fields

Use these fields when adding or updating project-level capability records:

| Field | Meaning |
| --- | --- |
| `profile_id` | Project-local capability record id. |
| `profile_type` | Runtime, model, reasoning, Skill, plugin, MCP, business-system, or Pal capability. |
| `organization_profile_ref` | Optional reference to an organization-level record. |
| `project_scope` | Bound project, environment, customer, workflow, or task scope where this record applies. |
| `source` | User confirmation, current file evidence, current host Runtime evidence, or `unknown`. |
| `confidence` | `high`, `medium`, `low`, or `unknown`. |
| `last_updated` | Last update date or `unknown`. |
| `confirmed_by` | User, maintainer, host Runtime evidence, or `unknown`. |
| `status` | Available, limited, unavailable, not-run, not-confirmed, or `unknown`. |
| `project_available` | Whether the capability is confirmed available for this project. |
| `project_limitations` | Project-specific limits, exclusions, permissions, or business constraints. |
| `privacy_boundary` | What project data may or may not be recorded. |
| `credential_policy` | Explicit no-credentials rule for tokens, passwords, API keys, cookies, and secrets. |
| `verification_notes` | Evidence needed, evidence seen, and what was not verified. |
| `usage_memory` | Project-specific successes, failures, recommendations, and not-run notes. |
| `project_override_policy` | How this project supplements organization records without modifying central contacts or global facts. |
| `unknown_fields` | Fields intentionally left unknown until confirmed. |
