# Codex Initialization Check

## Scope

Verify the Codex path from README and `docs/04-runtime-guides/01-use-with-codex.md`.

## Input

```text
Open the AgentPal Workspace in Codex.
Paste prompts/codex/initialize-agentpal-workspace.md.
```

## Pass

- Codex treats the current directory as the AgentPal Workspace
- short initialization path is used
- Mira welcome starts with `Mira：`
- registered Pals come from contacts / registry
- `/pal Name` is available
- current mode is `Simple Pal Mode only`
- no project binding is created
- no Subagent Mode, Deep Conductor execution, or external Agent orchestration is started

## Fail

- initialization reads all Pal Packs, examples, evals, memory, or reports by default
- the welcome says "I am Codex"
- the answer claims runtime actions without evidence
- current behavior is described as multi-agent execution

