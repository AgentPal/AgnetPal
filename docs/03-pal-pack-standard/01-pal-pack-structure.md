# Pal Pack Structure

A Pal Pack is one directory that represents one Pal.

In the AgentPal Workspace, official and user-added Pal Packs live under:

```text
pals/<Pal-Directory>/
```

The AgentPal root is not one Pal Pack. It is the workspace that contains multiple Pal Packs and shared workspace assets.

## Recommended Structure

```text
pals/<Pal-Directory>/
├─ AGENTS.md
├─ PAL.md
├─ README.md
├─ SKILL.md
├─ pal.json
├─ core/
│  └─ output-contract.md
├─ identity/
├─ knowledge/
├─ skills/
├─ runbooks/
├─ workflows/
├─ learning/
├─ memory/
├─ state/
├─ reports/
├─ examples/
└─ evals/
```

## Minimum Required Files

A contributed Pal Pack should include:

- `PAL.md`
- `pal.json`
- `SKILL.md`
- `README.md`
- `AGENTS.md`
- `core/output-contract.md`

## Directory Purposes

| Path | Purpose |
| --- | --- |
| `PAL.md` | Human-readable Pal identity, role, boundaries, and collaboration rules. |
| `pal.json` | Machine-readable Pal metadata, aliases, capabilities, and compatibility. |
| `SKILL.md` | Runtime entry for Skill-aware systems; must say this is a Pal Pack, not one ordinary Skill. |
| `AGENTS.md` | Runtime instructions local to this Pal Pack. |
| `README.md` | Human entry point for maintainers and users. |
| `core/output-contract.md` | What a valid answer from this Pal must include. |
| `identity/` | Additional identity and voice material. |
| `knowledge/` | Short knowledge cards and indexes. |
| `skills/` | Formal Pal-owned Skills. |
| `runbooks/` | Repeatable operational procedures. |
| `workflows/` | Higher-level lifecycle flows. |
| `learning/` | Public-safe learning candidates and reusable improvements. |
| `memory/` | Public-safe placeholders; private user memory should not be committed. |
| `state/` | Public-safe placeholders; runtime state should remain private or ignored. |
| `reports/` | Public-safe placeholders; real task reports should not be published. |
| `examples/` | Synthetic examples and failure examples. |
| `evals/` | Tests and self-checks for Pal behavior. |

## Contacts Boundary

Only valid Pal Packs should enter `contacts/` and `registry/`.

Skills, tools, plugins, models, MCP servers, raw repositories, runtime adapters, knowledge packs, and persona packs do not become Pals because they are useful or indexed.

## Related

- [What is a Pal Pack?](../01-concepts/02-what-is-a-pal-pack.md)
- [Root files](02-root-files.md)
- [Contacts and registry](10-contacts-and-registry.md)
- [Public/private boundary](11-public-private-boundary.md)
