# Codex Mode Selection Matrix

Status: v0.5 no-code protocol

## Modes

| codex_mode | Use when | Avoid when |
| --- | --- | --- |
| `normal_chat` | Short answers, simple rewrite, explanation, low-risk advice, no file/action needed | Multi-step execution, unclear risk, external writes, broad verification |
| `plan_mode` | User needs design, scope, risk review, approval, or task package before edits | User explicitly asks for immediate low-risk answer |
| `goal_mode` | Sustained implementation, verification, reports, or multi-step local work is authorized | Trivial writing, pure explanation, missing repo/scope |
| `owner_verifier` | One owner can execute or package work and independent evidence review adds value | No evidence target exists or verifier would only repeat owner claim |
| `parallel_review` | Independent reviews of separate artifacts or options improve quality | Customer-private data cannot be safely partitioned or host support is unknown |
| `sequential_chain` | Work must flow through ordered stages such as research -> plan -> implementation -> verification | Single-step work or when stages are artificial |
| `external_agent_handoff` | Another host such as Claude Code is a better fit and capability evidence or user instruction exists | The external host is unknown, unverified, or lacks user authorization |
| `fallback` | Capability unknown, host unavailable, safety boundary blocks execution, or no registered Pal clearly owns it | A normal Pal/host path is available |

## Required Anti-examples

- Simple sentence rewriting should not use `goal_mode`.
- Pure explanation should not start multi-Pal or subagent workflows.
- Customer-private data should not default to `parallel_review`; use a Context
  Access List first.
- Unknown capability must not become claimed subagent availability.
- External writes must not execute without authorization, even when a plugin is visible.

## Output Rule

When a task may use Codex as an execution layer, name `codex_mode` explicitly
from the enum and add `codex_mode_reason`.

