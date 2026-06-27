# Context Budget Protocol

Context Budget is AgentPal's no-code protocol for planning and reporting context use in Deep Conductor, Project Conductor, Runtime Task Packages, and complex Pal work.

It is not an exact token meter, cost calculator, model selector, scanner, validator, automation runtime, or execution feature.

## Required Plan Fields

A Context Budget Plan defines:

- Context Budget Plan: task goal, task type, risk, quality target, latency preference, cost sensitivity, initial tier, max tier, and escalation rules.
- Context Read Tier: the highest planned read depth and any tiers actually used.
- Index-known Paths: paths discovered by index, registry, directory listing, or Resource Index but not opened as content.
- Summary-read Content: memory snapshots, Routing Memory summaries, source summaries, or previous reports read as summaries.
- Full-content Read: selected files opened fully, each with a reason.
- Memory-used: Pal Project Memory, Routing Memory, Runtime Skill Usage Memory, Verification Memory, or other approved summaries.
- Profile-used: Runtime, model, reasoning, Skill, plugin, MCP, or Pal capability profiles.
- Runtime Skill-used: host Runtime Skill candidates named, checked, used, not-run, or blocked.
- Verification Context: evidence needed to verify the work.
- Stop Conditions: conditions where the Runtime or Pal must stop and report rather than continue.
- Ask-user Conditions: conditions requiring user confirmation or missing-decision clarification.
- Context Usage Report: expected final context use report shape.

## Context Read Tiers

Higher tiers cost more context and should be chosen deliberately.

- Tier 0: no read / use user input only.
- Tier 1: index only.
- Tier 2: memory snapshot / summary.
- Tier 3: selected file snippets.
- Tier 4: full selected files.
- Tier 5: expanded review with explicit reason.

Default behavior is low-to-high. High-risk tasks may jump tiers when waiting would create quality, safety, release, privacy, or verification risk. Every tier escalation must explain the reason.

## Tier Use Rules

- Tier 0 is acceptable for tiny, self-contained user requests.
- Tier 1 is the default start for repository or docs navigation.
- Tier 2 is preferred when recent valid memory or summaries can prevent rereading.
- Tier 3 is preferred before opening full files when the target section is known.
- Tier 4 is required when exact wording, complete contract structure, or whole-file consistency matters.
- Tier 5 is reserved for release checks, cross-file regressions, suspicious contradictions, or failure repair that needs broader evidence.

## Evidence Rule

The Conductor cannot skip evidence to save cost. If verification needs source files, screenshots, test output, rendered artifacts, or command output, the Context Budget must include that verification context or report it as missing, not-run, or blocked.

## Privacy Rule

`forbidden_context` supports privacy and relevance. It may exclude secrets, private memory, raw logs, unrelated Pal assets, local absolute paths, full chat history, user documents, or other material not approved for the task.

## Reporting Rule

A Context Usage Report must say what was actually used and what remained missing. It must not claim exact token counts unless the host Runtime provides exact metering evidence.
