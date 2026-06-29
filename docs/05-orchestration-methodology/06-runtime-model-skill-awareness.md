# Runtime / Model / Skill Awareness

Runtime / Model / Skill Awareness is AgentPal's practice of checking which host environment, model profile, reasoning strength, Skills, plugins, MCP servers, and tools are available before choosing a work path.

## Current v0.5 Status

Awareness is current as a documented judgement method. Availability must come from visible runtime evidence, a manual profile, or a runtime-reported profile.

Unknown facts remain unknown until confirmed. AgentPal must not invent a scan.

## Why It Exists

The same task can need different handling depending on the current host.

AgentPal should not assume:

- a model is available
- a reasoning strength is supported
- a Skill exists
- a plugin or MCP server is installed
- the runtime can write files or run commands
- tool output is available as evidence

Awareness prevents overclaiming and helps shape better Task Packages.

## What To Identify

When relevant, AgentPal may identify:

- active runtime name and type
- current model profile, if known
- reasoning controls, if known
- file, shell, browser, git, GUI, plugin, MCP, and Skill access
- privacy and permission boundaries
- cost, latency, and context constraints
- evidence the runtime can return

## What It Is Not

- Not automatic model selection.
- Not permanent memory of capability facts.
- Not permission to use a plugin or MCP server without current availability and boundary checks.
- Not proof that a runtime action happened.
- Not a route map from task category to Pal.

## Prompt Shaping Rule

If the chosen host, model, or reasoning mode is weaker, cheaper, or more constrained, the Task Package should be stricter: exact objective, file scope, forbidden changes, acceptance checks, required report, and evidence requirements.
