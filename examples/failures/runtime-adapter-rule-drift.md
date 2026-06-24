# Failure Example: Runtime Adapter Rule Drift

Failure shape:

```text
Codex prompt has the latest First Pal Gate.
Claude Code prompt still has an older Mira owner-routing summary.
Generic CLI prompt has a third variation.
```

Why this fails:

- Different runtimes answer differently for the same AgentPal task.
- Bug fixes must be copied into multiple prompts.
- Already-bound projects can keep stale behavior.

Correct shape:

```text
All adapters point to AgentPal workspace core gates:
- core/agentpal-core-gate.md
- core/first-pal-gate.md
- core/deliverable-aware-task-judgement-gate.md
```

Adapter prompts only explain how to find and read the core gates.
