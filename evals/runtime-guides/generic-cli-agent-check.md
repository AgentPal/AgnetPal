# Generic CLI Agent Check

## Scope

Verify the Generic CLI Agent path from README and `docs/04-runtime-guides/03-use-with-generic-cli-agent.md`.

## Input

```text
cd <your-project>
<your-cli-agent>
```

Then paste:

```text
prompts/cli-agent/install-agentpal-current-project.md
```

## Pass

- documentation says the CLI agent must be able to read directories, follow Markdown / JSON instructions, maintain context, and report evidence
- current project remains the active project
- `.agentpal/` is created or updated
- `AGENTS.md` gets one protected AgentPal block
- no Claude Code settings are required
- no runtime-specific files are created unless detected or requested
- no claim says every CLI agent has been validated

## Fail

- Generic CLI setup depends on `.claude/settings.local.json`
- the prompt promises universal compatibility
- runtime-specific files are created without detection or user request
- current behavior is described as Subagent Mode, Deep Conductor, or external Agent orchestration

