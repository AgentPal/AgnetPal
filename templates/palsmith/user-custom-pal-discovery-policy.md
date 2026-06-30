# User Custom Pal Discovery Policy

Use this template for a local workspace policy proposal. It is not central contacts, not official roster, and not a Marketplace listing.

```yaml
policy_id:
policy_status: proposed
workspace_scope:
created_by:
created_at:
review_after:
default_policy:
  user_custom_pals_private_by_default: true
  workspace_discovery_enabled_by_default: false
  workspace_invocation_enabled_by_default: false
  delegation_enabled_by_default: false
  contacts_registration_enabled_by_default: false
  marketplace_public_listing_enabled_by_default: false
entries:
  - pal_id:
    pal_name:
    pal_path:
    authorization_record:
    discovery:
      enabled: false
      allowed_callers: []
    invocation:
      enabled: false
      allowed_callers: []
    delegation:
      enabled: false
      allowed_callers: []
      allowed_tasks: []
      denied_tasks: []
      data_access:
        allowed: []
        denied: []
      memory_access:
        default: minimal
        allowed: []
        denied: []
        private_memory_allowed: false
    contacts_registration:
      enabled: false
      target_registry:
    marketplace:
      status: none
      draft_metadata_path:
revocation:
  policy_disable_method:
  entry_disable_method:
audit_notes:
```

## Policy Rules

- Do not add user custom Pals to `workspace/organization/contacts/` from this policy alone.
- Do not treat policy entries as official Pals.
- Do not allow delegation from discovery alone.
- Do not grant private memory access by default.
- Do not treat Marketplace draft metadata as public listing.
- Do not create runtime code, CLI, scanner, daemon, connector, backend service, or Marketplace backend.
