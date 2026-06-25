# Pal Asset Governance Protocol

PalSmith governs Pal assets with a public-safe, permissioned workflow.

## Asset Types

- Root identity files: `PAL.md`, `SKILL.md`, `AGENTS.md`, `README.md`, `pal.json`
- Identity assets: `identity/`
- Core protocols: `core/`
- Capability assets: `knowledge/`, `skills/`, `runbooks/`, `workflows/`
- Validation assets: `evals/`, `examples/`
- Runtime/private placeholders: `memory/`, `state/`, `reports/`
- Governance assets: `templates/`, `scanners/`, `audit/`

## Static vs Runtime Content

Public Pal Pack files may contain release-safe templates, public-safe examples, synthetic evals, and protocol text.

Do not commit:

- user private memory
- private project state
- real task reports
- private logs
- credentials, tokens, keys, passwords
- local absolute paths
- unlicensed third-party full text

## Governance Flow

```text
Inspect
  -> classify asset and permission level
  -> generate plan or report
  -> identify privacy and overwrite risks
  -> ask confirmation when needed
  -> Runtime executes
  -> Runtime returns evidence
  -> PalSmith reviews evidence and writes report/audit template
```

## Contacts Rule

Only valid Pal Pack directories can enter contacts and registry. Ordinary Skills, tools, models, plugins, MCP servers, non-Pal runtimes, raw repositories, knowledge packs, and persona packs stay in imports or registry candidate areas.
