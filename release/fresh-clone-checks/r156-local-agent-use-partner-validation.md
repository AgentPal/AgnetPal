# R156 Local Agent Use Partner Validation

Status: executed
Date: 2026-06-29

## Validation Checks

| Check | Result | Evidence |
| --- | --- | --- |
| `git status --short --branch` before edits | pass | Source worktree was clean and ahead of origin before R156 edits. |
| JSON parse: `agentpal.json` | pass | `ConvertFrom-Json` succeeded. |
| JSON parse: `workspace/organization/contacts/pals.json` | pass | `ConvertFrom-Json` succeeded. |
| JSON parse: `workspace/organization/contacts/aliases.json` | pass | `ConvertFrom-Json -AsHashtable` succeeded; default parser reports casing duplicate because both `Faye` and `faye` are valid aliases. |
| Central roster active count | pass | 10 active registered Pals. |
| Official Pal directory count | pass | 10 directories under `official/pals`. |
| Official `pal.json` parse | pass | 10 parsed, 0 failures. |
| R156 output files present | pass | All 8 required R156 files exist after write validation. |
| New1 thin binding | pass | `.agentpal` contains only `AGENTPAL.md` and `project.json`. |
| Codex real threads | pass | 3 real Codex background threads created and completed. |
| R156 real prompts | pass | 18 task prompts submitted and answered in real Codex thread. |
| Claude Code real call | pass-minimal | `claude --bare -p` returned `Claude Code real call ok`. |
| No GitHub/Notion/Lark/Cloudflare writes | pass | No write commands or connector write calls executed. |
| No git push/pull/fetch/tag/GitHub Release | pass | No such commands executed in R156. |
| Claude Code not falsely claimed | pass | Marked minimal real call only, not full host pass. |
| Generic CLI not falsely claimed | pass | Marked not-run. |

## Required R156 Files

- `evals/palbench/v0.5/agent-use/r156-agent-use-partner-real-task-test-plan.md`
- `evals/palbench/v0.5/agent-use/r156-agent-use-partner-real-task-results.md`
- `evals/palbench/v0.5/agent-use/r156-agent-use-partner-issues.md`
- `evals/palbench/v0.5/agent-use/r156-codex-mode-skill-plugin-trigger-matrix.md`
- `evals/palbench/v0.5/agent-use/r156-claude-code-real-call-results.md`
- `evals/palbench/v0.5/agent-use/r156-agent-use-optimization-backlog.md`
- `release/fresh-clone-checks/r156-local-agent-use-partner-validation.md`
- `release/integration-notes/r156-r157-agent-use-decision.md`

## Decision

Validation decision: `agent_use_partner_real_task_pass_with_minor_mode_label_gaps`.
