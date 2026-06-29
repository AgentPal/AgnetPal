# Project Memory

Project memory stores facts and records about a specific external project.

In a bound project, the external project remains `active_project_root`. AgentPal's central project record is the normal place for structured AgentPal records.

## Default Location

Approved project records belong under:

```text
workspace/projects/<project-id>/
```

Do not write project memory into the external project's `.agentpal/` directory by default.

## What Can Become Project Memory

- source maps
- derived knowledge
- task records
- bounded reports
- governance notes
- capability inventory profiles
- verified project facts
- privacy-approved business context

## What Must Stay Out

- credentials
- raw customer exports
- private data copied into public examples
- unverified assumptions
- hidden runtime logs
- AgentPal release evidence that belongs under `evals/` or `release/`

## Thin Binding Boundary

The external project `.agentpal/` folder should remain a small binding surface. It should not become a thick store for Pal Packs, memory, reports, docs, evals, or release files.

## Next Links

- [Bind an external project](../01-getting-started/bind-external-project.md)
- [Project-first connection](../04-runtime-guides/04-project-first-connection.md)
- [Memory overview](00-memory-overview.md)
