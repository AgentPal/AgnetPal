# Pal Skill Vs Runtime Skill Protocol

AgentPal uses two different Skill layers. They must not be mixed.

## Pal-Owned Skill

A Pal-owned Skill is a no-code method, workflow, output contract, runbook, or capability asset stored under a Pal Pack and used by that Pal to think, decide, package, review, or explain work.

Examples:

- Atlas development task splitting skill;
- Quinn completion review skill;
- PalSmith health-check skill;
- Mira owner judgement skill.

Pal-owned Skills are part of Pal identity and professional method. They do not directly execute host Runtime tools.

## Runtime-Installed Skill

A Runtime-installed Skill, Agent Skill, plugin, or MCP tool is installed in or exposed by the host Agent Runtime.

Examples:

- a Codex Skill;
- a Claude Code Skill;
- an MCP tool;
- a browser skill;
- an office document skill;
- a repository analysis skill;
- a plugin.

Runtime-installed Skills may perform file operations, browser operations, document operations, repository analysis, API calls, or other tool-backed work when the host Runtime supports and authorizes them.

## Separation Rule

The Pal does not execute a Runtime-installed Skill.

The Pal may identify or suggest a Runtime-installed Skill candidate, explain why it may help, and include it in a Task Package. The host Runtime decides whether the Skill is installed, available, authorized, and safe to use.

## Task Package Rule

When a Runtime-installed Skill may help, write it under `runtime_skill_candidates`.

When a Pal uses its own method, write it under `pal_owned_skills_used`.

Never place Pal-owned methods under Runtime Skill candidates. Never claim a Runtime-installed Skill ran unless current Runtime evidence shows it.

## Memory Rule

After a task, record results separately:

- Pal-owned Skill usefulness can enter Pal learning or Pal method notes.
- Runtime-installed Skill usage results can enter Routing Memory or Runtime Skill usage memory.

Both memory types are evidence for future judgement. Neither becomes a fixed route.

## Failure Signals

A response fails this protocol if it:

- says a Pal executed a browser, office, repository, or shell Skill directly;
- treats a Pal-owned runbook as an installed host Skill;
- treats a host Runtime plugin as a Pal identity asset;
- makes Skill availability claims without current evidence;
- turns any Skill profile into automatic routing.
