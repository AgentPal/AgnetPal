# R158 Claude Code Handoff Acceptance Results

Status: minimal-real-call-pass-not-full-host-acceptance
Date: 2026-06-29

## Acceptance Card

| Field | Value |
| --- | --- |
| `claude_code_installed` | yes |
| `installed_evidence` | `claude --version` returned `2.1.150 (Claude Code)` |
| `minimal_call_evidence` | `claude --bare --tools "" --max-budget-usd 0.05 -p ...` returned `R158 Claude Code minimal handoff call ok` |
| `full_host_acceptance_status` | not-run |
| `project_path` | not-run for a full Claude project task |
| `agentpal_workspace_path` | not-run for full Claude acceptance |
| `thin_binding_status` | New1 checked by Codex controller; not a Claude full-host test |
| `required_files_to_read` | not-run |
| `task_goal` | minimal handoff call only |
| `allowed_actions` | no-tool print call |
| `forbidden_actions` | no git remote, no external writes, no broad scan |
| `mcp_tool_assumptions` | none |
| `expected_output` | exact single-line confirmation |
| `evidence_required` | command output captured in `fixtures/r158/claude-minimal-call-evidence.json` |
| `return_to_mira_summary` | Claude Code can answer a minimal no-tool prompt in this machine |
| `quinn_verification_checklist` | minimal call evidence present; full AgentPal host acceptance not claimed |

## Boundary

This result must not be upgraded to a full Claude Code AgentPal host pass. It proves only that the local `claude` command can start and answer a minimal no-tool prompt.

Generic CLI Agent remains `not-run, not blocking Codex-first release`.

