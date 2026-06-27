# Routing Memory Guided Runtime Selection Example

## User Input

```text
Last time a similar task worked better in Claude Code. Should we use it again?
```

## Previous Memory

```yaml
schema: agentpal.routing_memory_record.v0.1
runtime_candidates:
  - runtime: codex
    reason: "Available in previous planning session."
  - runtime: claude-code
    reason: "Handled project-local edits after binding was verified."
runtime_selected:
  runtime: claude-code
verification_result: pass
what_worked:
  - "Project-local file edits returned clear evidence."
next_time_recommendation: "Consider Claude Code again if current project binding is verified."
not_a_fixed_route: true
```

## Current Runtime

The current runtime is unknown until the host reports evidence.

## Memory Snapshot

Routing Memory is read as a summary only. It does not prove that Claude Code is currently open, configured, authorized, or able to read the same files.

## Deep Conductor Decision

Selected topology: Capability-aware Task Package with Runtime candidate review.

Reason: previous success makes Claude Code a candidate, but current availability must be verified.

## Task Package

```yaml
runtime_candidates:
  - runtime: claude-code
    reason: "Prior verified success for similar project-local edit."
    current_evidence_required: true
  - runtime: current-host
    reason: "May already have required access."
    current_evidence_required: true
not_a_fixed_route: true
```

## Verification Plan

- Confirm current Runtime and project binding.
- Confirm file access before edit.
- Report Runtime Skill candidates as available, unavailable, or not-run.

## Memory Writeback Candidate

After completion, update the Routing Memory with what actually happened this time. Do not overwrite the record into a fixed rule.

## No-Code Boundary Note

This example does not start Claude Code, route automatically, or create a scheduler.
