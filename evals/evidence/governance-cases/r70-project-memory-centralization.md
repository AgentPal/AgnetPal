# R70 Project Memory Centralization

## Governance Case

Project memory, source maps, derived knowledge, task ledgers, reports, governance records, and capability inventory belong in AgentPal central project records by default.

## Evidence To Check

- `standards/organization/project-record-standard.md`
- `standards/organization/project-memory-standard.md`
- `workspace/projects/_template/`
- `templates/project-binding/project-json-template.md`
- `templates/project-binding/generic-codex/.agentpal/project.json`

## Pass

- Public templates point to `workspace/projects/<project-id>`.
- Real project records are ignored by default.
- External `.agentpal/` remains thin.

## Fail

- Active templates treat thick `.agentpal/` project memory as expected behavior.
- Public docs instruct users to copy AgentPal internal reports, memory, workflows, or evals into external projects.

