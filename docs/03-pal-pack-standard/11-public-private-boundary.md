# Public And Private Boundary

AgentPal public repositories should contain only release-safe Markdown, JSON, templates, protocols, examples, evals, and placeholders.

## Do Not Publish

- API keys, tokens, passwords, secrets, credentials, or private keys.
- Private user memory.
- Real user conversation history.
- Private project state.
- Customer data.
- Proprietary project data.
- Real task reports, verification reports, or internal development reports.
- Local absolute paths.
- Unauthorized third-party full text.
- Unlicensed source code or documentation copied from another project.
- Future feature claims written as current behavior.

## Public-Safe Content

Allowed public content includes:

- Pal Pack templates.
- Synthetic examples.
- Public-safe evals.
- Placeholder README files for memory, state, and reports.
- Protocol docs.
- Release notes and checklists.
- Short attributed references or links to third-party resources.

## Directory Watchlist

Review these carefully before release:

- `memory/`
- `state/`
- `reports/`
- `pals/*/memory/`
- `pals/*/state/`
- `pals/*/reports/`
- `examples/`
- `evals/`
- `imports/`
- `docs/`

## Future Design Boundary

Future child workflow, subagent, marketplace, desktop app, and runtime-adapter materials must be marked as future or not active in v0.1.0-rc.1.

## Related

- [Public-safe checklist](../08-release-and-maintenance/02-public-safe-checklist.md)
- [Third-party notices](../../THIRD_PARTY_NOTICES.md)
- [Release checklist](../../RELEASE_CHECKLIST.md)
