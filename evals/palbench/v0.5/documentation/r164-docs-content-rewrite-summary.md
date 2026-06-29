# R164 Docs Content Rewrite Summary

Date: 2026-06-30

## Scope

R164 rewrote retained user and integrator documentation after the R162 public docs rewrite and R163 docs directory restructure.

Primary target areas:

- Getting Started
- Runtime Guides
- Core Concepts
- Official Pals
- PalSmith / Faye / Pal Team creation
- Agent-use decision and capability awareness
- Memory / knowledge / repeated-task learning

## Key Updates

- Replaced old v0.1 / v0.2 / v0.3 placeholder language in high-visibility user docs with current v0.5 wording.
- Clarified AgentPal as a lightweight Pal team organization layer, not an Agent runtime or execution layer.
- Preserved Codex-first verified positioning.
- Limited Claude Code to limited/minimal handoff evidence.
- Limited Generic CLI Agent to compatibility path.
- Marked OpenCode / Gemini unavailable in current evidence.
- Added Faye into official 10-Pal docs and example-library navigation.
- Clarified Pal / Skill / Agent differences.
- Clarified Pal Team vs Agent Team and Deep Conductor no-code boundaries.
- Rewrote PalSmith pages around v0.5 governance, draft creation, Task Packages, and no automatic registration.
- Rewrote memory pages around memory candidates, privacy, project memory, and Skill promotion.
- Updated `RESOURCE_INDEX.md` and `agentpal.json` with R164 evidence paths.

## Files Rewritten Or Updated

Representative files:

- `docs/00-overview/00-what-is-agentpal.md`
- `docs/00-overview/01-current-status.md`
- `docs/00-overview/02-current-capabilities.md`
- `docs/00-overview/03-agentpal-vs-agent-runtime.md`
- `docs/00-overview/04-what-agentpal-is-not.md`
- `docs/01-concepts/01-what-is-a-pal.md`
- `docs/01-concepts/03-pal-vs-agent-vs-skill.md`
- `docs/01-concepts/04-pal-team-vs-agent-team.md`
- `docs/01-concepts/05-simple-pal-mode.md`
- `docs/01-concepts/08-pal-teams-collaboration-and-deep-conductor.md`
- `docs/01-getting-started/bind-external-project.md`
- `docs/01-getting-started/faq.md`
- `docs/02-getting-started/00-quick-start.md`
- `docs/02-getting-started/01-install-or-download.md`
- `docs/02-getting-started/02-open-in-codex.md`
- `docs/02-getting-started/03-open-in-claude-code.md`
- `docs/02-getting-started/04-initialize-agentpal.md`
- `docs/02-getting-started/05-call-your-first-pal.md`
- `docs/02-getting-started/06-create-your-first-pal-in-5-minutes.md`
- `docs/02-getting-started/mira-first-usage.md`
- `docs/02-getting-started/multi-pal-collaboration-prompt-cards.md`
- `docs/04-runtime-guides/00-runtime-compatibility.md`
- `docs/04-runtime-guides/01-use-with-codex.md`
- `docs/04-runtime-guides/02-use-with-claude-code.md`
- `docs/04-runtime-guides/03-use-with-generic-cli-agent.md`
- `docs/04-runtime-guides/04-project-first-connection.md`
- `docs/04-runtime-guides/99-future-runtime-adapters.md`
- `docs/05-orchestration-methodology/README.md`
- `docs/05-orchestration-methodology/00-methodology-overview.md`
- `docs/05-orchestration-methodology/05-capability-inventory.md`
- `docs/05-orchestration-methodology/06-runtime-model-skill-awareness.md`
- `docs/05-orchestration-methodology/09-deep-conductor-future.md`
- `docs/05-orchestration-methodology/11-pal-teams-and-deep-conductor.md`
- `docs/05-orchestration-methodology/runtime-installed-skill-orchestration-guide.md`
- `docs/06-palsmith/README.md`
- `docs/06-palsmith/palsmith-end-to-end-productization.md`
- `docs/07-memory-and-learning/`
- `docs/07-official-pals/`
- `docs/99-reference/`
- `docs/PalSmith.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`

## Non-Goals

- No directory restructure beyond content fixes.
- No GitHub push, pull, fetch, tag, or Release.
- No new CLI, app, installer, scanner, daemon, connector, marketplace, or runtime feature.
- No external project writes.
- No official Pal behavior asset changes.

## Result

Status: `pass`

R164 priority user documentation is now consistent with the current v0.5 public claim surface.
