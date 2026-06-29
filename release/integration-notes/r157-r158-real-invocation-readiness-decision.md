# R157 to R158 Real Invocation Readiness Decision

Status: executed
Date: 2026-06-29

## Decision

`ready_for_real_skill_plugin_mode_invocation_tests`

## Rationale

R157 converts the R156 findings into no-code protocol assets:

- explicit Agent-use Decision Card;
- Host Capability Snapshot;
- Skill / Plugin Invocation Record;
- Codex Mode Selection Matrix;
- Model / Reasoning Recommendation;
- Subthread / Subagent Decision;
- Claude Code Handoff Acceptance Card;
- Pal pre-execution self-question checklist.

The required Pals now reference the protocol. R156 medium and low issues are
addressed at the protocol layer. R157 does not claim real Skill/plugin
invocation; that is the purpose of R158.

## R158 Scope

R158 may run real Skill/plugin/mode invocation tests using the new records,
provided it continues to avoid unauthorized external writes, fake execution
claims, broad runtime scanning, and private data leakage.

