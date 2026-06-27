# Routing Result Record Template

```yaml
schema: agentpal.routing-result-record.v0.3
record_id:
decision_record_id:
completed_at:
verification_result: pass | fail | partial | not-run | blocked
evidence_summary:
  - "<evidence item>"
not_run_items:
  - "<not-run item or none>"
false_completion_caught: true | false | not_applicable
rework_count:
user_accepted: true | false | unknown
failure_reason:
next_time_recommendation:
privacy_review:
  public_safe: true
  no_private_content: true
not_a_fixed_route: true
```

Recommendations should name candidate lessons, not future requirements.
