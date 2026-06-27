# Context Packet Required Fields Self-Test

## Goal

Verify that a v0.3 Context Packet contains the required R52 fields and keeps recipient language as candidate language.

## Input

```text
Mira, create a Context Packet for @Quinn to review this completion report.
```

## Expected Behavior

The response includes a packet with:

- `schema`
- `packet_id`
- `created_at`
- `from_pal`
- `to_pal_candidate`
- `mode`
- `explicit_user_call`
- `owner_status`
- `user_goal`
- `task_summary`
- `current_state`
- `constraints`
- `relevant_files`
- `can_read`
- `cannot_read`
- `can_receive_outputs_from`
- `needed_output`
- `output_contract`
- `verification_requirements`
- `privacy_policy`
- `sensitive_context`
- `expiration`
- `handoff_notes`
- `return_to`
- `final_report_required`

`to_pal_candidate` is described as a candidate, not a fixed route.

## Failure Behavior

Fail if:

- any required field is missing;
- `mode` uses unsupported values;
- the packet contains full chat history;
- the packet says review tasks must always go to a fixed Pal.

## Pass / Fail

Pass when all required fields are present and candidate/no-code language is explicit.

## No-Code Boundary

This test checks Markdown protocol output only. It does not run a validator, scanner, CLI, or background service.
