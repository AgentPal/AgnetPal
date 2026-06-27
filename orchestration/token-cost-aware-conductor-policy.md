# Token / Cost-aware Conductor Policy

This policy makes Deep Conductor context use auditable without turning AgentPal into a token meter, cost calculator, model router, scanner, validator, installer, service, or runtime program.

Token / Cost-aware means the Conductor plans context, memory, profile reads, Runtime Skill candidates, prompt shape, and verification cost deliberately. It optimizes for useful evidence per context unit, not for the lowest immediate prompt size.

It is not `cheapest-first`. A cheaper model, lower reasoning strength, or shallower context tier is acceptable only when the task remains clear, bounded, and verifiable. If quality, safety, privacy, release readiness, or user trust would be harmed, Deep Conductor must spend more context or reasoning and explain why.

## Relationship To Deep Conductor Master Loop

This policy is applied mainly in Deep Conductor Step 2, Step 4, Step 5, Step 7, Step 8, Step 9, Step 10, and Step 12:

- Step 2 reuses approved Pal memory and Routing Memory summaries before rereading old material.
- Step 4 reads only relevant Capability Inventory profiles.
- Step 5 treats Runtime-installed Skills as cost and rework reducers only after availability evidence.
- Step 7 plans allowed and forbidden context.
- Step 8 records the Context Budget Plan and prompt shaping notes.
- Step 9 passes bounded context to the host Runtime.
- Step 10 protects verification from cost-cutting.
- Step 12 records Context Usage Report and Routing Memory candidates.

Deep Conductor remains no-code. The policy creates Markdown / JSON-readable plans and reports; it does not count exact tokens, calculate cost, choose models automatically, or run tools.

## Context Budget Concept

A Context Budget is a planned boundary for what may be read, summarized, reused, fully opened, verified, and excluded. It is qualitative and auditable.

The default reading order is:

1. Resource index.
2. Pal memory snapshot.
3. Routing Memory summary.
4. Capability profiles.
5. Selected source files or selected snippets.
6. Full content only when necessary.

This order prevents two common failures: reading everything before judgement, and under-reading evidence because token cost feels uncomfortable.

## Model And Reasoning Strength Principles

Model and reasoning notes are candidates for the host Runtime or user. They are not automatic selectors.

- Strong / high reasoning candidates fit ambiguous, high-risk, multi-stage, release, repair, or synthesis work.
- Medium / medium reasoning candidates fit bounded planning, normal documentation, and known workflow packaging.
- Economy / weak / low reasoning candidates fit narrow edits, extraction, checklist filling, or highly specified execution packages.

Weak or economy candidates require more explicit prompts: file boundaries, steps, acceptance criteria, do-not-do items, and exact final report fields.

## Runtime-installed Skill Cost Role

Runtime-installed Skills, plugins, MCP tools, browser tools, repository-analysis tools, and document tools may reduce rework and context load when the host Runtime already has them and the package names them within scope.

They must be treated as candidates. AgentPal does not scan, install, invoke, or own them. Availability evidence is separate from execution evidence, and execution evidence is separate from verification evidence.

## Verification Is Not Optional

Verification must not be skipped to save tokens or cost. If verification is expensive, the plan records `verification_cost_reason` and chooses the smallest sufficient evidence path. If a check cannot run, report `not-run` or `blocked`; do not convert missing evidence into a pass.

## Required Artifacts

Use these no-code artifacts when token / cost awareness matters:

- `orchestration/context-budget-protocol.md`
- `templates/orchestration/context-budget-plan.md`
- `templates/orchestration/context-usage-report.md`
- `orchestration/prompt-shaping-by-model-and-reasoning.md`
- `templates/memory/routing-memory-record.md`

## Context Usage Report

After a task or package returns evidence, record what context was actually used:

- read tiers used;
- index-known path count;
- memory used;
- profiles read;
- summary sources and full-content files;
- Runtime Skills used or not-run;
- verification context used;
- context saved by reuse;
- quality tradeoffs;
- missing context;
- next-time recommendation.

The report is not an exact token count. It is used by Routing Memory and PalBench to improve future judgement without becoming a fixed route.

## Anti-patterns

- Cheapest-first selection that lowers quality or verification.
- Reading the whole workspace before task judgement.
- Treating memory as proof of current files, tools, or Runtime state.
- Claiming exact token or cost numbers without host-provided metering.
- Treating a model, Pal, Runtime, Skill, plugin, or MCP candidate as an automatic route.
- Skipping verification, source checks, release checks, screenshots, tests, or evidence review to reduce context.
