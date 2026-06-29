# R156 to R157 Agent Use Decision

Status: executed
Date: 2026-06-29

## Decision

`agent_use_partner_real_task_pass_with_minor_mode_label_gaps`

## Rationale

R156 performed real host operations instead of simulated conversation:

- Confirmed Codex project list and created real Codex background threads.
- Submitted the 18 R156 task prompts to real Codex threads.
- Received final task-level answers for all 18 prompts.
- Confirmed Claude Code exists and completed a minimal no-tool non-interactive call.
- Confirmed `New1` remains thin binding only.

The tested Pal generally behaved as an Agent-use partner. It chose or proposed Pal owners, Agent host, Codex mode shape, model/reasoning level, visible Skill/plugin, subthread/subagent shape, authorization boundary, and why-not-use constraints.

## Release Interpretation

- R155 Codex-first real host confirmation remains valid.
- R156 Agent-use-partner behavior passes with minor gaps.
- Claude Code is upgraded from R155 `not-run` to R156 `minimal-real-call-pass`, but not full AgentPal host acceptance.
- Generic CLI Agent remains `not-run, not blocking Codex-first release`.

## R157 Recommendation

R157 should focus on optimization rather than a blocking repair:

1. Make Codex mode labels explicit: normal, Plan Mode, Goal Mode, owner+verifier, parallel review.
2. Add a Host Capability Snapshot so verified commands like Claude Code can be passed into tested Pal judgement.
3. Add a quick-answer path for broad Agent-use advice before optional Skill-doc reads.
4. Run a dedicated Claude Code AgentPal prompt-card acceptance test.
