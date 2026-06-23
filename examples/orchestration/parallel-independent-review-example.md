# Parallel Independent Review Example

This is a future-design example.

## Situation

The user needs independent perspectives before making a decision.

## Shape

```text
Mira -> independent reviewers -> summary stage
```

## Isolation

Each reviewer receives a Context Access List and does not read other reviewer drafts before submitting.

Each reviewer receives only:

- its own task
- its own `can_read_paths`
- permitted summaries
- the requested output contract

Reviewers do not receive other reviewers' drafts, hidden process notes, unrelated Pal persona files, private memory, or raw external Agent traces.

## Summary

The summary stage starts only after independent reports exist. Mira or the owner Pal compares agreements, conflicts, evidence quality, and next actions from final reports.

## Failure Avoided

This avoids group-chat collapse where later reviewers simply follow the first answer.

AgentPal v0.1 does not run this as an active parallel workflow. It is a future Deep Conductor design example.
