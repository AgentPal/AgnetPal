# Add Runbooks

## Status

Current for AgentPal `v0.1.0-rc.1`.

Runbooks document repeatable procedures. They help the Pal guide the host runtime; they do not execute actions themselves.

## Start With Indexes

```text
runbooks/index.md
workflows/index.md
```

These can be placeholders until real procedures exist.

## Runbook Template

```md
# Runbook Name

## Use When

## Inputs

## Steps

## Approval Gates

## Evidence Required

## Report Shape
```

## Workflow Template

```md
# Workflow Name

## Stages

## Assets Used

## Handoff Points

## Completion Criteria
```

## Boundary

Do not describe Subagent Mode, Deep Conductor, parallel child workflows, or external Agent orchestration as active `v0.1.0-rc.1` behavior.
