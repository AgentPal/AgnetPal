# R181 PalSmith Draft To Custom Enablement Plan

date: 2026-06-30
workspace: `J:\开发\AgentPal`
host_mode: `current_codex_thread_agentpal_mode`
speaking_pal: PalSmith
result: `palsmith_host_plan_pass_current_thread`

## Request

Plan how to enable the reviewed draft Pal Pack:

```text
evals/palbench/v0.5/palsmith/draft-pal-packs/FirstPrinciplesProductReviewer/
```

as a user custom Pal only.

Constraints:

- do not make it an official Pal;
- do not add it to central contacts;
- do not enable discovery automatically;
- do not create a public Marketplace listing;
- do not add runtime code, CLI, scanner, daemon, connector, backend service, or Marketplace backend.

## Terminology

Here, installation is not a software installer.

Here, installation means a no-code Pal Pack enablement / placement / local-index flow:

```text
draft Pal Pack
  -> user confirmation
  -> user custom Pal test artifact
```

It is not:

```text
installer.exe / CLI / daemon / background service
```

## Source Evidence Read

Draft source:

```text
evals/palbench/v0.5/palsmith/draft-pal-packs/FirstPrinciplesProductReviewer/
```

Source files observed:

- `README.md`
- `PAL.md`
- `SKILL.md`
- `pal.json`
- `identity/role.md`
- `identity/source-boundary.md`
- `identity/tone.md`
- `knowledge/mental-models.md`
- `knowledge/product-review-knowledge.md`
- `workflows/product-review-workflow.md`
- `workflows/complexity-compression-workflow.md`
- `skills/skill-map.md`
- `runtime/agent-usage-policy.md`
- `memory/memory-template.md`
- `contacts/collaboration-boundary.md`
- `evals/draft-pal-quality-gate.md`
- `marketplace/metadata-draft.md`
- `marketplace/publication-boundary.md`

Review evidence available:

- `evals/palbench/v0.5/palsmith/r175-draft-pal-pack-quality-regression.md`
- `evals/palbench/v0.5/palsmith/r177-draft-pal-usage-regression-summary.md`
- R178 local commit report confirms R177 usage regression evidence was committed.

## Target Directory

Use the R179 protocol default target:

```text
workspace/resources/user-pals/FirstPrinciplesProductReviewer/
```

This target is non-official. It is separate from:

- `official/pals/`
- `workspace/organization/contacts/`
- official Pal registry / roster

## Files To Copy

Copy Pal Pack assets only:

- `README.md`
- `PAL.md`
- `SKILL.md`
- `pal.json`
- `identity/`
- `knowledge/`
- `workflows/`
- `skills/`
- `runtime/`
- `memory/`
- `contacts/`
- `evals/`
- `marketplace/`

Do not copy R174 / R175 / R177 reports as runtime assets. They remain evidence in `evals/palbench/v0.5/palsmith/`.

## `pal.json` Changes

For the copied user custom Pal, migrate the metadata to:

```json
{
  "status": "user_custom_pal",
  "official": false,
  "draft": false,
  "source_type": "palsmith_created_from_draft",
  "visibility": "private_by_default",
  "contact_discovery": "disabled_by_default",
  "marketplace_listing": "none"
}
```

Also preserve:

- `source_draft_path`
- `installed_by`
- `installed_date`
- `installation_scope`

Do not write:

- `official: true`
- `central_contacts: true`
- `marketplace_public: true`
- `discovery_enabled: true`

## Files Absolutely Not Modified

- `official/pals/`
- `workspace/organization/contacts/`
- official Pal registry / roster files
- Git remote state
- tag or release state

## User Confirmation Question

Confirmation required before writes:

```text
For R181 test only, do you confirm creating a user custom Pal test artifact under
workspace/resources/user-pals/FirstPrinciplesProductReviewer/
from the reviewed draft Pal Pack, without official registration, central contacts,
automatic discovery, public Marketplace listing, or runtime code?
```

## Simulated User Confirmation For This Test

user_confirmation_for_test: `true`

scope: `FirstPrinciplesProductReviewer draft -> user custom Pal test artifact only`

not_allowed:

- official Pal
- central contacts
- discovery
- Marketplace listing
- runtime code

confirmation_statement:

```text
For R181 test only, user confirmation is simulated by the main thread to create a user custom Pal test artifact under the approved non-official path.
```

## Runtime Task Package

Allowed writes after test confirmation:

1. Create `workspace/resources/user-pals/FirstPrinciplesProductReviewer/`.
2. Copy approved draft Pal Pack assets into the target.
3. Update copied `pal.json` to user custom state.
4. Write `INSTALL_REPORT.md` in the target.
5. Create or update a local user custom Pal index under `workspace/resources/user-pals/`.
6. Write R181 evidence reports under `evals/palbench/v0.5/palsmith/`.
7. Update `RESOURCE_INDEX.md` and `agentpal.json`.

Blocked writes:

- `official/pals/`
- `workspace/organization/contacts/`
- official registry / roster
- Marketplace backend or public listing
- runtime code / CLI / scanner / daemon / connector / backend service

## Verification Commands

Required checks:

```text
git status --short --branch
python -m json.tool agentpal.json
python -m json.tool workspace/resources/user-pals/FirstPrinciplesProductReviewer/pal.json
git diff --check
git diff --name-only -- workspace/organization/contacts
git diff --name-only -- official/pals
find official/pals -maxdepth 1 -mindepth 1 -type d | wc -l
find workspace/resources/user-pals/FirstPrinciplesProductReviewer -type f | sort
```

Windows execution may use PowerShell-equivalent commands for `find` / `wc`.

## Plan Decision

pass_partial_fail: `pass`

PalSmith judges the draft-to-custom enablement plan ready for the R181 test write scope because the target is non-official, the draft has existing quality and usage evidence, the user confirmation is explicitly test-scoped, and the plan blocks central contacts, official roster, discovery, public Marketplace listing, and runtime implementation changes.
