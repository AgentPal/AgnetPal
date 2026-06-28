# Memory

## Purpose

This directory stores public-safe durable memory summaries and memory policy
notes for Vega.

Memory stores extracted long-term lessons, research process preferences, source
quality decisions, routing lessons, and continuity references. It is not a place
for full task reports.

## What belongs here

- Reviewed long-term lessons from Vega research and intelligence work.
- Public-safe source-review, runtime, and tool-use memory summaries.
- Pointers to central project memory records.
- Research workflow lessons after they are extracted and reviewed.
- Notes that preserve `unknown`, `missing`, or `not-run` evidence.

## What does not belong here

- Full completion reports, research reports, source inventories, or validation
  records.
- Raw evidence, source dumps, customer data, or current runtime state.
- Credentials, tokens, secrets, cookies, passwords, API keys, or private project
  data.
- Unapproved private user or project memory.
- External project `.agentpal/memory/` as a default target.
- Keyword routing maps or deterministic dispatch rules.

## Current assets

| Asset | Memory purpose | Status | Notes |
| --- | --- | --- | --- |
| `skill-memory/` | Skill-related memory candidates or durable lessons | `present` | Keep Agent Skill references as references unless rewritten as Pal-owned methods. |
| `user/` | User-facing preference or continuity memory area | `present` | Use only for approved, public-safe summaries. |

## Candidate memories / needs review

| Candidate | Source report / evidence | Review status |
| --- | --- | --- |
| Source-quality review lessons | Future research reports | `needs-review` |
| Research uncertainty handling lessons | Future verified task evidence | `needs-review` |

## Relationship to reports

Reports belong in `reports/`. Research outputs and source inventories belong in
`research/` or `reports/` until stable lessons are extracted, reviewed, and
summarized as memory.

## Project-private memory boundary

Project-private memory belongs to AgentPal central project records, not external
project directories. Do not copy Vega memory into an external project's
`.agentpal/` tree by default.

## Related standards

- `standards/pal-asset/pal-asset-directory-standard.md`
- `templates/pal-asset/index-templates/memory-index-template.md`
- `templates/pal-asset/safe-index-backfill-guide.md`

## Public safety boundary

Do not store private user memory, private project memory, raw source dumps,
secrets, credentials, tokens, passwords, API keys, or private evidence in this
public Pal Pack directory.

## External project boundary

Vega memory assets stay in the AgentPal central workspace or approved central
project records by default. External projects remain thin-bound through
`.agentpal/project.json` and must not receive copied `.agentpal/memory/` assets
by default.

