# R71 No Active Keyword Router

## Case ID

R71-NO-ACTIVE-KEYWORD-ROUTER

## Goal

Verify that R71 release-readiness changes did not introduce an active deterministic keyword, domain, or role router.

## Setup

- Use the current AgentPal workspace after R68/R69/R70 migrations and R71 checks.
- Search root entries, docs, standards, templates, evals, workspace records, and release checks.

## Evidence Paths

- `workspace/organization/contacts/pals.json`
- `standards/routing-and-judgement/no-keyword-routing-standard.md`
- `standards/boundaries/no-keyword-routing-boundary.md`
- `docs/02-concepts/why-no-keyword-routing.md`
- `templates/project-binding/`
- `evals/palbench/no-keyword-routing/`

## Expected Result

- `keyword_map`, `domain_map`, and `role_map` only appear in forbidden, boundary, template-check, or regression-test contexts.
- `/pal Atlas`, `/pal Quinn`, and similar calls are treated as explicit user direct calls.
- Natural language such as code, test, writing, development, or review does not create a fixed owner route by itself.
- `workspace/organization/contacts/pals.json` keeps `routing_policy: ai_judgement_only` and `keyword_routing_allowed: false`.

## Forbidden Result

- `开发 -> Atlas`, `测试 -> Quinn`, `写作 -> Harper`, or equivalent rules appear as current behavior.
- A template includes `keyword_map`, `domain_map`, or `role_map` as active routing data.
- A release check treats deterministic semantic routing as acceptable.

## R71 Verification Notes

Use `rg "keyword_map|domain_map|role_map" -n` plus targeted searches for Pal names and task-domain words. Classify hits before deciding.

