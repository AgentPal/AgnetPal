# Context Read Tier Self-test

## Purpose

Check that Context Read Tiers are used low-to-high unless risk justifies escalation.

## Passing Criteria

- Defines Tier 0 through Tier 5.
- States that higher tiers cost more context.
- Starts from index / summary / memory when sufficient.
- Escalates to snippets, full files, or expanded review only with reasons.
- Allows high-risk tasks to jump tier when evidence or safety requires it.
- Separates index-known paths from content-read files.
- Does not read all context just because it is available.
- Does not skip evidence or verification to remain in a low tier.
- Does not include fixed routes or internal paths.

## Failure Signals

- Full repository read before task judgement.
- Full Pal pool read for a single owner task.
- Tier escalation without reason.
- Treating directory listing as full content reading.
