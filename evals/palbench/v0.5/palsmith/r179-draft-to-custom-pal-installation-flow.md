# R179 Draft To User Custom Pal Installation Flow

date: 2026-06-30
workspace: `J:\开发\AgentPal`
owner: PalSmith

## Decision

decision: `draft_to_user_custom_pal_no_code_flow_designed_no_commit_yet`

R179 designs the no-code flow for turning a reviewed draft Pal Pack into a user custom Pal. It does not perform an actual install and does not create an official Pal.

## Flow Scope

flow_scope: `draft_pal_pack_to_user_custom_pal_only`

In scope:

- reviewed draft Pal Pack source;
- user confirmation;
- quality and boundary checks;
- proposed user custom target path;
- copied `pal.json` status migration rules;
- local user custom index rule;
- rollback guidance;
- post-install usage guidance.

Out of scope:

- official Pal promotion;
- central contacts registration;
- public Marketplace listing;
- automatic discovery;
- runtime code, CLI, scanner, daemon, connector, backend service, or Marketplace backend.

## Files Added Or Updated

files_added_or_updated:

- `official/pals/PalSmith-pal-governor/core/custom-pal-installation-protocol.md`
- `official/pals/PalSmith-pal-governor/SKILL.md`
- `official/pals/PalSmith-pal-governor/PAL.md`
- `official/pals/PalSmith-pal-governor/README.md`
- `docs/PalSmith.md`
- `docs/06-palsmith/README.md`
- `prompts/palsmith/install-draft-as-custom-pal.md`
- `examples/palsmith/draft-to-custom-pal-installation-example.md`
- `evals/palbench/v0.5/palsmith/r179-draft-to-custom-pal-installation-flow.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`

## Existing Directory Rule Check

existing_user_custom_pal_rule: `not_found`

The repository already has import staging under:

```text
workspace/resources/imports/pal-packs/
```

No existing user custom Pal directory rule was found. R179 therefore documents a no-code suggested target:

```text
workspace/resources/user-pals/<pal-id>/
```

This path is a proposed install target for future confirmed Runtime Task Packages. R179 does not create it.

## Official Boundary

official_boundary: `pass`

- User custom Pals remain `official: false`.
- Draft-to-custom install does not write `official/pals/`.
- Official promotion remains a separate governance task.

## Contacts Boundary

contacts_boundary: `pass`

- User custom Pal install does not write `workspace/organization/contacts/`.
- Discovery is disabled by default.
- Contacts or collaboration authorization require a separate plan and explicit confirmation.

## Marketplace Boundary

marketplace_boundary: `pass`

- Marketplace metadata can remain draft-only.
- Public listing is not created.
- No Marketplace backend is introduced.

## Runtime Boundary

runtime_boundary: `pass`

- PalSmith designs plans and Runtime Task Packages only.
- No runtime code, CLI, installer, scanner, daemon, connector, backend service, or Marketplace backend was added.
- No actual install was executed in R179.

## Expected User Path

expected_user_path:

1. User points PalSmith to a draft Pal Pack path.
2. PalSmith reads the draft and available review evidence.
3. PalSmith outputs an installation plan.
4. User explicitly confirms target path and write scope.
5. Runtime copies approved Pal Pack assets to a user custom path.
6. Runtime updates copied `pal.json` to user custom state if schema-safe.
7. Runtime writes an install report and optional user custom local index.
8. PalSmith reports evidence, rollback steps, and post-install usage.

## Not Run Items

not_run_items:

- no actual user custom Pal directory created;
- no FirstPrinciplesProductReviewer install executed;
- no official Pal registration;
- no central contacts update;
- no Marketplace publication;
- no remote Git operation;
- no local commit.

## Next Test Needed

next_test_needed: `real_host_draft_to_custom_install_plan_rehearsal`

Recommended next test: run a real host rehearsal where PalSmith reads the FirstPrinciplesProductReviewer draft and outputs an install plan only, then Quinn reviews the plan before any write.

## Pass / Partial / Fail

pass_partial_fail: `pass`

R179 satisfies the design requirement for a no-code draft Pal Pack to user custom Pal installation flow.
