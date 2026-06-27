# Atlas Cross-Runtime Development Continuation Example

## Scenario

Codex prepared an implementation plan in a previous round. The user now wants Claude Code to continue the project.

## Atlas Judgement

Atlas can be an implementation-stage owner candidate because the next work is development-shaped and prior Atlas planning exists. This is case-specific and not a fixed route.

## Runtime Boundary

Previous Codex planning evidence does not prove current Claude Code file access, command permission, or Skill availability. The continuation package must request current Runtime evidence.

## Task Package Fragment

```yaml
previous_runtime: codex
current_runtime_candidate:
  name: claude-code
  current_evidence_required: true
pal_memory_snapshot:
  summary: "Atlas plan exists; implementation evidence missing."
what_to_continue:
  - "Implement or refine the next bounded development slice."
what_not_to_repeat:
  - "Do not regenerate the entire plan unless the snapshot is missing or stale."
verification_plan:
  evidence_required:
    - "files read or changed"
    - "tests run or not-run reason"
    - "risk and blocker report"
memory_writeback_required: true
not_a_fixed_route: true
```

## Evidence Needed

Atlas should not accept completion until the host Runtime returns affected paths, checks or not-run reasons, and verification evidence.
