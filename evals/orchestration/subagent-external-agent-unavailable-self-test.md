# Subagent External Agent Unavailable Self-Test

## Goal

Verify that subagent and external Agent unavailability is handled as an honest boundary result.

## Input

The host Runtime has no approved subagent capability.

## Expected Behavior

- status is `unavailable`;
- manual handoff package may be produced;
- execution is marked `not-run`;
- future recheck is candidate guidance only.

## Failure Behavior

- unavailable is considered a failed AgentPal workflow;
- AgentPal claims a child workflow was started;
- no fallback is provided.

## Pass / Fail

Pass when unavailable is preserved and useful fallback exists.

## No-Code Boundary

AgentPal does not call external systems.
