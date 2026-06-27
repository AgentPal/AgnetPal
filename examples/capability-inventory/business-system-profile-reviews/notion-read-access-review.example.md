# Notion Read Access Review Example

## Example Scope

- review_id: `review-content-ops-notion-read-access-example`
- source_project_id: `content-ops-demo`
- source_project_record_path: `examples/project-records/business-system-profile-references/content-ops-demo/`
- organization_profile_ref: `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json`
- business_system_id: `notion-public-governance-example`
- example_only: true

## Review Reason

Project usage memory says the user mentioned Notion may be used for content planning. That project memory can suggest an organization profile review, but it cannot update organization truth by itself.

## Proposed Change

Review whether Notion read access can be marked `user-confirmed` in an organization-level Business System profile.

## Evidence Summary

- project usage memory: user mentioned possible Notion use for content planning
- user confirmation: missing
- host Runtime evidence: not-run
- Notion workspace permission check: not-run
- Notion page read check: not-run
- Notion database visibility check: not-run

## Unknown Fields

- workspace access
- page read access
- database access
- API access
- integration status
- user role

## Missing Evidence

- explicit user confirmation
- current host Runtime evidence
- screenshot or UI confirmation
- exported report or documented admin setting

## Decision

- decision: `blocked_missing_evidence`
- recommended_status: `blocked_missing_evidence`
- decision_by: `example`
- decision_date: `unknown`

## Writeback Plan

No organization profile update yet.

If the user later confirms access and provides reviewable evidence, create a new review packet or update this packet with evidence. Only then propose a manual organization profile update.

## Forbidden

- no Notion connector
- no token, password, API key, cookie, integration secret, or private workspace value
- no central roster update
- no `.agentpal/reviews/` in an external project
- no `.agentpal/business-systems/` in an external project
- no keyword route
- no automatic organization profile update

