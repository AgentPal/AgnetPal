# Pal Index

This file is a legacy registry compatibility snapshot moved from the old root `registry/` path during R76 cleanup.

The current source of truth for Pal discovery is `workspace/organization/contacts/`. Individual Pal Packs must not maintain their own hard-coded list of other Pals or required collaborators.

## Registered

| Pal | id | Directory | Role | Direct call | Notes |
|---|---|---|---|---|---|
| Mira | `mira-main` | `official/pals/Mira-main` | main-leader-conductor | `/pal Mira` | Default Main Pal, Leader Pal, Conductor, team-leadership work owner, and ordinary-message receiver |
| Atlas | `atlas-developer` | `official/pals/Atlas-developer` | developer | `/pal Atlas` | Requirements, code tasks, repository handoff, review |
| Vega | `vega-research` | `official/pals/Vega-research` | research | `/pal Vega` | Research plans, source quality, evidence tables, comparisons |
| Rhea | `rhea-system` | `official/pals/Rhea-system` | system | `/pal Rhea` | System setup, app installation planning, permissions, recovery |
| Quinn | `quinn-quality` | `official/pals/Quinn-quality` | quality | `/pal Quinn` | Quality gates, acceptance, risk, evidence and release checks |
| Morgan | `morgan-document` | `official/pals/Morgan-document` | document | `/pal Morgan` | Files, documents, spreadsheets, PDFs, naming and archiving |
| Harper | `harper-writing` | `official/pals/Harper-writing` | writing | `/pal Harper` | Drafts, rewrites, communication and style alignment |
| Nova | `nova-product` | `official/pals/Nova-product` | product | `/pal Nova` | Idea intake, PRDs, scope, MVP slicing and developer handoffs |

## Scan Status

Mira and the official bundled specialist Pals are indexed. Directory naming follows `Name-role`.

The specialist Pals are slim embedded AgentPal modules, not standalone repositories. Workspace-level contacts, registry compatibility records, runtime compatibility notes, project binding, and current Pal-layer orchestration protocols are owned by AgentPal root.

## Routing Rule

Ordinary messages go to Mira. Specialist Pals do not listen by default. Mira may consult, delegate, hand off, or request review from a specialist Pal through a Context Packet. Users may also call a Pal directly with `/pal Name`.

When collaboration is needed, the current AI / Mira / Brain resolves collaborators from central contacts and decides case-by-case. The table above is a historical registration view, not a route map.

## Boundary

Only Pal Packs enter the Pal index and contacts. Tools, models, plugins, MCP servers, non-Pal runtimes, raw repositories, knowledge packs, and persona packs are not Pal contacts.


