# Context Packet Example

## Purpose

This public-safe context packet shows the minimum information a Runtime or
Brain could use when applying the combined pack to a no-code workflow task.

It is an example shape only. It is not a live project packet and does not
contain customer-private data.

## Context Packet

```yaml
packet_id: org-fde-content-ops-accounting-advisor-example
status: public-safe-example
user_goal: >
  Design a monthly workflow that combines content planning, revenue-record
  handoff notes, and a monthly review for a content team.
selected_combined_pack:
  path: examples/combined-packs/content-ops-with-accounting-advisor/
  metadata: examples/combined-packs/content-ops-with-accounting-advisor/combined-pack.json
org_pack_refs:
  - examples/org-packs/content-ops-org-pack/
fde_pack_refs:
  - examples/fde-packs/accounting-advisor-fde-pack/
recommended_pals_as_ai_judgement_input_only:
  - Mira
  - PalSmith
  - Morgan
  - Quinn
  - Vega
  - Harper
project_binding_refs:
  thin_binding_templates:
    - templates/project-binding/project-json-template.md
    - templates/project-binding/generic-codex/.agentpal/project.json
  external_project_agentpal_policy: thin-binding-only
central_project_record_placeholder:
  path: workspace/projects/<project-id>/
  create_real_record_in_public_example: false
reusable_assets:
  - examples/combined-packs/content-ops-with-accounting-advisor/reusable-assets-map.md
  - examples/combined-packs/content-ops-with-accounting-advisor/verification-checklist.md
  - standards/org-pack/org-pack-practical-structure.md
  - standards/fde-pack/fde-pack-standard.md
customer_private_placeholders:
  - workspace/projects/<project-id>/source-map/
  - workspace/projects/<project-id>/derived-knowledge/
  - workspace/projects/<project-id>/memory/
  - workspace/projects/<project-id>/tasks/
  - workspace/projects/<project-id>/reports/
  - workspace/projects/<project-id>/governance/
forbidden_context:
  - real customer names
  - real invoices
  - real contracts
  - real ledgers
  - real revenue reports
  - tax materials
  - payroll records
  - bank statements
  - account identifiers
  - private screenshots
  - credentials
  - tokens
  - cookies
  - passwords
  - API keys
  - connection strings
  - external project .agentpal/org-pack/
  - external project .agentpal/fde-pack/
  - keyword_map
  - domain_map
  - role_map
approval_and_verification_needs:
  human_review_required: true
  professional_decision_auto_approved: false
  not_run_is_pass: false
  missing_evidence_is_pass: false
runtime_execution:
  connector_included: false
  scanner_included: false
  validator_included: false
  marketplace_program_included: false
  external_api_client_included: false
  auto_execution: false
```

## Notes

- The recommended Pal list is not a deterministic route map.
- The current AI must judge ownership from the user goal, central roster,
  project context, risk, evidence needs, and expected deliverable.
- Private evidence belongs in a real approved project record only after user
  approval.
- This packet does not create that record.
