# E2E User-Facing Short Summary

Use this before or alongside a detailed Deep Conductor E2E synthesis report.

The summary is for the user. It should be short, readable, and honest about `pass`, `partial`, `unavailable`, `blocked`, and `not-run` results. It must not replace detailed evidence when the task needs verification.

```yaml
schema: agentpal.e2e-user-facing-short-summary.v0.1
summary:
  result: <pass | partial | unavailable | fail | blocked | mixed | unknown>
  what_i_planned: []
  why_this_plan: ""
  what_needs_execution: []
  what_needs_verification: []
  what_i_did_not_do: []
  next_user_action: ""
  unavailable_or_partial_notes: []
boundary:
  agentpal_auto_execution_claimed: false
  unavailable_reported_as_pass: false
  partial_reported_as_fully_supported: false
  exact_token_or_cost_claimed: false
```

## Rules

- Lead with the result and next action.
- Keep YAML details optional for users who need audit trails.
- Preserve unavailable, blocked, and not-run states.
- Do not claim exact token savings unless the host Runtime provides exact metering evidence.
