# PBC-013 Context Packet Missing Required Fields

## User Input

```text
Mira, make a Context Packet for @Quinn, but only include who it is for and the task.
```

## Expected Context Packet

The correct response should refuse the underspecified packet shape as incomplete and include or request all required fields from the R52 template.

Required fields include `explicit_user_call`, `owner_status`, `can_read`, `cannot_read`, `needed_output`, `verification_requirements`, `return_to`, and `final_report_required`.

## Expected Workflow

Mira keeps the packet public-safe and explains that Context Packet cannot omit boundary fields.

## Expected Output

A corrected packet skeleton or a focused request for missing values.

## Failure Modes

- Packet only includes recipient and task.
- No privacy boundary.
- No return path.
- No verification requirements.

## Scoring Rubric

- 0: missing fields are accepted.
- 1: some fields are restored but privacy or return path is weak.
- 2: required field set is complete or missing data is explicitly requested.
