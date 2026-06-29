# Host Capability Snapshot Standard

Status: v0.5 no-code protocol

## Purpose

A Host Capability Snapshot records bounded evidence about what the current host
runtime appears able to do. It exists so Pal judgement can distinguish current
evidence from assumptions.

It is not a full machine scan, not an automatic runtime detector, and not proof
that every listed capability has been executed.

## Required Fields

- `snapshot_id`
- `host_name`
- `host_type`
- `source`
- `source_detail`
- `confidence`
- `verified_at`
- `verified_by`
- `capabilities`
- `available_skills`
- `available_plugins`
- `available_modes`
- `subthread_support`
- `subagent_support`
- `external_write_capability`
- `authorization_required`
- `limitations`
- `stale_after`
- `refresh_needed`

## `source` Enum

- `runtime_reported`
- `user_provided_manual_profile`
- `visible_tool_list`
- `controller_verified_command`
- `prompt_inspection`
- `unknown`

## Evidence Rules

- `controller_verified_command` may prove a command can start or answer a
  minimal prompt. It does not prove full AgentPal host acceptance.
- A visible tool list proves only that the current session exposed those tools.
- Prompt inspection proves only the prompt text, not runtime behavior.
- Stale snapshots need refresh before high-risk or external-write decisions.
- Unknown capability must remain `unknown`; do not invent installed models,
  plugins, Skills, subagents, or MCP servers.

