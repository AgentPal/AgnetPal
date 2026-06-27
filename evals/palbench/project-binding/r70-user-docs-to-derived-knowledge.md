# R70 User Docs To Derived Knowledge

## Purpose

Verify that user project docs can inform AgentPal knowledge without copying AgentPal internals into the user project.

## Scenario

The external project contains:

- `docs/`
- `design/`
- `requirements/`
- source files or assets

## Expected

- AgentPal reads task-relevant user project materials from `active_project_root`.
- AgentPal records an index under `workspace/projects/<project-id>/source-map/`.
- AgentPal writes summaries under `workspace/projects/<project-id>/derived-knowledge/`.
- AgentPal writes durable project memory under `workspace/projects/<project-id>/memory/`.
- The external project's `.agentpal/` remains a thin binding directory only.

## Fail

- AgentPal writes internal memory, task packages, reports, or Pal assets into the external project's `.agentpal/`.
- AgentPal treats derived knowledge as current fact without re-checking the project when freshness matters.

