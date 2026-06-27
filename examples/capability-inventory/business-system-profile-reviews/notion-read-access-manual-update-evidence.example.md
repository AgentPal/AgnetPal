# Notion Read Access Manual Update Evidence Example

## Example Scope

- evidence_pack_id: `evidence-content-ops-notion-read-access-example`
- source_review: `notion-read-access-review.example.md`
- source_review_id: `review-content-ops-notion-read-access-example`
- review_decision: `approved_for_manual_update`
- organization_profile_ref: `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json`
- business_system_id: `notion-public-governance-example`
- example_only: true

## Approved Review Packet Premise

This example assumes a later review packet for Notion read access has been explicitly marked `approved_for_manual_update`.

That approval is only a premise for preparing this evidence pack. It is not an automatic organization profile update and it does not modify any Business System Profile.

## Proposed Manual Change

Mark `read_access` as `user_confirmed` only if both are present:

- explicit user confirmation that the relevant Notion read access exists
- current host Runtime evidence or other reviewable evidence that supports the claim

The proposed change must remain narrow. It must not infer page write access, database write access, API access, integration availability, export permission, admin permission, billing status, or workspace ownership.

## Current Example State

- user confirmation: example placeholder, not a real user confirmation
- host Runtime evidence: example placeholder, not a real Runtime result
- Notion token: none
- Notion connector: none
- real workspace id: none
- real page id: none
- real database id: none
- central roster update: none
- organization profile update performed by this example: no

## Evidence Summary

- project usage memory suggested possible Notion use for content planning
- approved review packet says this item may be prepared for manual writeback
- user confirmation must identify the access scope without exposing private workspace values
- host Runtime evidence must be current, scoped, and public-safe
- missing or not-run checks remain visible until performed

## Manual Writeback Target

```text
workspace/organization/capability-inventory/business-systems/
```

This example does not write to that target. It only shows the evidence pack shape that would be prepared before a user-approved manual writeback.

## Manual Writeback Steps

1. Re-read the approved review packet.
2. Re-read the current organization Business System Profile snapshot.
3. Confirm user approval for the exact organization-level change.
4. Confirm host Runtime evidence is present and public-safe.
5. Apply only the narrow read access field change to the organization profile.
6. Do not change central Pal contacts.
7. Do not create Notion connector files, API client files, tokens, or external project `.agentpal/evidence/`.
8. Run second verification and record the result.

## Rollback Note

Restore the previous profile snapshot summary if the manual update is rejected, over-scoped, or fails second verification.

For this example, rollback means returning the profile read access state to the prior `unknown`, `not-run`, or example-only state captured before writeback.

## Second Verification Checklist

- confirm the intended organization profile field changed only after manual writeback
- confirm `workspace/organization/contacts/pals.json` did not change
- confirm `workspace/organization/contacts/PAL_CONTACTS.md` did not change
- confirm no external project `.agentpal/evidence/` was created
- confirm no `.agentpal/reviews/`, `.agentpal/business-systems/`, or `.agentpal/capability-inventory/` was created in an external project
- confirm no Notion connector or API client was created
- confirm no token, password, API key, cookie, integration secret, private workspace id, page id, or database id was stored
- confirm no `keyword_map`, `domain_map`, or `role_map` was introduced
- confirm `not-run` checks were not converted to pass
- confirm missing evidence was not hidden

## Second Verification Status

```text
second_verification_status: second_verification_not_run
```

Second verification must be run after manual writeback. If it is not run, status remains `second_verification_not_run`.

## Decision

```text
decision: ready_for_manual_writeback
decision_by: example
decision_date: unknown
```

This decision means the evidence pack example is ready as a manual-writeback preparation artifact. It does not mean the organization profile has already been updated.

## Forbidden

- no automatic organization profile update
- no central roster update
- no external project `.agentpal/evidence/`
- no external project `.agentpal/reviews/`
- no external project `.agentpal/business-systems/`
- no external project `.agentpal/capability-inventory/`
- no Notion connector
- no Notion API client
- no credentials
- no token
- no password
- no API key
- no cookie
- no integration secret
- no private workspace id, page id, or database id
- no keyword routing
