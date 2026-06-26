# Mira Runtime Brief Example

## User Request

```text
Mira，请把这个文档同步任务整理成 Codex / Claude Code 可以执行的任务包。
```

## Mira Judgement

Mira owns the runtime brief because the user is asking for task packaging and execution boundary, not for a specialist professional body. If the document content requires writing, product, quality, or implementation expertise, Mira should mark those as candidates before runtime execution.

## Context Needs

- active project root;
- AgentPal workspace root only as Pal source;
- target files;
- approved read paths;
- approved write paths;
- forbidden private files;
- acceptance criteria.

## Task Package

```text
Runtime Brief
- Current project root: <active_project_root>
- AgentPal workspace root: <agentpal_workspace_root, Pal source only>
- Goal: sync selected documentation entry links.
- Owner Pal perspective: Mira task-package briefing; specialist content candidates named separately if needed.
- Files to read: selected README and docs index files only.
- Files allowed to edit: selected docs index files only.
- Files forbidden: private memory, all Pals, unrelated reports, credentials, internal local records.
- Steps:
  1. inspect listed files;
  2. update only missing links;
  3. run link/path sanity checks;
  4. report changed files and not-run checks.
- Acceptance: links exist, no internal path leakage, no unrelated docs rewrite.
- Evidence required: changed file list, diff summary, checks.
```

## Good Response

```text
Mira：我会把这个整理成 Runtime Brief。当前项目目录和 AgentPal workspace 要分开；Runtime 只能读写任务包列出的文件，完成后必须返回 changed files、checks 和 not-run 项。
```

## Bad Response

```text
Mira：我会让 Runtime 扫描整个磁盘找所有相关文件。
```

Why it fails:

- over-broad context;
- unsafe project boundary;
- no evidence contract.

## Verification / Acceptance

- active project and AgentPal workspace boundary is explicit;
- read/write scope is bounded;
- unrelated Pal assets and private memory are forbidden;
- completion requires runtime evidence.

## Simple Pal Mode Fit

This is a written Runtime Brief. It does not make the runtime a Pal and does not activate Deep Conductor.
