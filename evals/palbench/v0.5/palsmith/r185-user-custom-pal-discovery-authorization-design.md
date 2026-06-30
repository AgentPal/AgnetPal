# R185 User Custom Pal Discovery Authorization Design

date: 2026-06-30
workspace: `J:\开发\AgentPal`
owner: PalSmith
result: `pass`

## Goal

Design a no-code authorization flow for user custom Pal discovery after R181-R184 proved the default refusal boundary.

Core rule:

```text
user custom Pal default = private
authorization must be explicit, scoped, auditable, and revocable
```

## Assets Added

- `official/pals/PalSmith-pal-governor/core/user-custom-pal-discovery-authorization-protocol.md`
- `docs/06-palsmith/user-custom-pal-discovery-authorization.md`
- `prompts/palsmith/authorize-user-custom-pal-discovery.md`
- `templates/palsmith/user-custom-pal-authorization-record.md`
- `templates/palsmith/user-custom-pal-discovery-policy.md`

## Authorization Fields

| Field | Meaning | Default |
| --- | --- | --- |
| `private` | explicit path or explicit name only | enabled |
| `workspace_discoverable` | workspace may list the Pal as available | disabled |
| `workspace_invocable` | local unified call entry may invoke it | disabled |
| `limited_delegation` | named caller may delegate limited tasks | disabled |
| `contacts_registered` | explicit contacts registry target may include it | disabled |
| `marketplace_draft` | draft metadata only | disabled |
| `marketplace_public_requested` | publication request and review only | disabled |

These fields are independent. Discovery does not grant delegation, contacts registration, or Marketplace publication.

## Required Record

The authorization record must include:

- Pal identity and path;
- requested scopes;
- requested by / approved by / approved at;
- expiry or review date;
- allowed callers;
- allowed and denied tasks;
- data and memory access boundaries;
- revocation method;
- audit notes.

## No-Code Boundary

This design does not create:

- runtime code;
- CLI;
- scanner;
- daemon;
- connector;
- backend service;
- Marketplace backend.

## Contacts And Official Boundary

This design does not modify:

- `workspace/organization/contacts/`
- `official/pals/` outside PalSmith no-code protocol assets
- central roster entries
- official Pal count

## Decision

R185 design satisfies the requested authorization layer while preserving the R183/R184 refusal boundary.
