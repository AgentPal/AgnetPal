# FAQ

## Is AgentPal An Agent Runtime?

No. AgentPal is a Pal layer and Pal Pack standard practice. The host runtime still performs model execution, file operations, commands, tool calls, publishing, deletion, and other actions.

## Is A Pal An Agent?

No. A Pal is a working partner loaded by a host runtime. It is not an independent process.

## Is AgentPal A Multi-Agent System?

AgentPal can coordinate multiple Pals as no-code collaboration, but it is not a multi-Agent runtime. It does not start multiple Agent processes by itself.

## What Is Active In v0.5?

Mira-first entry, 10 official Pals, `/pal Name` direct calls, AI owner judgement, Fast Route, Task Packages, Context Slicing, Asset Loading Budget, Runtime Response Gate, Deep Conductor as no-code collaboration and mode-decision protocol, and Codex-first real host evidence.

## Which Hosts Are Supported?

Codex is the verified first host. Claude Code has limited/minimal handoff evidence. Generic CLI Agent is a compatibility path. OpenCode and Gemini are unavailable in current evidence.

## Where Do Pals Live?

Single Pal Packs live under `official/pals/<Pal-Directory>/` or another approved Pal asset area.

## Is The AgentPal Root One Pal Pack?

No. The AgentPal root is the AgentPal workspace. It contains multiple Pal Packs and shared workspace assets.

## How Does AgentPal Discover Pals?

Through `workspace/organization/contacts/`. That central contact area is the current source of truth.

## Can A Skill Or Plugin Be A Pal Contact?

No. Skills, tools, plugins, models, MCP servers, raw repositories, runtime adapters, and knowledge packs do not become Pal contacts unless they are packaged as valid Pal Packs and approved.

## Related

- [Current status](../00-overview/01-current-status.md)
- [Known limitations](known-limitations.md)
- [What is AgentPal?](../00-overview/00-what-is-agentpal.md)
