# Project Usage Memory Boundary

Project usage memory records what happened in one project.

It is not organization truth.

It may suggest a future organization-level review.

It must not silently update organization capability profiles.

It must not update the central Pal roster.

It must not update no-keyword-routing policy.

It must not be copied into external project `.agentpal/` by default.

## Correct Use

Project usage memory can record project-specific evidence such as:

- a check that was not run
- a missing confirmation
- a host Runtime result for one project
- a project-specific limitation
- a recommendation to review an organization profile later

It cannot certify global access, global write permission, global API access, or central Pal ownership.

## Example

Good:

```text
In content-ops-demo, Notion write permission check was not-run.
```

Bad:

```text
Therefore Notion write access is available globally.
```

Correct:

```text
Record project-level not-run. If user later confirms access, propose an organization profile review.
```

## Boundary Checklist

- Keep project usage memory under the central project record.
- Keep external project `.agentpal/` thin by default.
- Do not update `workspace/organization/contacts/pals.json`.
- Do not update `workspace/organization/capability-inventory/` without explicit review.
- Do not convert `unknown`, `not-run`, or `missing` into a pass.
- Do not use project usage memory as `keyword_map`, `domain_map`, `role_map`, or deterministic routing.

