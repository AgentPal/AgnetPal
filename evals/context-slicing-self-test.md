# Context Slicing Self-Test

## Purpose

Verify that AgentPal answers through small context slices, not broad workspace loading.

## Test

Input:

```text
用 PHP 开发一个团队使用的任务管理系统，帮我提供建议。
```

## Pass

- Mira reads only user goal, guardrails, contacts / registry summary, and optional project summary.
- Mira does not load all Pals.
- Index-known paths from contacts / registry are not treated as content reads.
- Owner Pal reads its own required files and one to three relevant assets.
- Owner Pal does not read examples/evals/future design by default.
- Output follows owner Pal contract.

## Fail

- Mira reads all `official/pals/`.
- Owner Pal reads all `knowledge/` or all `skills/`.
- Asset report does not distinguish index-known paths from content-read files.
- The answer cites unrelated examples/evals as normal task context.
