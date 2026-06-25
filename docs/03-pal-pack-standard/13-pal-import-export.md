# Pal Import And Export

## Status

Current for AgentPal `v0.1.0-rc.1`.

Pal import and export are Pal asset governance tasks. The official owner Pal is PalSmith (`/pal PalSmith`), while the host Runtime performs actual file operations and must return evidence.

## Import Rule

All external imports are untrusted by default and must enter staging before installation.

Supported sources:

- GitHub repository URL
- GitHub repository subdirectory
- GitHub Release archive
- GitHub branch, tag, or commit
- local directory
- local archive
- AgentPal internal Pal copy
- project `.agentpal/pals`

PalSmith must classify imports as Standard Pal Pack, Pal Team Pack, ordinary Skill, Knowledge Pack, Persona Pack, Tool Pack, Mixed Resource Pack, or Unknown Resource.

Only valid Pal Packs can enter `pals/`, contacts, and registry. Ordinary Skills, tools, models, plugins, MCP servers, external Agents, raw repositories, knowledge packs, and persona packs do not become Pal contacts.

## Import Risk Checks

Before installation, check for executable scripts, install scripts, binaries, hidden directories, external links, `.env`, token/key/password strings, private memory, state, reports, logs, incompatible schema, overwrite attempts, Pal ID conflicts, unknown license, large files, submodules, and external dependencies.

Default recommendation:

- stage first
- install to `pals/imported/` only after confirmation
- do not import `memory / state / reports`
- do not automatically add to contacts
- isolate risk files

## Export Types

PalSmith supports five export modes:

1. Clean Pack Export
2. With Memory Export
3. Template Export
4. Team Export
5. Backup Export

Users must choose a mode before export. Clean Pack Export is the default recommendation for sharing or public release.

## Clean Pack Export

Clean Pack Export includes public-safe Pal files and excludes private runtime data.

Include `PAL.md`, `SKILL.md`, `AGENTS.md`, `pal.json`, `README.md`, `CHANGELOG.md`, `LICENSE`, `identity/`, `core/`, `knowledge/`, `skills/`, `runbooks/`, `workflows/`, `evals/`, `export-manifest.json`, and `export-report.md`.

Exclude `memory/user/`, `memory/project/`, `state/`, `reports/`, private reasoning logs, private contacts history, runtime private logs, user private files, `.env`, credentials, and tokens.

## With Memory Export

With Memory Export may include private memory, state, reports, and usage history. It requires strong confirmation and a follow-up question about which memory types to include.

Do not use With Memory Export for public sharing unless the user explicitly confirms and the privacy check passes.

## Export Manifest

Each export plan should include an `export-manifest.json` with schema, export type, timestamps, Pal identity, source path, included and excluded sections, memory/state/report flags, private data risk, license, compatible runtimes, and checksum.
