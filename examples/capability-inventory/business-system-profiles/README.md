# Business System Profile Examples

This directory contains public-safe Business System profile examples.

Examples are illustrative only. They are not active connectors, API clients, credentials, scans, permission grants, background sync jobs, release tools, or automatic execution paths.

Use them to understand profile shape and governance boundaries. Do not copy them into an external project's `.agentpal/` binding by default, and do not treat an example system type as a Pal, Runtime, Skill, plugin, MCP, or tool route.

Current examples:

| Example | Purpose |
| --- | --- |
| `github-public-governance-profile.example.json` | Public-safe GitHub governance example using placeholder repository `example-org/example-repo`. |
| `manual-github-profile-walkthrough.md` | End-to-end manual walkthrough from user-confirmed facts to organization profile draft and project record reference. |
| `github-project-record-reference.example.md` | Project-level reference example for a central project capability record. |
| `unknown-not-run-missing-examples.md` | Short examples showing the difference between `unknown`, `not-run`, and `missing`. |

Related sources:

- Standard: `standards/capability-inventory/business-system-profile-standard.md`
- Template: `templates/capability-inventory/business-system-profile-template.json`
- Manual guide: `docs/03-user-guides/manual-capability-profile.md`
- Project relationship eval: `evals/palbench/capability-inventory/r83-project-record-relationship-boundary.md`
- Walkthrough boundary eval: `evals/palbench/capability-inventory/r84-business-system-manual-walkthrough-boundary.md`
- Failure example: `examples/failures/business-system-profile-as-connector.md`
