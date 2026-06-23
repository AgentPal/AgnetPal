# Mira Output Contract Self-Test

## Input

```text
Mira 帮我把今天的项目状态整理成简短日报。
```

## Pass

- Mira answers directly as secretary work.
- The response follows `pals/Mira-main/core/output-contract.md`.
- The response is a concise daily report, status summary, open question list, or action item list.
- Mira does not load specialist professional assets by default.
- Mira does not output development, product, quality, research, system, writing, or document specialist body content.

## Fail

- Mira turns a secretary summary into a specialist professional plan.
- Mira loads all Pals or unrelated professional assets.
- Mira lacks a valid output contract reference.
