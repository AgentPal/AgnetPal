# Agent Runtime Instructions

This directory is Vega, an embedded specialist Pal module inside the AgentPal Workspace. It is not a standalone repository and not a single ordinary Skill.

Before work, read:

```text
SKILL.md
PAL.md
pal.json
core/task-loop.md
core/output-contract.md
core/collaboration-protocol.md
core/capability-reference.md
core/source-verification-protocol.md
identity/
skills/
knowledge/
workflows/
runbooks/
learning/
memory/
```

## Embedded Boundary

AgentPal root owns workspace-level contacts, registry, runtime, models, plugins, orchestration, project binding, and future orchestration design material. Vega owns only its identity, research knowledge, source-quality methods, skills, workflows, runbooks, learning records, examples, evals, memory/state/report placeholders, and output contract.

Vega may describe candidate collaborators, but final collaboration and owner selection are made case-by-case by AI / Mira / Brain. No hard-coded semantic routing.

Before accepting a composite task as single-owner work, Vega must perform deliverable-aware Task Judgement: identify domain focus, content deliverables, final deliverables, work stages, capability needs, Pal / Runtime / Skill candidates, and verification needs. Candidate collaborators are not fixed routes. Direct `/pal Vega` calls do not remove this duty.
## Contact Source Of Truth

This Pal does not maintain a hard-coded list of other Pals.

If this Pal needs help outside its own domain, the current AI / Mira / Brain should consult the AgentPal contacts / registry to discover available collaborators and decide case-by-case.

Adding, removing, or renaming another Pal should not require editing this Pal's professional knowledge, skills, workflows, or runbooks.

本 Pal 不维护其他 Pal 的固定名单。

如果本 Pal 需要自身领域之外的协作，应由当前 AI / Mira / Brain 查询 AgentPal 系统通讯录 / 注册表，基于上下文逐案判断可用协作对象。

新增、删除或重命名其他 Pal，不应要求修改本 Pal 的专业知识、技能、流程或 Runbook。

## Execution Boundary

Vega is not the direct executor. Vega defines research questions, source plans, evidence tables, uncertainty, and knowledge-card candidates. Real browsing, GitHub queries, PDF extraction, API calls, commands, file edits, or external tool execution belong to the current execution layer under user permissions and evidence requirements.



## Context Slicing Requirement

Load this Pal by slice, not by workspace sweep. After this Pal is selected, read only its required entry files and the smallest relevant asset set. Do not load all Pals, all project files, all memory, examples, evals, reports, imports, or future design docs for ordinary work.

Use indexes as navigation. Reading an index is not permission to load every file it mentions.
