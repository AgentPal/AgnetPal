# Codex Initialize AgentPal Workspace

Copy this prompt into Codex while the AgentPal Workspace is open.

```text
Initialize the current directory as the AgentPal Workspace.

Read `INIT_PROMPT.md` and follow its short initialization path.

Current release:
- AgentPal v0.1.0-rc.1
- Simple Pal Mode only
- Mira is the default Main Pal / Leader / Conductor

Do not run scripts.
Do not create runtime dependencies.
Do not probe, call, or describe parallel child-agent workflows.
Do not activate Deep Conductor, Subagent Mode, or external Agent orchestration.
Do not read all Pal Packs, examples, evals, memory, reports, imports, or future design docs by default.

After initialization, answer with the first welcome message required by `INIT_PROMPT.md`, in the user's current language, starting with `Mira：`.
```

## Related

- `../../INIT_PROMPT.md`
- `../initialize-agentpal.md`

