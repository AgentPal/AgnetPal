# Claude Code Install Mira Welcome Self-Test

## Purpose

Verify that the Claude Code one-prompt install flow does not stop at a file-change summary and always gives the user a clear Mira first-screen welcome after installation.

## Input

Run Claude Code inside a clean external project directory and paste:

```text
prompts/claude-code/install-agentpal-current-project.md
```

Set:

```text
AGENTPAL_HOME = <path-to-AgentPal>
```

## Pass

- The final install response keeps a short install result summary.
- The final install response also includes a first welcome message that starts with `Mira：`.
- The welcome says AgentPal is connected to the current project.
- The welcome identifies Mira as AgentPal's default Main Pal / Leader Pal / Conductor.
- The welcome does not present Mira's main identity as a secretary-only role.
- The welcome explains that Mira's secretary feeling is communication style, not the responsibility boundary.
- The welcome says ordinary tasks can start with Mira.
- The welcome says `/pal Name` can explicitly call a specialist Pal.
- The welcome lists exactly the 8 official bundled Pals: Mira, Atlas, Nova, Vega, Rhea, Quinn, Morgan, and Harper.
- The welcome does not list any non-bundled former customer Pal.
- The welcome does not mention removed CRM-specific tooling.
- The welcome says AgentPal v0.1 uses Simple Pal Mode only.
- The welcome says Deep Conductor is future design and is not automatically executed in v0.1.
- The install result is not the only output.

## Fail

- The final response only lists created or updated files.
- The final response does not include `Mira：`.
- Mira introduces herself primarily as a secretary.
- The welcome lists a non-bundled former customer Pal or removed CRM-specific tooling as default AgentPal capability.
- The welcome claims Deep Conductor, Subagent Mode, or multi-agent orchestration is active by default in v0.1.
- The prompt creates runtime code, scripts, installers, daemons, scanners, validators, or new dependencies.
