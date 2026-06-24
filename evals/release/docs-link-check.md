# Release Docs Link Check

## Scope

Manual link review for README, runtime guides, prompts, examples, and evals.

## Required Path Checks

- `README.md`
- `README.zh-CN.md`
- `docs/04-runtime-guides/00-runtime-compatibility.md`
- `docs/04-runtime-guides/01-use-with-codex.md`
- `docs/04-runtime-guides/02-use-with-claude-code.md`
- `docs/04-runtime-guides/03-use-with-generic-cli-agent.md`
- `docs/04-runtime-guides/04-project-first-connection.md`
- `prompts/codex/initialize-agentpal-workspace.md`
- `prompts/claude-code/install-agentpal-current-project.md`
- `prompts/generic-cli-agent/install-agentpal-current-project.md`
- `examples/quickstart/README.md`
- `evals/runtime-guides/README.md`

## Pass

- every referenced file exists
- README and runtime guides use the same three Quick Start paths
- prompts are described as copy-and-paste Markdown instructions, not scripts or installers
- generic CLI wording remains conservative

## Fail

- README links to a missing prompt
- docs point to a renamed example that does not exist
- a future Subagent or Deep Conductor file is linked as a current Quick Start path
