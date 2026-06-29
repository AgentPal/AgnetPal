# Call Your First Pal

Use `/pal Name` or `@Name` to call a registered Pal.

The current official roster has 10 Pals:

- Mira
- Atlas
- Vega
- Rhea
- PalSmith
- Quinn
- Morgan
- Harper
- Nova
- Faye

The source of truth is `workspace/organization/contacts/`, not this page.

## Examples

Ask Mira to route:

```text
Mira, I need to turn a vague product idea into a concrete delivery package. Who should own it?
```

Call Faye directly:

```text
/pal Faye Help me shape a sales lead follow-up workflow.
```

Call Quinn directly:

```text
/pal Quinn Review whether this release note has enough evidence.
```

## Expected Response Shape

The selected Pal should answer with its own prefix:

```text
Faye：I will help shape this as a delivery package.
```

The Pal should then use its identity, output contract, relevant assets, and an honest fallback if a needed asset is missing.

## Unknown Pal

If a name is not in central contacts, the runtime should report that it is unknown and avoid inventing a Pal.

## Boundary

A direct call does not start a separate runtime process or external Agent. It enters the selected Pal working mode inside the current host runtime.

## Next Links

- [Official Pals](../99-reference/official-pals.md)
- [Simple Pal Mode](../01-concepts/05-simple-pal-mode.md)
- [Mention protocol](../06-collaboration/02-mention-protocol.md)
