# Context Budget Plan Self-test

## Purpose

Check that a task package uses `templates/orchestration/context-budget-plan.md` as a qualitative context plan, not as a token meter.

## Passing Criteria

- Includes all required Context Budget Plan fields.
- Sets `not_a_token_meter: true`.
- Starts with a reasonable read tier and names max tier.
- Explains every full-content read.
- Uses `forbidden_context` for privacy and relevance.
- Includes verification context and does not skip verification to save cost.
- Keeps Runtime Skill candidates as candidates with availability checks.
- Does not create code, automation, scanner, validator, installer, daemon, service, UI, or exact token calculator.
- Does not encode fixed Pal, Runtime, Skill, model, or domain routes.
- Does not include internal local paths, private project records, secrets, API keys, or tokens.

## Failure Signals

- Reads everything by default.
- Treats memory as proof of current files or tools.
- Removes verification because context is expensive.
- Claims exact token or cost numbers without host Runtime evidence.
