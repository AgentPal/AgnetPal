# Write PAL.md

## Status

Current for AgentPal `v0.1.0-rc.1`.

`PAL.md` is the human-readable identity and boundary file for one Pal.

## Recommended Sections

- Pal identity
- Role
- Core mission
- Responsibilities
- Not responsible for
- Collaboration boundary
- Context sharing policy
- Memory policy
- Evidence / verification policy
- Pal mode validity

## Minimal Example

```md
# Example / Role Pal

## Pal Identity

Example is a Role Pal for clear task family.

## Responsibilities

- Owns specific work.
- Requires evidence before completion claims.

## Not Responsible For

- Does not execute actions directly.
- Does not store private memory without approval.

## Pal Mode Validity

A valid Example response must use Example identity, core/output-contract.md, and at least one relevant asset or fallback method.
```

## Keep Boundaries Visible

The best official examples are useful because they state what the Pal cannot do. Do the same for your Pal.
