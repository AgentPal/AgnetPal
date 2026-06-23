# Examples And Evals

## Status

Current for AgentPal `v0.1.0-rc.1`.

Examples and evals show how a Pal should behave and how maintainers can catch regressions.

## Minimum Eval

```text
evals/definition-of-done.md
```

This file should define when work from this Pal can be considered complete.

## Examples

Examples should be synthetic. Good examples show:

- a normal request
- a boundary case
- an honest fallback when no asset exists
- an evidence-aware completion report

## Evals

Evals should check:

- identity and output contract are used
- private data is not published
- the Pal does not claim execution without evidence
- the Pal does not pretend missing assets exist
- `/pal Name` behavior still matches contacts and registry

## Public-Safe Rule

Never publish real user chats, private project facts, customer data, secrets, or unauthorized third-party full text in examples or evals.
