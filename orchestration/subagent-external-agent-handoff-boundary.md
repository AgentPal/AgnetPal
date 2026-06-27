# Subagent / External Agent Handoff Boundary

This protocol defines how AgentPal may prepare no-code handoff packages for host Runtime subagents or external Agents.

AgentPal does not start subagents, call external Agents, manage child workflows, or run multi-agent execution. Subagent and external Agent support is a host Runtime capability. Current availability must be proven by the host Runtime and must stay inside user-approved scope.

## Status Values

Use one of:

- `available`: the host Runtime reports current support and permission evidence.
- `unavailable`: the host Runtime does not support the capability.
- `unknown`: availability was not checked or cannot be determined.
- `blocked`: policy, permission, privacy, or safety boundary prevents use.

`unavailable` is not a failure of AgentPal. It means the useful output is a manual handoff package or a fallback package.

## Allowed

- Prepare an external-agent handoff package.
- Prepare a subagent task package for a host Runtime that explicitly supports and permits it.
- Require Context Packet fields, final report fields, and verification evidence.
- Mark missing capability as `unavailable`, `unknown`, or `blocked`.

## Forbidden

- Do not probe all host subagent tools automatically.
- Do not call a subagent or external Agent from AgentPal.
- Do not claim AgentPal activated a child workflow.
- Do not describe handoff packages as automatic multi-Agent execution.
- Do not convert unavailable status into pass.

## Required Evidence Before Use

- host Runtime name;
- current availability evidence;
- permission boundary;
- context that may be shared;
- context that must not be shared;
- required final report;
- verifier or verification plan;
- fallback when unavailable.

## Fallback

When unavailable, unknown, or blocked:

1. Produce a manual handoff package if useful.
2. Mark execution as `not-run`.
3. Preserve missing evidence.
4. Recommend a future host Runtime recheck only as a candidate, not a fixed route.
