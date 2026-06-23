# Runtime / Model / Skill Awareness

Runtime / Model / Skill Awareness is AgentPal's practice of checking which execution environment, model profile, reasoning strength, Skills, plugins, MCP servers, and tools are available before choosing a work path.

## Status

- Current: Documented as awareness and refresh policy. Unknown facts remain `unknown until scanned` in v0.1.0-rc.1.
- Future: May become richer profile refresh and capability validation.
- Research: PalBench can measure whether awareness improves runtime selection, prompt shaping, Skill activation, and verification.

## Why it exists

The same task can need different handling depending on the current runtime.

AgentPal should not assume:

- a model is available
- a reasoning strength is supported
- a Skill exists
- a plugin or MCP server is installed
- the runtime can write files or run commands
- tool output is available as evidence

Awareness prevents overclaiming and helps shape better Task Packages.

## How it works

Before important work, AgentPal may identify:

- active runtime name and type
- current model profile, if known
- reasoning strength controls, if known
- file, shell, browser, git, GUI, plugin, MCP, and Skill access
- privacy and permission boundaries
- cost, latency, and context constraints
- evidence the runtime can return

Model and reasoning choices should consider:

- complexity
- risk
- ambiguity
- context size
- verification need
- cost and latency

Stronger model or reasoning profiles are useful for planning, complex judgement, failure diagnosis, and final verification. Lower-cost profiles fit bounded, deterministic, well-specified work.

## What it is not

- Not automatic model selection in v0.1.
- Not a permanent memory of capability facts.
- Not permission to use a plugin or MCP server without current availability and boundary checks.
- Not proof that a runtime action happened.
- Not a route map from task category to Pal.

## Prompt shaping rule

If the chosen model or runtime is weaker, cheaper, or more constrained, the Task Package should be stricter:

- exact objective
- file scope
- forbidden changes
- acceptance checks
- required final report
- evidence required

