# What Is A Pal?

A Pal is a portable working companion for agent runtimes.

It packages persona, role boundaries, domain knowledge, skills, memory rules, workflows, context rules, output contracts, verification standards, and collaboration protocols into a maintained working asset.

## A Pal Is Not

- an independent runtime process
- an agent executable
- a single prompt
- a single Skill
- a tool, plugin, model, MCP server, or raw repository

## What A Pal Contains

A mature Pal can include:

- identity and role
- responsibility boundaries
- tone and collaboration style
- domain knowledge
- Skills and reusable methods
- runbooks and workflows
- memory and state boundaries
- output contract
- verification expectations
- learning rules for repeated tasks

## How A Pal Works In v0.1.0-rc.1

In Simple Pal Mode, the host runtime reads the selected Pal's assets and answers through that Pal's working mode. The Pal does not execute actions by itself.

For example, `/pal Harper` means the current runtime should use Harper's identity, assets, and output contract. It does not start a separate Harper process.

## Related

- [What is a Pal Pack?](02-what-is-a-pal-pack.md)
- [Pal vs Agent vs Skill](03-pal-vs-agent-vs-skill.md)
- [Simple Pal Mode](05-simple-pal-mode.md)
