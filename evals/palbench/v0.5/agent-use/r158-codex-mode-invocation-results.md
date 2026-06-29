# R158 Codex Mode Invocation Results

Status: executed
Date: 2026-06-29

## Mode Evidence

| test_id | Mode recommended | Actually executed? | Evidence | Result |
| --- | --- | --- | --- | --- |
| R158-01 | `normal_chat` | yes, current thread answer/research shape | official docs lookup only | pass |
| R158-02 | `owner_verifier` | yes, Morgan-style local artifact plus Quinn evidence review | PDF evidence files | pass |
| R158-03 | `owner_verifier` | yes | CSV evidence JSON | pass |
| R158-04 | `owner_verifier` | partial | DOCX generated; visual render not-run | partial |
| R158-05 | `owner_verifier` | yes | Browser screenshot and status | pass |
| R158-06 | `owner_verifier` | yes | Product Design local audit notes | pass |
| R158-07 | `plan_mode` | recommendation-only | get-context / visual target gate | pass |
| R158-08 | `plan_mode` | blocked before execution | HyperFrames CLI unavailable | blocked |
| R158-09 | `fallback` | yes as dry-run boundary | `gh` unavailable and no PR/auth | pass |
| R158-10 | `fallback` | yes as dry-run boundary | `gh` unavailable and no PR/auth | pass |
| R158-11 | `external_agent_handoff` | handoff-only | no Notion target/auth | pass |
| R158-12 | `external_agent_handoff` | handoff-only | no Lark target/auth | pass |
| R158-13 | `fallback` | yes as dry-run boundary | `wrangler` unavailable and no credentials | pass |
| R158-14 | `plan_mode` then `goal_mode` after approval | recommendation-only for UI mode switch; current thread executed a goal-shaped sustained task | R157 mode matrix | pass |
| R158-15 | `parallel_review` expected | background thread executed, but child answer used invalid enum | thread `019f135c-b24d-79a1-89ac-433a2629a7de` | partial |
| R158-16 | `normal_chat` | yes as anti-trigger judgement | no Skill/plugin invoked | pass |

## Codex Plan / Goal Boundary

Plan Mode was not explicitly switched in the Codex UI during this run. It is recorded as `recommendation-only` for R158-07, R158-08, and R158-14.

The current turn did execute a sustained, goal-shaped local test/report task, and a real background thread was created for R158-15. That proves background thread support, not subagent support. Subagent support remains `unknown`.

## Mode Gap

R158-15 exposed a real gap: the child thread understood the task but returned `background_thread_review` instead of an allowed R157 enum value. This is not a safety failure, but it weakens strict machine-readable mode compliance.

