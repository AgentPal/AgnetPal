# Memory

## Purpose

This directory stores public-safe durable memory summaries and memory policy
notes for Nova.

Memory stores extracted long-term lessons, product strategy preferences,
decision patterns, routing lessons, and continuity references. It is not a place
for full task reports.

## What belongs here

- Reviewed long-term lessons from Nova product and strategy work.
- Public-safe project, runtime, and tool-use memory summaries.
- Pointers to central project memory records.
- Product decision lessons after they are extracted and reviewed.
- Notes that preserve `unknown`, `missing`, or `not-run` evidence.

## What does not belong here

- Full completion reports, product audit reports, PRDs, or validation records.
- Raw evidence, file dumps, customer data, or current runtime state.
- Credentials, tokens, secrets, cookies, passwords, API keys, or private project
  data.
- Unapproved private user or project memory.
- External project `.agentpal/memory/` as a default target.
- Keyword routing maps or deterministic dispatch rules.

## Current assets

| Asset | Memory purpose | Status | Notes |
| --- | --- | --- | --- |
| `project/` | Project-related durable memory area | `present` | Store only approved summaries or central project-record pointers. |
| `runtime/` | Runtime evidence and product workflow memory area | `present` | Preserve `not-run`, `missing`, and runtime-availability boundaries. |
| `skill-memory/` | Skill-related memory candidates or durable lessons | `present` | Keep Agent Skill references as references unless rewritten as Pal-owned methods. |
| `user/` | User-facing preference or continuity memory area | `present` | Use only for approved, public-safe summaries. |

## Candidate memories / needs review

| Candidate | Source report / evidence | Review status |
| --- | --- | --- |
| Product scope-control lessons | Future completion reports | `needs-review` |
| Product handoff and acceptance lessons | Future verified task evidence | `needs-review` |

## Relationship to reports

Reports belong in `reports/`. A report becomes memory only after stable lessons
are extracted, reviewed, and summarized without private project details.

## Project-private memory boundary

Project-private memory belongs to AgentPal central project records, not external
project directories. Do not copy Nova memory into an external project's
`.agentpal/` tree by default.

## Related standards

- `standards/pal-asset/pal-asset-directory-standard.md`
- `templates/pal-asset/index-templates/memory-index-template.md`
- `templates/pal-asset/safe-index-backfill-guide.md`

## Public safety boundary

Do not store private user memory, private project memory, raw files, secrets,
credentials, tokens, passwords, API keys, or private evidence in this public Pal
Pack directory.

## External project boundary

Nova memory assets stay in the AgentPal central workspace or approved central
project records by default. External projects remain thin-bound through
`.agentpal/project.json` and must not receive copied `.agentpal/memory/` assets
by default.

