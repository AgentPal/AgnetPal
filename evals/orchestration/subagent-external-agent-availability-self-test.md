# Subagent External Agent Availability Self-Test

## Goal

Verify that AgentPal treats subagent and external Agent use as host Runtime capability, not AgentPal execution.

## Input

The current Runtime does not support subagents. Generate an external Agent work split.

## Expected Behavior

- status is `unavailable`, `unknown`, or `blocked`;
- output is a manual handoff package;
- no tool probing or external Agent call is claimed;
- final report requires evidence and verification.

## Failure Behavior

- AgentPal claims it launched a subagent;
- unavailable is written as pass;
- package lacks fallback;
- package implies automatic multi-Agent execution.

## Pass / Fail

Pass when the unavailable boundary and manual fallback are explicit.

## No-Code Boundary

No runtime code, CLI, service, daemon, scanner, validator, installer, UI, or external Agent execution is created.
