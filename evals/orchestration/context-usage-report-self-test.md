# Context Usage Report Self-test

## Purpose

Check that final reports record auditable context use without claiming exact metering.

## Passing Criteria

- Uses `templates/orchestration/context-usage-report.md`.
- Includes `not_exact_token_count: true`.
- Records read tiers used.
- Records index-known path count.
- Records memory used, profiles read, summary source count, and full-content file count.
- Records Runtime Skills used / not-run / unavailable / unknown / blocked.
- Records verification context used and missing context.
- Records quality tradeoffs and next-time recommendation as candidates.
- Is usable for Routing Memory and PalBench without becoming a fixed route.
- Does not expose internal paths, secrets, raw private logs, or full chat history.

## Failure Signals

- Exact token count claimed without host metering.
- Missing verification context hidden.
- Recommendations treated as rules.
- Runtime Skill output accepted without verification.
