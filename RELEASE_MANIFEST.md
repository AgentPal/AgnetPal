# AgentPal v0.5.0-rc.1 Release Manifest

## Release Identity

| Field | Value |
| --- | --- |
| Release name | AgentPal v0.5.0-rc.1 |
| Workspace version line | `v0.5` |
| Package type | local release-candidate package |
| Runtime policy | Codex-first no-code Pal collaboration |
| Publication status | local package prepared; no tag, push, or GitHub Release performed by this manifest |
| License | MIT |

## Included Public Package Scope

- `README.md`
- `README.zh-CN.md`
- `START_HERE.md`
- `LICENSE`
- `THIRD_PARTY_NOTICES.md`
- `CHANGELOG.md`
- `RELEASE_NOTES.md`
- `RELEASE_CHECKLIST.md`
- `GITHUB_RELEASE_DRAFT.md`
- `CONTRIBUTING.md`
- `AGENTS.md`
- `PAL.md`
- `SKILL.md`
- `agentpal.json`
- `RESOURCE_INDEX.md`
- `docs/`
- `prompts/`
- `official/`
- `workspace/organization/contacts/`
- `standards/`
- `templates/`
- `examples/`
- root release files: `RELEASE_NOTES.md`, `RELEASE_CHECKLIST.md`, `RELEASE_MANIFEST.md`, and `GITHUB_RELEASE_DRAFT.md`

The source repository may retain `evals/` and `release/` evidence records for maintainers. The curated public zip artifact can exclude those evidence archives when they contain local validation paths or maintainer-only records.

## Official Pal Set

| Pal | Directory | Role |
| --- | --- | --- |
| Mira | `official/pals/Mira-main` | Main Pal, Leader, and Conductor |
| Atlas | `official/pals/Atlas-developer` | Developer / Implementation Lead |
| Nova | `official/pals/Nova-product` | Product / Strategy Lead |
| Faye | `official/pals/Faye-delivery` | AI Delivery Pal |
| Vega | `official/pals/Vega-research` | Research / Intelligence Lead |
| Quinn | `official/pals/Quinn-quality` | Quality / Verification Lead |
| Morgan | `official/pals/Morgan-document` | Document / File Workflow Lead |
| Harper | `official/pals/Harper-writing` | Writing / Content Craft Lead |
| Rhea | `official/pals/Rhea-system` | System / Runtime Safety Lead |
| PalSmith | `official/pals/PalSmith-pal-governor` | Pal Asset Governor |

Contacts source of truth:

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`

## Not Included

- `.git/`
- internal development directories and local reports outside the repository
- local clean-copy directories
- temporary files, caches, and system artifacts
- private memory, private project facts, real customer data, credentials, secrets, tokens, or API keys
- generated external-project `.agentpal/` test folders
- runtime code, CLI installers, app runtimes, daemons, scanners, connector layers, marketplace programs, or hosted services

## Validation Summary

R166 release-candidate preflight:

- core JSON parse: pass
- all visible JSON parse: pass
- official Pal dirs: 10
- official Pal `pal.json`: 10
- central active contacts: 10
- Faye included: yes
- README Pal rows: 10
- README.zh-CN Pal rows: 10
- Markdown links: 158 files, 0 missing
- stale entry / forbidden full support wording scan: pass
- claim boundary scan: pass with expected negative boundary hits
- internal/local path leak scan: pass
- credential assignment scan: pass
- added executable artifacts: 0
- clean-copy validation: pass

R167 package preparation must re-check the final zip before any remote publication.

## Publication Boundary

This manifest does not authorize or record remote publication.

The following remain not performed unless a later authorized release operation does them:

- `git push`
- `git pull`
- `git fetch`
- tag creation
- GitHub Release creation
