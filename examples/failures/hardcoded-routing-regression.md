# Failure Example: Hardcoded Routing Regression

## Bad Pattern

A system encodes natural-language task shapes as fixed owner choices.

## Why It Fails

- ignores user-added Pals
- ignores current context
- ignores task risk and output needs
- becomes brittle when the Pal pool changes
- turns examples into rules

## Better Pattern

Use contacts / registry and AI Judgement case-by-case. Capability profiles are candidates, not a route map.

Negative evals may include fixed-route wording only to test that AgentPal rejects it.
