# Intra-Workflow Pal Isolation Example

This is a future-design example.

## Goal

Avoid group-chat collapse during independent review.

## Correct Shape

```text
Mira creates separate Context Access Lists.
Atlas receives only the development CAL.
Nova receives only the product CAL.
Quinn receives only the quality CAL.
Mira reads final reports after all independent outputs exist.
```

## Not Allowed

```text
Atlas drafts first.
Nova reads Atlas and follows it.
Quinn reads both and lowers the testing bar.
Rhea repeats the summary.
```

## v0.1 Boundary

AgentPal v0.1 does not execute this parallel flow. The example documents the future Deep Conductor isolation rule.

