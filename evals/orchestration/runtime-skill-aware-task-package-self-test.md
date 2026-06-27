# Runtime Skill-aware Task Package Self-Test

## Purpose

Verify that Runtime Skill-aware packages separate host Runtime capabilities from Pal methods.

## Pass Criteria

- Required YAML fields are present: `schema`, `task_id`, `user_goal`, `owner_pal`, `runtime_candidate`, `runtime_skill_candidates`, `runtime_skill_usage_reason`, `pal_owned_skills_used`, `required_inputs`, `allowed_files`, `cannot_read`, `execution_steps`, `prompt_shaping_notes`, `verification_requirements`, `expected_outputs`, `final_report_required`, and `routing_memory_writeback`.
- `runtime_skill_candidates` are installed host Skill candidates, not Pal methods.
- `pal_owned_skills_used` are Pal methods, workflows, runbooks, or output contracts.
- Candidate wording remains non-binding.
- Verification requirements name evidence and `not-run` reporting.
- No fixed route or keyword route is introduced.
- No internal path or private project data appears.

## Fail Criteria

- The package implies AgentPal installs or invokes Runtime Skills.
- The package omits final report or routing memory writeback requirements.
