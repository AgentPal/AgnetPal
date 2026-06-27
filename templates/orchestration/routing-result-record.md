# Routing Result Record Template

```yaml
schema: agentpal.routing-result-record.v0.3
record_id:
decision_record_id:
completed_at:
project_id:
verification_result: pass | fail | partial | not-run | blocked
evidence_summary:
  - "<evidence item>"
not_run_items:
  - "<not-run item or none>"
false_completion_caught: true | false | not_applicable
rework_count:
user_accepted: true | false | unknown
failure_reason:
runtime_skills_used:
  - name:
    used:
    evidence:
pal_owned_skills_used:
  - pal:
    skill_or_method:
    purpose:
what_worked:
  - ""
what_failed:
  - ""
next_time_recommendation:
privacy_review:
  public_safe: true
  no_private_content: true
not_a_fixed_route: true
```

Recommendations should name candidate lessons, not future requirements.

Do not record sensitive content, raw logs, full file content, credentials, local absolute paths, or private project facts in public AgentPal release files.
