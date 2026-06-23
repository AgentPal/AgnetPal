# Current Status

AgentPal v0.1.0-rc.1 is a release candidate for the AgentPal Workspace and Pal Pack standard practice for agent runtimes.

## Release Snapshot

- Version: `v0.1.0-rc.1`
- Release status: release candidate
- Current active path: `Simple Pal Mode only`
- Default Main Pal / Leader / Conductor: `Mira`
- Official bundled Pals: `Mira`, `Atlas`, `Vega`, `Rhea`, `Quinn`, `Morgan`, `Harper`, `Nova`

## What Is Active In This Release

- AgentPal Workspace root files for runtime initialization.
- Pal Packs under `pals/`.
- Mira as the default entry Pal.
- `/pal Name` direct calls through contacts and registry.
- Fast Route for clear owner-Pal handoff.
- Task Package, Context Slicing, and Asset Loading Budget protocols.
- Codex path, Claude Code project-first path, and generic CLI compatibility path.

## What Is Not Active In This Release

- Agent runtime execution owned by AgentPal.
- Multi-agent runtime behavior.
- Subagent Mode.
- Parallel child workflows.
- Deep Conductor as an active runtime path.
- External Agent orchestration.
- Desktop app, web app, marketplace, installer, daemon, scanner, validator, or hosted service.

## Runtime Boundary

AgentPal is a Pal layer. The host runtime reads files, writes files, runs commands, calls tools, and provides evidence when it claims an action happened.

## Related

- [What Is AgentPal](00-what-is-agentpal.md)
- [Current Capabilities](02-current-capabilities.md)
- [What AgentPal Is Not](04-what-agentpal-is-not.md)
- [Release Candidate Summary](05-release-candidate-summary.md)
