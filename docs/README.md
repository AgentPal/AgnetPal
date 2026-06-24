# AgentPal Documentation

This documentation set is the public entry point for AgentPal v0.1.0-rc.1.

AgentPal is a Pal layer and Pal Pack Standard practice for Markdown/JSON-capable agent runtimes. It is not an Agent layer, not a multi-agent runtime, and not an execution layer.

## Start Here

- [What is AgentPal?](00-overview/00-what-is-agentpal.md)
- [Current status](00-overview/01-current-status.md)
- [Repository map](00-overview/02-repository-map.md)
- [Why Pal?](01-concepts/07-why-pal.md)
- [Quick start](02-getting-started/00-quick-start.md)
- [Use AgentPal with Claude Code](10-using-agentpal-with-claude-code.md)
- [Use AgentPal with generic CLI agents](11-using-agentpal-with-cli-agents.md)
- [Simple Pal Mode](01-concepts/05-simple-pal-mode.md)
- [Pal Pack Standard](03-pal-pack-standard/README.md)
- [Author your own Pal](07-authoring-pals/README.md)
- [Orchestration methodology](05-orchestration-methodology/README.md)
- [Pal Teams and Deep Conductor](05-orchestration-methodology/11-pal-teams-and-deep-conductor.md)
- [Validation and evidence](06-validation-and-evidence/README.md)
- [v0.1.0-rc.1 release candidate](08-release-candidate/README.md)

## Documentation Map

| Area | Use it for |
| --- | --- |
| [00-overview](00-overview/00-what-is-agentpal.md) | Product definition, current status, repository map, and runtime boundary |
| [01-concepts](01-concepts/01-what-is-a-pal.md) | Pal, Pal Pack, Skill, Agent, Why Pal, Pal Team, and Simple Pal Mode concepts |
| [02-getting-started](02-getting-started/00-quick-start.md) | Opening AgentPal, initializing Mira, and calling a Pal |
| [03-pal-pack-standard](03-pal-pack-standard/README.md) | Pal Pack structure, root files, public/private boundary, and checklist |
| [04-runtime-guides](04-runtime-guides/00-runtime-compatibility.md) | Runtime compatibility, Codex, Claude Code, and future adapters |
| [05-orchestration-methodology](05-orchestration-methodology/README.md) | Fast Route, Task Package, Context Slicing, Asset Loading Budget, Pal Teams, evidence records, and future orchestration boundaries |
| [06-collaboration](06-collaboration/00-collaboration-overview.md) | Contacts, mention protocol, Context Packets, handoff, and project workgroups |
| [06-validation-and-evidence](06-validation-and-evidence/README.md) | PalBench meaning, limits, observed benefits, and future validation design |
| [07-authoring-pals](07-authoring-pals/README.md) | Designing, writing, testing, and publishing Pal Packs |
| [07-memory-and-learning](07-memory-and-learning/00-memory-overview.md) | User memory, project memory, skill memory, and repeated-task learning |
| [08-release-and-maintenance](08-release-and-maintenance/00-release-process.md) | Release process, public-safety checks, versioning, and maintenance |
| [08-release-candidate](08-release-candidate/README.md) | v0.1.0-rc.1 scope, manifest, public-safe audit summary, tag process, and known limitations |
| [research](research/README.md) | Archived research notes only; not a primary docs entry point |
| [99-reference](99-reference/glossary.md) | Glossary, file index, official Pals, FAQ, and known limitations |

## Current v0.1.0-rc.1 Boundary

- Simple Pal Mode is the only active task-handling path.
- Mira is the default Main Pal, Leader Pal, and Conductor.
- `/pal Name` calls a registered Pal by display name or alias.
- `contacts/` and `registry/` are the source of truth for Pal discovery.
- AgentPal does not execute actions by itself; the host runtime performs file reads, writes, commands, tool calls, publishing, and deletion.
- Future child workflow or subagent design material is not active in v0.1.0-rc.1.
- Research and orchestration methodology docs are design foundations. They do not enable Deep Conductor, external Agent calls, or Subagent Mode in v0.1.0-rc.1.

## Public-Safe Rule

Do not publish private user memory, private project state, real task reports, internal development notes, secrets, credentials, local absolute paths, customer data, or unauthorized third-party full text.

See [public/private boundary](03-pal-pack-standard/11-public-private-boundary.md) and [public-safe checklist](08-release-and-maintenance/02-public-safe-checklist.md).
