# Routing Decision Record

A Routing Decision Record captures why AgentPal selected a Pal, topology, runtime, model profile, reasoning strength, Skill, plugin, MCP candidate, or verification path.

It is a memory and audit artifact, not a route rule.

## Status

- Current: Available in v0.1.0-rc.1 as a template and audit artifact.
- Future: May feed Routing Reward Memory and improve future non-binding recommendations.
- Research: PalBench can compare routing choices with outcomes, rework count, user acceptance, and verification results.

## Why it exists

Without a record, routing lessons disappear or become vague habits.

With a record, maintainers can inspect:

- what task was being handled
- what constraints mattered
- what route was selected
- what alternatives were considered
- what context was read
- what verification was planned
- whether the route worked
- what to try next time

## How it works

A record may include:

- task summary and task type
- decision context
- selected Pal, topology, runtime, model, reasoning strength, and capability candidates
- why selected
- alternatives considered
- context usage
- verification plan
- privacy review
- outcome
- next-time recommendation

The `next_time_recommendation` must stay non-binding. It can inform AI judgement later, but it must not become a keyword route.

## What it is not

- Not a hard-coded routing table.
- Not a permanent task-domain rule.
- Not a way to bypass Mira's case-by-case judgement.
- Not proof that the selected route succeeded.
- Not a place for secrets, private project facts, or raw private memory.

## Good record behavior

Write the reason in terms of the actual task, constraints, risk, evidence need, and available capabilities.

Avoid reasons like "this keyword routes to this Pal."

