# Contributing to AgentPal

Thank you for helping improve AgentPal.

AgentPal v0.5 is a no-code Pal organization layer and Pal Pack workspace for existing agent runtimes. Contributions should keep the repository public-safe, runtime-readable, and honest about current evidence.

## What Contributions Are Welcome

- Public documentation improvements.
- Pal Pack standards, templates, and examples.
- Public-safe examples for Pal teams, Task Packages, Context Packets, and project binding.
- Runtime guide wording that preserves current evidence limits.
- PalBench and validation records that clearly say `pass`, `partial`, `blocked`, `not-run`, or `unavailable`.
- Fixes for broken links, stale version wording, or public-safety issues.

## Current Boundary

AgentPal is not an Agent runtime, multi-agent runtime, app runtime, installer, daemon, scanner, connector layer, marketplace, or external-system executor.

Do not add required Python, Node.js, Rust, Go, service, daemon, scanner, validator, installer, desktop UI, or web UI dependencies unless a future release explicitly changes that boundary.

Real execution belongs to the host runtime and must be backed by current evidence and user authorization.

## Pal Pack Contributions

Valid Pal Packs belong under an approved Pal Pack area, such as `official/pals/` for bundled official Pals or another organization-approved Pal area.

Minimum public Pal Pack files:

- `README.md`
- `PAL.md`
- `pal.json`
- `SKILL.md`
- `AGENTS.md`
- `core/output-contract.md`

A useful Pal Pack should also include responsibility boundaries, collaboration permissions, safety notes, verification expectations, and public-safe placeholders for memory, state, reports, examples, and evals when those directories are present.

Do not register ordinary Skills, tools, models, MCP servers, plugins, raw repositories, knowledge packs, or persona packs as Pal contacts. Only valid Pal Packs should enter the central contacts under `workspace/organization/contacts/`.

## Documentation Contributions

Good documentation contributions:

- explain current v0.5 behavior
- distinguish Pal, Skill, Agent, and Runtime
- keep Codex as the current verified first path
- mark limited, experimental, unavailable, or not-run host support honestly
- use relative links
- avoid local absolute paths
- keep root files short and move deeper explanation into `docs/`
- keep user onboarding separate from evidence archives

The current Codex initialization path is:

```text
prompts/codex/initialize-agentpal-workspace.md
```

## Runtime Support Claims

Use conservative public wording:

- Codex: verified first path.
- Claude Code: minimal handoff evidence only unless future full host acceptance passes.
- Generic CLI Agent: compatibility prompt path, not broad validation.
- DeepSeek / DeepSeek-TUI: experimental or version-help level unless future tests pass.
- Plan Mode: UI unavailable in current evidence.
- Goal Mode: limited evidence.
- OpenCode / Gemini: unavailable in current evidence.

Do not claim connector, scanner, daemon, marketplace, app runtime, automatic environment scan, or external-system writeback support without current runtime evidence.

## Public-Safe Data Rules

Do not submit:

- private user memory
- real user conversation history
- private project facts
- internal development reports
- API keys, tokens, passwords, secrets, credentials, or private keys
- real customer data
- proprietary documents without permission
- copied internal reference documents
- long third-party README, Skill, source, or documentation text
- copyrighted material without permission and proper license handling

Templates and examples must use synthetic or placeholder data.

## Release Boundary

Everything committed to the public AgentPal repository is treated as release content. Keep runtime-private memory, private state, real reports, internal notes, and secrets outside the repository or under ignored local-only paths.

Remote publication actions such as `git push`, tags, GitHub Releases, or package publication require explicit current-session authorization.
