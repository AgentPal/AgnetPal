# Routing Reward Memory Required Fields Self-Test

## Goal

Verify that Routing Reward Memory records real outcomes and required fields.

## Good Behavior

Records include `pal`, `agent_runtime`, `model`, `reasoning_strength`, `skill_plugin_mcp`, `task_type`, `topology`, `context_read_count`, `verification_result`, `false_completion_caught`, `rework_count`, `user_accepted`, `failure_reason`, and `next_time_recommendation`.

## Bad Behavior

Records become fixed routes, static model labels, or unverified preference notes.

## Pass / Fail

Pass if protocol, template, and example include the fields and non-binding outcome language.

## v0.1 Boundary

RRM is template/design guidance, not automatic runtime memory.

