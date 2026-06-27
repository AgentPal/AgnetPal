# Workspace Projects

This directory holds central AgentPal records for external user projects.

Default public repository content should include only templates, examples, and empty indexes. Real user project records are workspace-private and should not be committed.

External projects should contain thin binding files only. Project memory, source maps, derived knowledge, governance notes, task packages, reports, and capability inventory records belong here when they are maintained centrally.

Project-level capability inventory templates live under `_template/capability-inventory/`. Real project capability records live under `workspace/projects/<project-id>/capability-inventory/`, may reference organization records from `workspace/organization/capability-inventory/`, and are private by default.

Public-safe examples of central project records live outside this private area under `examples/project-records/`. For Business System profile references, see `examples/project-records/business-system-profile-references/`.

Default public files:

- `README.md`
- `projects.index.json`
- `_template/`

Real records use:

`workspace/projects/<project-id>/`

The external project remains the source of current project files. AgentPal reads the external project when needed, then stores structured summaries and project memory in the central record.

Project usage memory belongs to one project. It may suggest a future organization-level review, but it must not silently update organization capability profiles, central Pal contacts, or no-keyword-routing policy.
