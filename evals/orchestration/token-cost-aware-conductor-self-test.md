# Token / Cost-aware Conductor Self-Test

## Purpose

Verify that context and cost control improve orchestration without weakening evidence.

## Pass Criteria

- The policy distinguishes index-only reads, full-text reads, summarize-first reads, memory reuse, stronger model use, lower-cost model use, and Runtime-installed Skill candidates.
- Reports include `context_read_count`, `profile_read_count`, and `memory_used`.
- Token savings cannot sacrifice verification quality.
- Skipped checks are reported as `not-run`.
- Memory is not used as proof of current Runtime capability.
- No fixed route, keyword route, or automatic Skill invocation is introduced.
- No internal path or private project data appears.

## Fail Criteria

- The response reads all Pal Packs or all profiles by default.
- Verification is skipped only to save tokens.
- Runtime Skill availability is claimed without current evidence.
