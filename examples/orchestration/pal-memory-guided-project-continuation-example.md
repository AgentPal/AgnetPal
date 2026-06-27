# Pal Memory Guided Project Continuation Example

## User Input

```text
Continue the project from the last Pal round. Use the Pal's memory and project state, but keep private details out of the handoff.
```

## Previous Memory

- Pal Project Memory Snapshot exists.
- Routing Memory says an Owner + Verifier topology reduced false completion in the previous round.
- Verification Memory says one check was blocked by missing evidence.

## Current Runtime

Current runtime candidate: generic CLI agent.

The runtime must prove it can read the project files and AgentPal core files before execution.

## Memory Snapshot

```yaml
schema: agentpal.pal_project_memory_snapshot.v0.1
pal_id: mira-main
project_goal: "Continue a multi-stage project."
current_state: "One planning round complete; one evidence check blocked."
open_blockers:
  - blocker: "Missing evidence for completion claim."
    evidence_needed:
      - "changed-file list"
      - "verification result"
user_preferences_summary:
  - "User prefers not to restart from zero."
privacy_notes:
  excludes_raw_chat_history: true
  user_approval_required_before_sharing: true
```

## Deep Conductor Decision

Selected topology: Project Conductor with memory read and verification-first next step.

Reason: memory identifies a blocked evidence gap, so the next task should gather evidence rather than repeat planning.

## Task Package

```yaml
schema: agentpal.next_round_runtime_task_package.v0.1
round_goal: "Gather evidence for the blocked continuation check."
previous_runtime_context:
  memory_snapshot_used: "snapshot summary"
  not_a_fixed_route: true
required_context:
  - "Pal Project Memory Snapshot summary"
  - "Verification Memory summary"
forbidden_context:
  - "raw private chat history"
verification_plan:
  evidence_required:
    - "actual files checked"
    - "not-run items"
memory_writeback_required:
  required: true
```

## Verification Plan

- The runtime reports exact evidence or `not-run`.
- Private data is absent from the package.
- Memory writeback candidate is prepared after evidence exists.

## Memory Writeback Candidate

Record whether the evidence-gathering step cleared the blocker. Keep the next-time lesson as a recommendation, not a rule.

## No-Code Boundary Note

The memory snapshot guides judgement only. AgentPal does not automatically query a database or sync runtime state.
