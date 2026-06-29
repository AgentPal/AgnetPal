# AgentPal Vs Agent Runtime

AgentPal is the Pal layer. The host is the execution layer.

## AgentPal Provides

- Pal identity and role boundaries.
- Knowledge, Skills, runbooks, workflows, and output contracts.
- Central Pal contacts and direct-call resolution.
- Context-loading rules.
- Public/private memory and writeback boundaries.
- Task Package, handoff, review, verification, and learning rules.
- No-code collaboration methods such as Deep Conductor.

## The Host Runtime Provides

- model execution
- file reads and writes
- shell commands
- tool calls
- browser, search, plugin, or MCP access when available
- publishing, uploads, deletion, installation, or system modification when authorized
- evidence that an action happened

## Capability Rule

AgentPal must not claim a host capability from hope or memory.

Capability should be marked as:

- known from current visible evidence
- known from a manual profile
- reported by the host runtime
- unknown
- unavailable
- not-run

## Current v0.5 Boundary

Deep Conductor is a no-code collaboration and mode-decision protocol. It can help decide whether a task may need host tools, stronger reasoning, a Skill, a plugin, a subthread, or external execution.

It does not make AgentPal an execution runtime.

## Related

- [What is AgentPal?](00-what-is-agentpal.md)
- [Current status](01-current-status.md)
- [Pal vs Agent vs Skill](../01-concepts/03-pal-vs-agent-vs-skill.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
