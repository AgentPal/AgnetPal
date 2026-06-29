# Agent-use Decision Card Standard

Status: v0.5 no-code protocol

## Purpose

The Agent-use Decision Card is the pre-execution judgement record for tasks
where a Pal may recommend an Agent host, Codex mode, model class, reasoning
strength, Skill, plugin, subthread, subagent, external Agent handoff, Context
Packet, or Task Package.

It is a decision aid and evidence boundary. It is not proof that anything was
executed.

## Required Fields

- `task_summary`
- `user_goal`
- `missing_information`
- `risk_level`
- `privacy_or_external_write_risk`
- `owner_pal`
- `verifier_pal`
- `candidate_collaborators`
- `agent_host_recommendation`
- `host_capability_source`
- `codex_mode`
- `codex_mode_reason`
- `model_class_recommendation`
- `reasoning_strength`
- `skill_plugin_candidates`
- `skill_plugin_invocation_plan`
- `skill_plugin_non_use_reason`
- `subthread_subagent_decision`
- `subthread_subagent_reason`
- `context_packet_required`
- `task_package_required`
- `authorization_required`
- `next_action`
- `confidence`
- `residual_risks`

## `codex_mode` Enum

Use one of these exact values:

- `normal_chat`
- `plan_mode`
- `goal_mode`
- `owner_verifier`
- `parallel_review`
- `sequential_chain`
- `external_agent_handoff`
- `fallback`

## Rules

- Pal recommendations are AI judgement inputs, not deterministic routes.
- Do not create keyword routes from task words to Pal owners, Skills, plugins,
  modes, or Agents.
- If a host capability is unknown, say `unknown` or request a Host Capability
  Snapshot.
- A Skill/plugin candidate is not an invocation claim.
- External writes, publishing, credential access, customer data movement, and
  high-risk local changes require explicit authorization.
- Simple tasks should normally use `normal_chat` or Fast Route, not heavy modes.

## Quick-answer Path

For broad Agent-use advice, Mira may fill a compact Decision Card from visible
capability evidence first, then ask whether the user wants deeper Skill/plugin
document inspection. This prevents capability advice from becoming a slow
workspace-wide read.

