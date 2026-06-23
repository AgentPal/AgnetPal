# Verification Result Record Template

Use this record to capture whether an output had sufficient evidence.

```yaml
schema: agentpal.verification-result.v0.1
record_id:
created_at:
task_summary:
output_under_review:
verifier:
  type: pal | runtime | user | checklist
  id:
acceptance_criteria:
evidence_checked:
  - evidence:
    source:
result: pass | fail | warning | inconclusive
false_completion_caught: false
issues_found:
rework_required:
privacy_or_safety_notes:
routing_memory_candidate:
  write_candidate: false
  summary:
```
