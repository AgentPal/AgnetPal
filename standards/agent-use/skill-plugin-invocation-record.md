# Skill / Plugin Invocation Record Standard

Status: v0.5 no-code protocol

## Purpose

The Skill / Plugin Invocation Record is the R158-ready evidence shape for
recording whether a host Skill, plugin, MCP tool, or comparable runtime
capability was actually invoked, dry-run, only inspected, handed off, skipped,
or blocked.

It prevents candidate recommendations from being mistaken for execution.

## Required Fields

- `invocation_id`
- `task_id`
- `skill_or_plugin`
- `capability_source`
- `intended_use`
- `preconditions`
- `input_summary`
- `authorization_status`
- `invocation_type`
- `invoked`
- `dry_run`
- `output_summary`
- `evidence_path`
- `failure_or_skip_reason`
- `why_this_skill`
- `why_not_other_skills`
- `privacy_boundary`
- `external_write_boundary`
- `verifier`
- `result_status`

## `invocation_type` Enum

- `real_call`
- `dry_run`
- `handoff_only`
- `prompt_inspection`
- `not_invoked`
- `blocked`

## Rules

- `invoked = yes` requires current runtime evidence.
- `dry_run = yes` must say what was simulated or inspected and what was not.
- External writes require explicit authorization and a boundary statement.
- Private customer data must not be copied into public examples or reusable
  Pal Pack assets.
- A verifier should check evidence for high-risk or release-facing results.

