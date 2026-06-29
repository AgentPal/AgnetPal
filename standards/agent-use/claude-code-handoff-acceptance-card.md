# Claude Code Handoff Acceptance Card Standard

Status: v0.5 no-code protocol

## Purpose

This card records whether a task is ready to be handed to Claude Code and what
evidence is needed for AgentPal to accept the result later.

## Required Fields

- `claude_code_installed`
- `installed_evidence`
- `minimal_call_evidence`
- `full_host_acceptance_status`
- `project_path`
- `agentpal_workspace_path`
- `thin_binding_status`
- `required_files_to_read`
- `task_goal`
- `allowed_actions`
- `forbidden_actions`
- `mcp_tool_assumptions`
- `expected_output`
- `evidence_required`
- `return_to_mira_summary`
- `quinn_verification_checklist`

## Boundary

`claude --bare -p` success is minimal real-call evidence only. It does not prove:

- AgentPal initialization in Claude Code;
- project binding correctness;
- Pal routing;
- MCP/tool availability;
- subagent support;
- full host acceptance.

Full pass requires a real project task, a Claude Code answer, evidence returned
to Mira or Quinn, and verification against the original acceptance criteria.

