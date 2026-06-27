# Non-Verifiable Business System Fields

Some Business System Profile fields cannot be verified by AgentPal itself. AgentPal is a Markdown / JSON / protocol workspace, not a connector, scanner, validator, browser session, admin console, or external system API client.

## Common Non-Verifiable Fields

These fields usually remain `unknown`, `not-run`, or `missing` until the user or host Runtime provides evidence:

- access
- write permission
- admin permission
- API availability
- export permission
- billing or plan capability
- user role
- workspace, tenant, organization, or account ID
- database, page, contact, deal, ticket, pipeline, or record visibility
- integration status
- business workflow ownership
- allowed output destination
- customer-data handling permission

Do not infer these fields from a product name such as Notion, CRM, Feishu, Jira, Linear, WordPress, OA, ERP, or GitHub.

## Accepted Evidence Sources

Use public-safe evidence from one of these sources:

- user confirmation
- current host Runtime evidence from an explicitly approved task
- business system UI confirmation provided by the user
- screenshot provided by the user
- exported report
- documented admin setting
- system log or audit record provided by the user
- task report that records the exact check, scope, result, and date

If the evidence is private, store only a public-safe summary in release files. Real project-specific records belong in central private project records under `workspace/projects/<project-id>/`.

## Evidence State Rules

Use these distinctions:

```text
Not verified != false
Not run != pass
Unknown != available
Missing evidence != acceptable completion
```

Required handling:

- If a fact is not confirmed, write `unknown`.
- If a check did not execute, write `not-run`.
- If evidence is required but absent, write `missing`.
- If a field is task-specific, require explicit user approval and current host Runtime evidence before claiming it.

## Forbidden Conversions

Do not convert:

- `availability: unknown` into `available: true`
- `write_access: unknown` into `write_access: true`
- `api_access: unknown` into `api_access: true`
- `permission_check: not-run` into `permission_check: pass`
- `verification_evidence: missing` into `verification: complete`
- `system_type: crm` into a route to a sales, operations, or product Pal
- `system_type: notion` into a route to a documentation Pal

Business System Profiles may inform AI judgement. They must not become keyword maps, deterministic semantic routes, connectors, API clients, automatic scans, background sync jobs, or automatic execution paths.

## Reporting Pattern

When evidence is incomplete, report it directly:

```text
availability: unknown
write_access: unknown
api_access: unknown
permission_check: not-run
verification_evidence: missing
next_step: ask the user for confirmation or run a user-approved host Runtime check
```

This is a valid profile state. It is better than pretending the system is connected, writable, or verified.
