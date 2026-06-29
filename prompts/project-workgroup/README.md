# Project Workgroup Prompts

Project workgroup prompts connect or remove AgentPal from an external user project.

## Project-First Prompts

- Claude Code: `../claude-code/install-agentpal-current-project.md`
- Generic CLI Agent: `../generic-cli-agent/install-agentpal-current-project.md`

## AgentPal-Led Prompts

- `../join-external-project-workgroup.md`
- `../remove-agentpal-workgroup.md`

## Boundary

Project means the external user project, not the AgentPal Workspace. The external project remains the active project root. AgentPal is only a Pal source and routing reference.

Project workgroups must use thin binding only. By default the external project may receive `.agentpal/project.json`, `.agentpal/AGENTPAL.md`, and protected `AGENTS.md` / `CLAUDE.md` blocks when the selected host needs them. Do not copy Pal Packs, Pal assets, memory, knowledge, workflows, reports, governance records, official Pal directories, examples, evals, or release files into the external project.

Project-private and customer-private material belongs in the correct private boundary. Do not write real customer data into public examples or reusable Pal Packs.

Deep Conductor in AgentPal v0.5 is a no-code collaboration and mode-decision protocol. It may help judge candidate workflow shapes, but project workgroup prompts must not claim automatic subagent execution, external Agent execution, scanners, connectors, installers, runtime services, or remote publication.
