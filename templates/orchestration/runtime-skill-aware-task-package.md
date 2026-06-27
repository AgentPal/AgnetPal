# Runtime Skill-aware Task Package

This template keeps Pal-owned Skills separate from Runtime-installed Skills.

`runtime_skill_candidates` are installed host Runtime Skill candidates. They may include Agent Skills, plugins, MCP tools, browser tools, office-document tools, repository analysis tools, or other host capabilities. They are candidates, not fixed routes, and must be verified by the current Runtime.

`pal_owned_skills_used` are Pal methods, workflows, runbooks, output contracts, or judgement skills used to prepare the package. They do not execute host tools.

```yaml
schema: agentpal.runtime_skill_aware_task_package.v0.1
task_id: example-task-id
user_goal: ""
owner_pal:
  name: ""
  reason: ""
runtime_candidate:
  name: ""
  reason: ""
  availability_evidence_required: true
runtime_skill_candidates:
  - name: ""
    type: "" # Agent Skill | plugin | MCP | browser | office document | repo analysis | other
    reason: ""
    required_inputs: []
    evidence_required: []
runtime_skill_usage_reason: ""
pal_owned_skills_used:
  - pal: ""
    skill_or_method: ""
    purpose: ""
required_inputs: []
allowed_files: []
cannot_read: []
execution_steps:
  - ""
prompt_shaping_notes:
  runtime_notes: ""
  model_notes: ""
  reasoning_notes: ""
  skill_notes: ""
verification_requirements:
  - ""
expected_outputs:
  - ""
final_report_required:
  required: true
  must_include:
    - files_changed_or_read
    - commands_or_tools_used
    - runtime_skills_used_or_not_run
    - verification_results
    - blockers
routing_memory_writeback:
  required: true
  fields:
    - task_type
    - owner_pal
    - runtime_candidate
    - runtime_skill_candidates
    - runtime_skills_used
    - pal_owned_skills_used
    - context_read_count
    - profile_read_count
    - memory_used
    - verification_result
    - rework_count
    - notes_for_next_time
```

## Use Rule

Use this template when a task may benefit from a host Runtime Skill, plugin, MCP tool, or special tool surface.

The package must not imply that AgentPal owns, installs, invokes, or verifies the Skill by itself.
