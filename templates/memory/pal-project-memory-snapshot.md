# Pal Project Memory Snapshot

This template summarizes what a Pal needs to continue the same project across host Runtimes.

It is not a full private chat history, not a database record, and not proof that the current Runtime has the same capabilities as a previous Runtime.

```yaml
schema: agentpal.pal_project_memory_snapshot.v0.1
snapshot_id: ""
created_at: ""
pal_id: ""
project_id: ""
project_goal: ""
current_state: ""
recent_tasks:
  - task_id: ""
    summary: ""
    runtime_used: ""
    outcome: ""
important_decisions:
  - decision: ""
    reason: ""
    date_or_round: ""
open_blockers:
  - blocker: ""
    owner_candidate: ""
    evidence_needed: []
known_risks:
  - risk: ""
    mitigation: ""
user_preferences_summary:
  - ""
runtime_history:
  - runtime_id: ""
    model_or_reasoning: ""
    capability_evidence: ""
    known_limits: []
verification_history:
  - verification_id: ""
    result: "" # pass | fail | partial | not-run | blocked
    evidence_summary: []
routing_summary:
  - record_id: ""
    lesson: ""
    not_a_fixed_route: true
next_recommended_steps:
  - ""
privacy_notes:
  public_safe: false
  contains_private_project_summary: true
  excludes_raw_chat_history: true
  excludes_credentials: true
  user_approval_required_before_sharing: true
```

## Rules

- Use this as a summary for cross-runtime project continuation.
- Do not include full private chat history.
- Do not include secrets, credentials, API keys, tokens, local absolute paths, or unauthorized user privacy.
- Keep `runtime_history` as history. It does not prove current Runtime availability.
- Keep `routing_summary` as candidate evidence. It must not become a fixed route.
