# R93-D Local Central Asset Integrity Validation

## Summary

Decision: pass with non-blocking path-fix suggestions.

Validation target: AgentPal Workspace central entry files, central Pal roster, official Pal Packs, Capability Inventory paths, Business System governance chain, thin binding templates, and forbidden active behavior surface.

Execution layer: current Codex local shell in `J:\开发\AgentPal`.

## Commands / Checks Run

- `git status --short --branch`
- PowerShell JSON parse for all visible `.json` files
- required root file existence checks
- central roster count, routing flags, and pack path checks
- official Pal count, entry files, `pal.json` parse, and copied `.agentpal/` directory checks
- Capability Inventory four-source path and README checks
- Business System governance-chain path checks
- project binding template and project JSON parse checks
- `rg` searches for thick binding paths, keyword route maps, auto scanner/connector language, and credential-like strings
- tracked runtime-code/dependency-manifest check through `git ls-files`

## Validation Results

| Check | Result |
| --- | --- |
| Git baseline before new R93-D files | `## master...origin/master [ahead 19]` |
| Root entries | 6 / 6 present |
| Visible `.json` files parsed | 82 |
| JSON parse failures | 0 |
| Central roster registered Pals | 9 |
| Central roster active Pals | 9 |
| `routing_policy` | `ai_judgement_only` |
| `keyword_routing_allowed` | `false` |
| exact JSON route keys `keyword_map`, `domain_map`, `role_map` | 0 |
| missing central roster `pack_path` targets | 0 |
| official Pal directories | 9 |
| official Pal required entry files | pass |
| official Pal `pal.json` parse | pass |
| copied `.agentpal/` dirs inside official Pals | 0 |
| Capability Inventory four-source paths | pass |
| Capability Inventory README checks | 5 / 5 present |
| Business System governance chain | 21 / 21 present |
| generic Codex thin binding templates | pass |
| Claude Code thin binding templates | pass |
| project JSON parse checks | pass |
| tracked runtime code / dependency manifests | 0 |

## Public-Safe Boundary

No tracked CLI, web app, desktop app, scanner, validator, daemon, installer, connector, background sync, database, dependency manifest, or runtime code entrypoint was found.

Search hits for forbidden terms are classified as boundary language, examples, evals, release checklists, archive notes, or ignored local runtime/smoke data. Exact JSON route keys are absent.

The only concrete secret-like value match is `ghp_DO_NOT_USE_EXAMPLE_TOKEN` in `examples/failures/business-system-profile-as-connector.md`, classified as an intentional negative example.

## Not-Run / Not Applicable

- No fresh clone was created in a separate directory. This is a local clean-path validation from the current workspace.
- No remote operations were run.
- No release, tag, or GitHub Release action was run.
- No external project `.agentpal/` directory was written.

## Findings

Blocking findings: none.

Non-blocking path navigation debt:

- `RELEASE_MANIFEST.md` still contains stale root references to `pals/`, `contacts/`, and `registry/`.
- `RELEASE_CHECKLIST.md` still contains stale root references to `pals/`, `contacts/`, and `registry/`.

Fix details are recorded in `release/integration-notes/r93d-path-fix-suggestions.md`.

## Decision

R93-D local validation passes for central asset integrity and path reachability, with non-blocking stale release-support references deferred to the integration thread.
