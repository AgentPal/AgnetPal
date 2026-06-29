# Runtime-installed Skill Orchestration Guide

Runtime-installed Skill Orchestration is a no-code AgentPal method for naming host capability candidates inside a Task Package.

It helps a Pal say: "This task may benefit from a host Skill, plugin, MCP tool, browser tool, office-document tool, repository-analysis tool, or other installed capability. The current host must confirm availability and execute it if allowed."

It does not make AgentPal a runtime, tool caller, scanner, installer, validator, connector, or automation layer.

## Runtime-installed Skill

A runtime-installed Skill is supplied by the host runtime or its plugin/MCP/tool surface.

Examples:

- browser inspection capability
- document rendering capability
- repository analysis capability
- GitHub or issue-tracker tool exposed by the host
- MCP tool made available by the host

The host installs, invokes, permissions, and evidences the capability. AgentPal may describe it as a candidate, but AgentPal does not own it.

## Pal-owned Skill

A Pal-owned Skill is a no-code method stored under a Pal Pack. It describes judgement, intake, context slicing, task packaging, verification, and learning behavior.

Keep the labels separate:

- `pal_owned_skills_used`: Pal methods used to prepare the package
- `runtime_skill_candidates`: host capabilities that might inspect or execute something
- `plugin_candidates`: host plugins that might be available
- `mcp_tool_candidates`: host MCP tools that might be available

Do not copy runtime Skills into Pal Packs. Do not put Pal-owned Skills into runtime availability checks.

## Capability Evidence

Availability can come from:

- visible current runtime evidence
- runtime-reported capability
- a user-maintained manual profile

If a capability is not visible, mark it `unknown`, `unavailable`, or `not-run`. Do not invent a scan.

## Standard Flow

1. Identify the task need.
2. Select the Pal-layer owner.
3. Name host capability candidates only if they are relevant.
4. Ask the host runtime to confirm availability when needed.
5. Prepare a Task Package with fallback behavior.
6. Host runtime executes or reports unavailable.
7. The owner Pal or verifier reviews returned evidence.
8. Write a memory candidate only when privacy and scope allow it.

## Fallback

If the capability is unavailable, use one of:

- ordinary Task Package without the specialized capability
- different capability candidate
- user confirmation to install, enable, or choose another host
- `blocked` / `not-run` report when execution would be unsafe or impossible

## Risks

- treating a profile as proof of installation
- treating a previous success as a hard route
- mixing Pal-owned Skill learning with runtime Skill availability
- letting a runtime Skill output bypass Pal verification
- leaking private local paths, source material, or credentials into public examples
- creating keyword-to-Skill rules that bypass AI judgement

## Next Links

- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
- [Capability Inventory](05-capability-inventory.md)
- [Verification Result Record](07-verification-result-record.md)
