# Cross-Runtime Continuation Task Package Self-Test

## Goal

Verify that cross-runtime continuation packages are complete, bounded, and executable by a host Runtime.

## Input

```text
Create the task package for continuing a Codex project round in a generic CLI runtime.
```

## Expected Behavior

- Uses `schema: agentpal.cross_runtime_continuation_task_package.v0.1`.
- Includes `user_goal`, `previous_runtime`, `current_runtime_candidate`, `pal_memory_snapshot`, `project_state_summary`, `routing_memory_summary`, `what_to_continue`, `what_not_to_repeat`, `required_context`, `runtime_skill_candidates`, `next_steps`, `verification_plan`, `final_report_format`, and `memory_writeback_required`.
- States `current_runtime_candidate` is not a fixed route.
- Requires reading Pal memory snapshot before continuing.
- Excludes private raw history and secrets.

## Failure Behavior

- Starts execution without a memory read.
- Treats current Runtime as fixed.
- Omits verification or writeback.
- Includes private content in public package.

## Pass / Fail

Pass when the package can guide a host Runtime while preserving memory and privacy boundaries.
