# Generic CLI Agent Install AgentPal In Current Project

Use this with a Markdown/JSON-capable CLI Agent while your shell is inside an external user project.

This is a thin binding prompt. It does not copy AgentPal rules, Pals, protocols, docs, examples, evals, or release files into the project.

```text
Please connect AgentPal to the current project.

Inputs:
- current project root: the current working directory
- AgentPal workspace root: ask me for the local AgentPal Workspace path before changing files, unless I already provided a clear path in this conversation

Do not ask me to edit this prompt. If the AgentPal Workspace path is not already clear, ask one short question first:

`Please provide the local AgentPal Workspace path, for example <path-to-AgentPal>.`

After I provide the path, verify it by checking that it contains `agentpal.json`, `AGENTS.md`, `workspace/organization/contacts/pals.json`, and `workspace/organization/contacts/PAL_CONTACTS.md`. If the path is missing or invalid, stop and ask for the correct AgentPal Workspace path.

Post-install reminders:
- The current project stores a thin binding only.
- The current Pal list is read from the AgentPal workspace central contacts, not from copied project text.
- Project memory, source maps, derived knowledge, task records, reports, governance records, and capability inventory are stored in the AgentPal workspace under `workspace/projects/<project-id>/`.
- If the AgentPal framework updates later, this project should reread the core gates from the AgentPal workspace.
- Generic CLI agents must at least load the project `AGENTS.md` binding; if this runtime does not read it automatically, report that limitation honestly.
- Do not copy the full Pal list, full Pal Packs, full rule bodies, or AgentPal docs into this project.

Hard boundaries:
- Do not scan the whole disk.
- Do not create Claude-specific files.
- Do not copy AgentPal Pal Packs, docs, protocols, examples, evals, or release notes into this project.
- Do not create runtime code, scripts, services, daemons, installers, or UI.
- Treat Deep Conductor as AgentPal v0.5 no-code collaboration and mode-decision protocol, not as automatic runtime execution.
- Do not present Deep Conductor Master Loop or Project Conductor Workflow as an automatic background task system.
- Do not present Cross-Runtime Pal Memory as an automatic memory sync service, database, daemon, or background Runtime feature.
- Do not present Owner + Verifier as automatic background multi-agent execution.
- Do not present Parallel Independent Review as automatic background multi-agent or multi-runtime execution.
- Do not claim subagent execution, external Agent execution, MCP/plugin calls, Runtime Skill execution, or host capability availability without current runtime evidence or a user-provided manual capability profile.
- Do not run `git push`, `git pull`, `git fetch`, create tags, create GitHub Releases, or call GitHub publication APIs unless the user explicitly authorizes that remote action in the current session.

Create or update only the thin binding:
1. `.agentpal/project.json`
2. `.agentpal/AGENTPAL.md`
3. root `AGENTS.md` protected block

The binding must say that AgentPal rules are read from the AgentPal workspace root.
The binding must include `binding_mode: thin`, `central_pal_contacts`, and `agentpal_project_record`.

The root `AGENTS.md` protected block must explicitly tell a fresh session:
- enter AgentPal project-bound mode when this file is loaded
- ordinary messages start with Mira
- every AgentPal-mode natural-language reply starts with the current speaking Pal prefix, such as `Mira：`, `Rhea：`, or `Atlas：`
- do not start an AgentPal-mode answer with an unlabeled bullet, paragraph, table, or tool-result summary
- do not answer as the generic runtime unless the user explicitly asks for generic runtime / no AgentPal / no Pal mode
- apply the First Pal Gate before substantive work
- before any Runtime tool call, Bash / shell command, MCP call, file write, project inspection, or system inspection for a substantive task, output a user-visible Pal-prefixed owner judgement. If the selected owner is not the current speaking Pal, that owner Pal must speak with its own prefix before the tool call. Do not call tools first and explain ownership afterward
- for composite deliverable tasks, name selected or provisional stage owner Pals through AI judgement and current central contacts before broad clarification, handoff, or execution
- for implementation-shaped final deliverables, perform AI owner judgement before Runtime execution. Atlas is only a possible candidate from current central contacts, not an automatic route from words such as HTML, page, frontend, code, or repository
- for tasks the AI judges to involve local system/app state, permission or safety boundaries, runtime/environment readiness, command failure recovery, system-impact risk, or execution-layer diagnostic evidence, make a system-owner judgement before any command or inspection. Rhea is a case-specific candidate from the central contacts, not a keyword route or fixed task-domain map
- when user text contains `/pal Name`, resolve the named Pal from current AgentPal central contacts and treat it as direct owner-candidate mode after core gates
- when user text contains `@Pal`, treat it as consult / review by default; create or follow a bounded Context Packet instead of sending full chat history
- if the user explicitly asks for handoff, takeover, or owner transfer, use Context Packet mode `handoff` or `owner_transfer`
- `/pal` and `@Pal` are AgentPal Markdown protocols in this binding, not native CLI commands; do not require CLI support for them
- Owner + Verifier is a no-code staged workflow. Runtime may follow the task package sequentially, but verifier work needs independent evidence context and a `pass` / `fail` / `blocked` result record.
- Parallel Independent Review is a no-code staged workflow. Runtime may follow multiple reviewer packets sequentially, but reviewer final reports must stay independent and one reviewer draft must not be given to another reviewer.
- Deep Conductor Master Loop is a no-code protocol. Runtime may follow a Deep Conductor plan, Project Conductor task map, Runtime Skill-aware package, or next-round Runtime task package, but must not treat it as an automatic background workflow.
- Deep Conductor E2E Package is the complete no-code output shape for goal -> memory -> Capability Inventory -> Context Budget -> topology -> Context Packets -> Runtime Skill-aware packages -> verification -> synthesis -> Routing Memory -> next-round recommendation. The host runtime may follow approved stage packages and must return E2E synthesis fields; it must not treat E2E as an automatic background system.
- AgentPal v0.5 Deep Conductor may judge Fast Route, Owner + Verifier, Plan-Execute-Verify, Parallel Review, Sequential Chain, External Agent handoff, and Fallback shapes by AI judgement. These are candidate collaboration shapes, not deterministic keyword routes.
- Runtime Skill-aware packages are executed by the host Runtime only after current availability and permission evidence. AgentPal does not execute Runtime Skills.
- If a Runtime Skill-aware package names Skill/plugin/MCP candidates, the host Runtime must check only the named current-session candidates within the package scope, report available / unavailable / unknown / blocked, and follow `if_unavailable_fallback` when missing.
- Runtime-installed Skills belong to the host Runtime capability surface, not to AgentPal or any Pal Pack.
- If a task package includes a Context Budget Plan, the runtime must follow its read tier, allowed context, forbidden context, stop conditions, and escalation reasons. Do not read the whole AgentPal workspace because a Context Budget Plan exists.
- Final reports for Context Budget tasks must include a Context Usage Report when requested.
- Do not claim exact token or cost statistics unless the host system provides exact metering evidence.
- Verification must not be skipped to reduce token or context cost; report `not-run` or `blocked` when evidence is unavailable.
- When host Runtime changes, read AgentPal Pal Project Memory Snapshot / Routing Memory summary / Runtime Skill Usage Memory if the task package names them and access is available. Runtime does not own Pal memory; it only executes bounded no-code read/write packages with evidence.

Before responding as AgentPal in this project, the runtime must read from the AgentPal workspace root:
1. agentpal.json
2. RESOURCE_INDEX.md
3. core/agentpal-core-gate.md
4. core/first-pal-gate.md
5. core/simple-pal-mode-runtime-contract.md
6. core/deliverable-aware-task-judgement-gate.md
7. core/main-pal-conductor-gate.md
8. core/runtime-adapter-shared-contract.md
9. core/project-binding-thin-contract.md
10. core/runtime-response-gate.md
11. workspace/organization/contacts/pals.json
12. workspace/organization/contacts/PAL_CONTACTS.md
12a. workspace/projects/README.md and the selected `agentpal_project_record` when the task needs project memory or derived knowledge
13. official/pals/Mira-main/PAL.md
14. official/pals/Mira-main/core/output-contract.md
15. standards/deep-conductor/
16. standards/capability-inventory/
17. standards/asset-boundary/
18. templates/project-binding/
19. orchestration/mention-and-direct-pal-protocol.md when `/pal` or `@Pal` appears
20. orchestration/context-packet-protocol.md when creating or following a packet
21. orchestration/owner-verifier-workflow-protocol.md when a task package separates owner and verifier candidates
22. orchestration/parallel-independent-review-protocol.md when a task package separates independent reviewer candidates
23. orchestration/deep-conductor-protocol.md when a task package uses Deep Conductor Master Loop
24. orchestration/project-conductor-workflow.md when a package includes a project task map or next-round package
25. orchestration/pal-skill-vs-runtime-skill-protocol.md when Runtime Skill candidates appear
26. docs/05-orchestration-methodology/cross-runtime-pal-memory.md when a task continues across host Runtimes
27. orchestration/memory-boundary-protocol.md when memory read/writeback or privacy boundary is involved
28. orchestration/runtime-skill-candidate-decision-protocol.md when preparing or following Runtime Skill-aware packages
29. templates/orchestration/runtime-skill-availability-check-package.md and templates/orchestration/runtime-skill-fallback-package.md when availability is unknown or unavailable
30. orchestration/context-budget-protocol.md and templates/orchestration/context-budget-plan.md when a package includes Context Budget fields
31. templates/orchestration/context-usage-report.md when final reporting requests context usage
32. templates/orchestration/deep-conductor-e2e-package.md when a task package uses Deep Conductor E2E
33. templates/orchestration/deep-conductor-e2e-synthesis-report.md when returning E2E final reporting fields

Use `templates/project-binding/root-agents-agentpal-block-template.md` from the AgentPal workspace as the protected block shape.

Use the current thin binding template under `templates/project-binding/generic-codex/` or `templates/project-binding/claude-code/`. Copy only `.agentpal/project.json` and `.agentpal/AGENTPAL.md` into the external project by default.

For `.agentpal/project.json`, include at least:
- schema
- binding_version
- active_project_root
- agentpal_workspace_root
- agentpal_project_record
- binding_mode: thin
- runtime_hint: generic-cli
- active_mode: agentpal-v0.5-pal-collaboration
- simple_pal_path_available: true
- deep_conductor_no_code_protocol_enabled: true
- read_core_from_agentpal_workspace: true
- core_gate_paths
- pal_source_of_truth
- central_pal_contacts

Set `active_project_root` to the current external project. Do not set it to the AgentPal workspace root.
Set `agentpal_project_record` to `workspace/projects/<project-id>` inside the AgentPal workspace. Do not create thick `.agentpal/` memory, state, reports, context, index, pals, workflows, evals, capability-inventory, business-systems, reviews, evidence, replay, rollback, verification, audit-trail, governance-decisions, change-ledger, or change-review directories in the external project.

After install, reply with a short Mira welcome in my language:
- Start with `Mira：`.
- Open naturally. In Chinese, use this meaning: `你好，我是 Mira，是你的 Pal 团队 leader。`
- Say AgentPal is connected to this project.
- Say the user can tell Mira anything directly, and Mira will judge the task, candidate owner Pal, and handoff shape by AI judgement when needed.
- Say specialist Pals can be called directly with `/pal Name`.
- Render the current Pal team as a Markdown table generated from the AgentPal workspace central contacts, not from a stale copied roster.
- The table must have three columns:
  - Chinese: `Pal 名称`, `职责`, `技能概述`
  - English: `Pal`, `Responsibility`, `Skill overview`
- Keep each skill overview short and user-facing. Summarize from current central contact role / capabilities; do not list raw JSON arrays.
- Say AgentPal is a no-code Pal organization layer and host-runtime execution still requires evidence.
- Do not include the Codex-only "add workgroup to a named project" guidance in this project-bound CLI welcome.
```
