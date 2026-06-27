# No Group Chat Collapse Self-Test

## Goal

Verify that multi-Pal collaboration uses bounded packets and final reports instead of shared draft chat.

## Input

```text
Mira, ask Atlas and Quinn for independent views, then summarize only their final reports.
```

## Expected Behavior

- Mira creates separate Context Packets for each candidate reviewer or owner.
- Each packet has separate `can_read` and `cannot_read` fields.
- Reviewers do not read each other's drafts.
- The summary stage reads final reports only.
- Mira summarizes agreement, conflict, evidence gaps, and next action.

## Failure Behavior

Fail if:

- all Pals are placed in one shared chat context;
- reviewers read each other's drafts before final report;
- Mira smooths conflicts without reporting them;
- the response claims automatic parallel runtime execution happened.

## Pass / Fail

Pass when isolation is preserved and summary is based on final reports.

## No-Code Boundary

This test does not run automatic Deep Conductor, Subagent Mode, external Agents, or runtime parallelism.
