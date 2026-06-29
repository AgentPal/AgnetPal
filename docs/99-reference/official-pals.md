# Official Bundled Pals

AgentPal v0.5 includes 10 official bundled Pals.

The table below is a central roster display, not a hard-coded route map. The source of truth is `workspace/organization/contacts/`. Owner selection remains case-specific AI judgement.

| Pal | ID | Directory | Role | Direct call |
| --- | --- | --- | --- | --- |
| Mira | `mira-main` | `official/pals/Mira-main` | Default entry Pal, Main Pal, Leader, and Conductor | `/pal Mira` |
| Atlas | `atlas-developer` | `official/pals/Atlas-developer` | Development, implementation structure, and code-facing risk | `/pal Atlas` |
| Vega | `vega-research` | `official/pals/Vega-research` | Research, source quality, and evidence framing | `/pal Vega` |
| Rhea | `rhea-system` | `official/pals/Rhea-system` | Local system, command, path, and environment safety | `/pal Rhea` |
| PalSmith | `palsmith-pal-governor` | `official/pals/PalSmith-pal-governor` | Pal asset governance, Pal creation, Pal team design, import/export, versioning, and privacy review | `/pal PalSmith` |
| Quinn | `quinn-quality` | `official/pals/Quinn-quality` | Quality, verification, release gates, acceptance, and risk | `/pal Quinn` |
| Morgan | `morgan-document` | `official/pals/Morgan-document` | Document and file workflow | `/pal Morgan` |
| Harper | `harper-writing` | `official/pals/Harper-writing` | Writing, communication, public docs, and editorial consistency | `/pal Harper` |
| Nova | `nova-product` | `official/pals/Nova-product` | Product scope, decision framing, and user value | `/pal Nova` |
| Faye | `faye-delivery` | `official/pals/Faye-delivery` | Business delivery packaging, workflow shaping, data/interface/risk lists, and Task Package readiness | `/pal Faye` |

## Default Behavior

Ordinary messages go to Mira. Specialist Pals do not listen by default.

Direct calls use display names or aliases, not directory names.

## Context Loading

Mira does not load every bundled Pal before routing. Mira reads central contacts summaries, then hands off to the selected owner Pal when needed.

The selected Pal reads its own minimum files and a small number of relevant assets. Index files are navigation aids, not permission to load every skill, knowledge card, runbook, workflow, example, or eval.

## Boundaries

- Pals are not Agent processes.
- Skills, tools, models, plugins, MCP servers, knowledge packs, and raw repositories are not Pal contacts by themselves.
- Adding a new official Pal is a governance change and must not be inferred from a draft.
- Customer-private data must not enter public Pal Packs or examples.

## Next Links

- [Call your first Pal](../02-getting-started/05-call-your-first-pal.md)
- [Simple Pal Mode](../01-concepts/05-simple-pal-mode.md)
- [Contacts and registry](../03-pal-pack-standard/10-contacts-and-registry.md)
