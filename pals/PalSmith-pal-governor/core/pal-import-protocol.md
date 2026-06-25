# Pal Import Protocol

All imports must go through staging before installation.

## Supported Sources

- GitHub repository URL
- GitHub repository subdirectory
- GitHub Release archive
- GitHub branch / tag / commit
- local directory
- local archive (`.zip`, `.tar`, `.tar.gz`, `.7z`)
- AgentPal internal Pal copy
- project `.agentpal/pals`

## Standard Flow

1. Identify the source type.
2. Download or copy to staging.
3. Scan directory structure.
4. Classify resource type.
5. Determine whether it is a standard Pal Pack.
6. Check `PAL.md`, `pal.json`, `SKILL.md`, `AGENTS.md`.
7. Check schema and version.
8. Check memory / state / reports.
9. Check sensitive files.
10. Check existing Pal ID conflicts.
11. Generate an import report.
12. Ask installation and enablement questions.
13. After confirmation, install.
14. Update registry if appropriate.
15. Optionally add to contacts only if it is a valid Pal Pack and the user confirms.
16. Generate completion report.
17. Prepare `audit/import-history.jsonl` entry.

## Resource Classification

| Type | Default Handling |
| --- | --- |
| Standard Pal Pack | can install to `pals/imported/` or `pals/user/` |
| Pal Team Pack | can install as a team after confirmation |
| Ordinary Skill | `imports/skills`, not contacts |
| Knowledge Pack | `imports/knowledge` |
| Persona Pack | `imports/personas` |
| Tool Pack | `imports/tools` |
| Mixed Resource Pack | generate `RESOURCE_INDEX`, wait for user choice |
| Unknown Resource | `imports/raw`, generate analysis report |

## Risk Checks

Check executable scripts, install scripts, binaries, hidden directories, external links, `.env`, token/key/password words, private memory, state, reports, logs, incompatible schema, overwrite attempts, Pal ID conflicts, unknown license, large files, submodules, and external dependencies.

## Default Recommendation

- install to `pals/imported/`
- do not import `memory / state / reports`
- do not automatically add to contacts
- isolate risk files
