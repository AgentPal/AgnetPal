# Token / Cost-aware Deep Conductor

Token / Cost-aware Deep Conductor is the no-code method for making complex AgentPal work context-efficient, evidence-aware, and cost-conscious without weakening quality.

It does not make AgentPal a token meter, cost calculator, model router, automation runtime, scanner, validator, installer, service, or execution layer.

## Definition

Token / Cost-aware means the Conductor explicitly plans:

- how much context to read;
- which summaries or memories to reuse;
- which Capability profiles to inspect;
- when full files are necessary;
- which Runtime Skill candidates may reduce rework;
- what model or reasoning strength may fit the package;
- which verification evidence is required.

The goal is best useful evidence per context unit, not the lowest possible prompt.

## Not Cheapest-first

Cheapest-first is a failure mode. It chooses low context, weak reasoning, or a cheaper Runtime even when the task needs stronger judgement, broader evidence, or independent verification.

The correct rule is quality-aware sufficiency:

- start with the smallest useful context;
- increase read tier when risk, ambiguity, or verification need requires it;
- explain every tier escalation;
- never skip evidence to save cost.

## Deep Conductor Relationship

This guide operationalizes Step 8 of the Deep Conductor Master Loop, and also affects memory loading, capability reads, Runtime Skill candidate decisions, verification planning, and Routing Memory writeback.

It is used with:

- `orchestration/token-cost-aware-conductor-policy.md`
- `orchestration/context-budget-protocol.md`
- `orchestration/prompt-shaping-by-model-and-reasoning.md`
- `templates/orchestration/context-budget-plan.md`
- `templates/orchestration/context-usage-report.md`

## Context Budget

A Context Budget is a qualitative plan for what will be read and what will stay excluded.

Default reading order:

1. Resource index.
2. Pal memory snapshot.
3. Routing Memory summary.
4. Capability profiles.
5. Selected source files or snippets.
6. Full content only when necessary.

This lets a Runtime or Pal answer questions like:

- Did we reuse valid memory?
- Which files were only index-known?
- Which files were fully read, and why?
- Which context was forbidden for privacy or relevance?
- What verification context was needed?

## Model / Reasoning Strength

Model and reasoning suggestions are candidates. The host Runtime or user chooses the actual model and reasoning strength.

- Strong / high reasoning: high ambiguity, high risk, multi-stage synthesis, release readiness, repair after failure, or sensitive verification.
- Medium / medium reasoning: normal task packaging, bounded documentation, straightforward multi-file changes, and ordinary synthesis.
- Economy / weak / low reasoning: narrow, low-risk, highly specified tasks with exact steps and acceptance criteria.

Weak or economy candidates need more detailed Task Packages. The package should include file boundaries, input summaries, explicit steps, acceptance criteria, forbidden actions, and final report fields.

## Runtime-installed Skill Cost Optimization

Runtime-installed Skills can reduce cost by avoiding manual rework or repeated context reading, for example browser verification, document rendering, repository analysis, or structured extraction. They are host Runtime capabilities, not AgentPal Skills.

The Conductor may name Runtime Skill candidates only as candidates. The host Runtime must report available / unavailable / unknown / blocked before use.

## Verification Cost

Verification is a necessary quality cost. If verification is required for safety, release, source-backed claims, or user-facing artifacts, it must remain in scope.

If verification cannot run, the result is `not-run` or `blocked`. The final report must not translate missing evidence into completion.

## Context Usage Report

Every token / cost-aware package should ask for a Context Usage Report. The report is not an exact token count. It records context tiers, memory reuse, full reads, Runtime Skills, verification context, quality tradeoffs, and next-time recommendations.

Routing Memory and PalBench may use the report as evidence for future judgement, but recommendations remain candidates, not fixed rules.

## No-code Boundary

This guide defines no-code protocols and templates only. It does not:

- add runtime metering;
- calculate cost;
- select models automatically;
- call Runtime Skills automatically;
- read files automatically;
- run verification automatically;
- create background tasks or services.
