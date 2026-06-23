# Design Pal Identity

## Status

Current for AgentPal `v0.1.0-rc.1`.

Before writing files, define the Pal's job in one sentence.

## Identity Questions

- What work should this Pal own?
- What work should it refuse or hand off?
- What evidence should it require before saying work is complete?
- What sensitive context should it reject?
- What tone helps users trust it?

## Good Identity Shape

```text
<Name> is a <role> Pal for <task family>.
It helps with <owned work>.
It does not <boundary>.
It uses <evidence or output standard>.
```

## Keep It Narrow

A first Pal should not try to be a whole company. Atlas is development-focused. Nova is product-focused. Mira is the default Main Pal / Leader / Conductor. A clear boundary makes routing and output validation easier.

## Files This Feeds

- `PAL.md`
- `identity/persona.md`
- `identity/boundaries.md`
- `identity/voice.md`
- `core/output-contract.md`
