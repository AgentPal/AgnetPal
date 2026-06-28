# R93-D Path Fix Suggestions

## Summary

R93-D found no blocking central asset reachability failures. The only public tracked navigation debt found in this audit is stale release-support wording in `RELEASE_MANIFEST.md` and `RELEASE_CHECKLIST.md`.

This file is a suggestion record only. R93-D did not modify the shared/release entry files.

## Suggested Fixes

### `RELEASE_MANIFEST.md`

Replace stale root Pal/contact/registry references:

| Current stale reference | Suggested current reference |
| --- | --- |
| `pals/Mira-main` and other `pals/*` paths | `official/pals/Mira-main` and other `official/pals/*` paths |
| `contacts/pals.json` | `workspace/organization/contacts/pals.json` |
| `contacts/PAL_CONTACTS.md` | `workspace/organization/contacts/PAL_CONTACTS.md` |
| `registry/pal.index.json` | `workspace/resources/registry/pal.index.json` if the registry reference is still intended |
| `registry/pal.index.md` | `workspace/resources/registry/pal.index.md` if the registry reference is still intended |

Observed stale samples:

- official bundled Pal Packs under `pals/`
- contacts and registry files under `contacts/` and `registry/`
- all official Pal table rows use `pals/<Pal-Directory>`
- R10 JSON parse sentence references `contacts/pals.json`, `registry/pal.index.json`, and `pals/`

### `RELEASE_CHECKLIST.md`

Replace stale root Pal/contact/registry references:

| Current stale reference | Suggested current reference |
| --- | --- |
| `pals/Mira-main` and other `pals/*` paths | `official/pals/Mira-main` and other `official/pals/*` paths |
| `contacts/pals.json` | `workspace/organization/contacts/pals.json` |
| `registry/pal.index.json` | `workspace/resources/registry/pal.index.json` if the registry reference is still intended |

Observed stale samples:

- official bundled Pal directories checklist still uses `pals/*`.
- PalSmith registration checklist references `registry/pal.index.json` and `contacts/pals.json`.
- official count consistency checklist references `agentpal.json`, `registry/pal.index.json`, and `contacts/pals.json`.

## Local Suspicious Item Not Included As Public Fix

The AgentPal Workspace root contains an ignored local `.agentpal/` runtime/smoke area, including `.agentpal/reports`. `git ls-files -- '.agentpal/*'` returned no tracked files.

Classification: suspicious-local, not public tracked release content. Keep ignored and do not copy into external project bindings. Optional local cleanup should be handled separately, not as an R93-D public-path integration fix.
