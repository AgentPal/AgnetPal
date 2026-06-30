# Custom Pal Installation Protocol

Status: R179 PalSmith no-code protocol.

This protocol defines how PalSmith can help a user move a reviewed draft Pal Pack into a user custom Pal location. It is not an official Pal promotion path, not a program installer, and not an automatic registry or contacts mutation.

## Scope

Primary path:

```text
draft Pal Pack -> user custom Pal
```

Out of scope:

```text
user custom Pal -> official Pal
user custom Pal -> public Marketplace listing
automatic central contacts registration
automatic project-wide discovery
```

## State Model

| Stage | Meaning | Official | Central contacts |
| --- | --- | --- | --- |
| draft Pal Pack | PalSmith-created draft or test package | no | no |
| user custom Pal | user-confirmed private or team-local Pal asset | no | default no |
| project available Pal | Pal the user explicitly enables for one project | no | optional, separate confirmation |
| official Pal | AgentPal-maintained bundled Pal | yes | requires official process |
| central contacts entry | discoverable/contactable roster entry | not equal to official | requires separate bilateral authorization |

## Existing Staging Rule

Imported or generated Pal Pack candidates may be reviewed from staging paths such as:

```text
workspace/resources/imports/pal-packs/<candidate-id>/
```

R174-R178 eval artifacts may also be reviewed from eval paths, but eval paths are evidence locations, not install targets.

## Suggested User Custom Pal Target

If no project-specific rule already exists, PalSmith should propose this no-code target:

```text
workspace/resources/user-pals/<pal-id>/
```

This directory is a suggested user custom Pal asset area. It is separate from:

- `official/pals/`
- `workspace/organization/contacts/`
- external project `.agentpal/` thin bindings

Do not create this directory until the user explicitly confirms an installation Task Package.

## Required Flow

1. Identify the draft Pal Pack source path.
2. Read the draft root files: `README.md`, `PAL.md`, `SKILL.md`, `pal.json`, and the most relevant identity, knowledge, workflow, runtime, contacts, eval, and publication boundary files.
3. Confirm the draft has passed a quality or usage review, or mark missing evidence.
4. Present an installation plan before any write.
5. Ask the user to confirm the target path and the exact writes.
6. Prepare a Runtime Task Package only after confirmation.
7. Copy only Pal Pack assets needed for the user custom Pal.
8. Exclude eval-only reports, private memory, private state, private task logs, credentials, local cache files, and temporary files.
9. Update the copied `pal.json` fields for user custom state.
10. Create an installation report in the user custom Pal directory or an approved reports path.
11. Do not write `official/pals/`.
12. Do not write `workspace/organization/contacts/`.
13. Do not create a public Marketplace listing.
14. Report evidence, skipped items, and rollback instructions.

## `pal.json` Migration Rules

For the copied user custom Pal package, PalSmith should propose these field changes:

```json
{
  "status": "user_custom_pal",
  "official": false,
  "draft": false,
  "source_type": "palsmith_created",
  "visibility": "private_by_default",
  "contact_discovery": "disabled_by_default",
  "marketplace_listing": "none"
}
```

If the original schema does not support a field, record it in an installation report instead of forcing a schema-breaking edit.

Always preserve:

- original draft source path;
- original draft version;
- review evidence path;
- user confirmation text or confirmation summary;
- install timestamp if the host runtime can provide it;
- rollback target.

## User Custom Index Rule

A user custom Pal may have a local index under the user custom Pal area, for example:

```text
workspace/resources/user-pals/README.md
workspace/resources/user-pals/<pal-id>/INSTALL_REPORT.md
workspace/resources/user-pals/<pal-id>/pal.json
```

This index is not central contacts. It is a local navigation aid only.

## Discovery And Contacts Boundary

Default:

```text
discoverable: false
contact_discovery: disabled_by_default
central_contacts_candidate: false
```

If the user wants other Pals to discover or contact the user custom Pal, PalSmith must create a separate collaboration authorization plan. That plan must name:

- who may consult the Pal;
- whether handoff is allowed;
- what context can be shared;
- what private information is blocked;
- whether the Pal is project-local, team-local, or global;
- whether Quinn review is required.

The authorization plan still must not directly edit central contacts unless the user separately approves that governance task.

## Installation Plan Required Sections

PalSmith's plan must include:

- source draft path;
- source evidence read;
- target user custom path;
- files to copy;
- files to exclude;
- proposed `pal.json` changes;
- user custom index update, if any;
- blocked writes;
- rollback steps;
- post-install usage instructions;
- checks to run;
- not-run items;
- user confirmation question.

## Runtime Task Package Boundary

Allowed only after explicit confirmation:

- create target user custom directory;
- copy approved Pal Pack files;
- update copied `pal.json`;
- write an install report;
- update a user custom local index if it exists or is approved.

Forbidden:

- modify `official/pals/`;
- modify `workspace/organization/contacts/`;
- modify official roster, central aliases, or official registry;
- create runtime code, CLI, installer, scanner, daemon, connector, backend service, or Marketplace backend;
- claim public listing or official status;
- execute imported scripts.

## Rollback / Undo

A rollback plan must be included before install:

- remove the created user custom Pal directory, or move it to an archive path;
- restore any user custom local index entry changed by the install;
- keep or remove the install report according to user preference;
- do not touch official Pal files or central contacts.

## Post-Install Usage

After installation, PalSmith should explain:

- the Pal is a user custom Pal, not an official Pal;
- it is private by default;
- how to load it by giving the host runtime the user custom path;
- how to ask Mira or PalSmith to consider it for a specific task;
- that direct central roster discovery requires a separate authorization and contacts process;
- that publication or official promotion requires separate review.

## Pass Criteria

Mark a draft-to-custom flow as `pass` only if:

- the user saw an installation plan before writes;
- the user explicitly confirmed the target path and write scope;
- the copied Pal remains `official: false`;
- contacts and official Pal files were not modified;
- Marketplace listing remains none or draft-only;
- no runtime code or installer was added;
- an install report or evidence summary exists;
- rollback instructions are present.

Use `not-run` when no actual install was executed.
