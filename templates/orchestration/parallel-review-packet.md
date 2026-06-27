# Parallel Independent Review Packet

```yaml
schema: agentpal.parallel-review-packet.v0.3
workflow_id:
created_at:
review_topic:
summary_owner_candidate: Mira
reviewers:
  - reviewer_id:
    reviewer_candidate:
    review_focus:
    context_packet:
      can_read:
        - "<allowed context>"
      cannot_read:
        - "other reviewer drafts"
        - "private memory"
        - "secrets"
      needed_output: "independent final report"
      output_contract:
        - judgement
        - evidence
        - assumptions
        - risks
        - recommendation
        - confidence
summary_stage:
  can_read:
    - "reviewer final reports"
  cannot_read:
    - "reviewer drafts"
    - "hidden reasoning"
  needed_output:
    - agreements
    - conflicts
    - evidence gaps
    - recommendation
boundary:
  no_group_chat: true
  no_automatic_parallel_execution: true
  candidates_not_fixed_routes: true
```
