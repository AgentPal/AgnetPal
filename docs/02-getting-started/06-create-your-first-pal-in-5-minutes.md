# Create Your First Pal In 5 Minutes

This guide shows the shortest safe path for designing a new Pal. It does not automatically add the Pal to the official roster.

For most users, start with PalSmith instead of hand-editing every file.

## 1. Describe The Pal

Use a public-safe idea. Do not paste private customer data.

```text
/pal PalSmith Help me design a Pal for customer onboarding QA.
Keep it as a draft and do not modify central contacts.
```

PalSmith should clarify:

- the Pal's job
- who it helps
- what decisions it should make
- what it must never claim
- what output shape it should produce
- what knowledge or examples it needs

## 2. Draft The Minimum Pal Pack

A draft Pal Pack normally needs:

- `PAL.md`
- `pal.json`
- `SKILL.md`
- `README.md`
- `AGENTS.md`
- `core/output-contract.md`

Put draft assets in an approved workspace area or a separate working branch. Do not write them into an external project's `.agentpal/` folder.

## 3. Review Before Registration

Before a Pal becomes registered, check:

- it is truly a Pal, not a Skill, tool, model, plugin, raw repo, or knowledge pack
- it has a clear owner role and output contract
- it does not contain private data, credentials, customer facts, or internal notes
- it does not claim connector, executor, app runtime, or automatic runtime behavior
- it has enough public-safe examples or an honest knowledge gap

## 4. Roster Changes Are Separate

Adding a Pal to `workspace/organization/contacts/` is a governance change. Do not treat draft creation as official registration.

For v0.5, the bundled official roster remains 10 Pals and includes Faye.

## Next Links

- [PalSmith guide](../06-palsmith/README.md)
- [Authoring overview](../07-authoring-pals/00-authoring-overview.md)
- [Pal Pack structure](../03-pal-pack-standard/01-pal-pack-structure.md)
- [Official Pals](../99-reference/official-pals.md)
