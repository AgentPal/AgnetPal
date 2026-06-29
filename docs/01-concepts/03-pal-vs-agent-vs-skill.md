# Pal Vs Agent Vs Skill

AgentPal v0.5 keeps three ideas separate: Skill, Pal, and Agent.

## Short Definitions

| Concept | What it means | AgentPal boundary |
| --- | --- | --- |
| Skill | A capability package or reusable method | Can be owned by a Pal or provided by a host runtime |
| Pal | A working partner with identity, judgement, knowledge, Skills, memory rules, and output contracts | Stored as a Pal Pack and used by the current runtime |
| Agent | The execution runtime or process that can read files, call tools, run commands, or perform actions | External to AgentPal |
| Pal Team | Several Pals coordinating responsibility and review for one goal | No-code collaboration layer, not multiple running processes |
| Multi-Agent system | Several Agent processes or workers executing work | Runtime-layer capability, not provided by AgentPal itself |

## Why The Boundary Matters

AgentPal can help a host runtime decide who should own a task, what context is safe to load, what evidence is needed, and how to structure the output.

AgentPal does not itself execute commands, call APIs, connect to systems, scan the machine, or start worker processes. Those actions require a host runtime and current evidence.

## Practical Example

If a user asks for a sales follow-up workflow:

- Faye can shape the business scenario, process, data list, interface list, risks, missing information, and Task Package.
- PalSmith can design or review a Pal Team if a new Pal or workflow asset is needed.
- Quinn can review whether evidence and acceptance criteria are strong enough.
- Codex, Claude Code, or another runtime may read files or edit documents only when authorized and able to provide evidence.

The Pal layer organizes the work. The Agent runtime executes actions.

## Clean Contact Rule

Only valid Pal Packs should enter central contacts.

Do not register these as Pals by themselves:

- Skills
- tools
- models
- plugins
- MCP servers
- raw repositories
- knowledge packs
- personas without Pal Pack structure

## Next Links

- [What is a Pal?](01-what-is-a-pal.md)
- [What is a Pal Pack?](02-what-is-a-pal-pack.md)
- [Pal Team vs Agent Team](04-pal-team-vs-agent-team.md)
- [AgentPal vs Agent Runtime](../00-overview/03-agentpal-vs-agent-runtime.md)
