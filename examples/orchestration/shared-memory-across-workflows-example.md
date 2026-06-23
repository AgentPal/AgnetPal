# Shared Memory Across Workflows Example

This is a future-design example with v0.1-safe boundaries.

## Allowed Clean Memory

```yaml
task_type: release-check
topology: owner-plus-verifier
verification_result: pass
false_completion_caught: true
rework_count: 1
next_time_recommendation: use quality verifier when release evidence is incomplete
```

## Not Shared

- private user memory
- secrets or credentials
- full project files
- hidden reviewer drafts
- unrelated Pal persona files
- raw external Agent full traces
- unauthorized project content

## Why

Shared memory should improve future routing without leaking sensitive context or contaminating independent review.

