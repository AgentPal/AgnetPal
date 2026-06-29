# Quick Start

Use this path when you want to try AgentPal v0.5 quickly and safely.

AgentPal is a lightweight Pal team organization layer. It gives an existing agent runtime a readable workspace for Pal identity, knowledge, skills, memory boundaries, task packages, routing judgement, and verification habits. It is not an Agent runtime, app runtime, connector, scanner, installer, daemon, or marketplace.

## 1. Get The Workspace

Clone or download AgentPal, then keep it as a normal local folder.

```text
git clone <AgentPal-repository-url>
cd AgentPal
```

If you downloaded a zip archive, extract it and open the extracted AgentPal folder.

## 2. Open In Codex

Codex is the verified first host for v0.5.

1. Create or open a Codex project using the AgentPal workspace directory.
2. Open [`prompts/codex/initialize-agentpal-workspace.md`](../../prompts/codex/initialize-agentpal-workspace.md).
3. Copy the whole prompt into the Codex thread.
4. Check that the first AgentPal reply starts with `Mira：`.
5. Confirm the official Pal roster has 10 Pals and includes Faye.

## 3. Start With Mira

Ordinary messages go to Mira first. Mira judges whether to answer directly, route to a specialist Pal, or ask for a focused clarification.

```text
Mira, explain what I should read first as a new AgentPal user.
```

## 4. Call A Pal Directly

Use `/pal Name` when you already know who you want.

```text
/pal Faye Help me turn a sales follow-up idea into a delivery plan.
```

Direct calls are resolved from the central contacts under `workspace/organization/contacts/`. They do not start a separate process.

## 5. Connect An External Project

For a separate user project, use thin binding. The external project remains the active project; AgentPal remains the Pal workspace reference.

Start here:

- [Bind an external project](../01-getting-started/bind-external-project.md)
- [Project-first connection](../04-runtime-guides/04-project-first-connection.md)

The project-side `.agentpal/` folder should stay small. It should not copy Pal Packs, docs, evals, release files, memory, reports, or internal AgentPal assets.

## Current Limits

- Codex-first behavior has real host confirmation evidence for v0.5.
- Claude Code has limited/minimal handoff evidence only; full host acceptance is not claimed.
- Generic CLI Agent is a compatibility path, not a fully validated runtime.
- OpenCode and Gemini are unavailable in the current evidence.
- Plan Mode UI evidence is unavailable; Goal Mode evidence is limited.
- Host capability must come from visible runtime evidence, a manual profile, or runtime-reported capability. AgentPal must not invent a scan.

## Next Links

- [Install or download](01-install-or-download.md)
- [Use with Codex](02-open-in-codex.md)
- [Initialize AgentPal](04-initialize-agentpal.md)
- [Call your first Pal](05-call-your-first-pal.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
