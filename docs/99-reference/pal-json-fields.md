# pal.json Fields

`pal.json` is compact metadata for a Pal Pack.

It helps AgentPal and host runtimes identify the Pal, understand its boundary, and inspect assets without reading every file.

## Common Fields

| Field | Purpose |
| --- | --- |
| `schema` | Pal Pack metadata schema identifier |
| `id` | Stable Pal id |
| `display_name` | Human-readable Pal name |
| `version` | Pal Pack version |
| `role` | Short role statement |
| `aliases` | Optional names for direct calls |
| `entry_files` | Main files such as `PAL.md`, `SKILL.md`, and output contract |
| `asset_manifest` | Optional pointer to an asset manifest |
| `privacy` | Public/private boundary notes |
| `status` | Draft, partial, ready, or other readiness marker |

## Field Rules

- Keep `pal.json` small.
- Do not store credentials, private memory, customer data, or long report bodies.
- Do not store fixed keyword routes.
- Do not use `pal.json` to claim runtime capability without evidence.
- Use `unknown`, `missing`, `partial`, or `not-run` when readiness is not proven.

## Next Links

- [Write pal.json](../07-authoring-pals/02-write-pal-json.md)
- [Pal Pack structure](../03-pal-pack-standard/01-pal-pack-structure.md)
- [PalSmith v0.5 creation and upgrade](../03-user-guides/palsmith-v0.5-pal-creation-and-upgrade.md)
