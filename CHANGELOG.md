# Changelog

All notable public changes to AgentPal are recorded here.

## v0.5 - local public-docs rewrite window

### Changed

- Rewrote the public README entry to explain AgentPal as a no-code Pal organization layer rather than an Agent runtime.
- Clarified the Skill / Pal / Agent relationship:
  - Skill is a capability package.
  - Pal is a working partner that uses Skills and Agents.
  - Agent is the execution runtime.
- Clarified multi-Pal versus multi-agent positioning.
- Updated the public roster to the current 10 official Pals: Mira, Atlas, Nova, Faye, Vega, Quinn, Morgan, Harper, Rhea, and PalSmith.
- Added Codex-first installation and initialization guidance using `prompts/codex/initialize-agentpal-workspace.md`.
- Reworked docs navigation so evidence and release records remain available but are not the primary user path.

### Evidence Boundary

- Codex is the verified first path for v0.5 public docs.
- Claude Code remains limited to minimal handoff evidence unless future full host acceptance passes.
- Generic CLI agents remain compatibility paths, not broad validated support.
- OpenCode and Gemini are unavailable in current evidence.
- Plan Mode UI support is unavailable in current evidence.
- Goal Mode evidence is limited.
- DeepSeek / DeepSeek-TUI remain experimental or version-help level.

### Not Added

- No runtime code.
- No CLI, app, installer, scanner, daemon, connector layer, marketplace, or external-system executor.
- No GitHub Release, tag, push, pull, or fetch as part of the local documentation rewrite.

## v0.4 / v0.5 local evidence line

AgentPal added local no-code organization assets for:

- central workspace and project records
- Pal asset standards
- Org Pack and FDE Pack standards
- Faye / Delivery Pack integration
- PalSmith v0.5 creation and governance standards
- Agent-use decision protocols and host capability evidence records
- Codex-first real-host confirmation and evidence-limit guards

These records are local release evidence unless a future release explicitly publishes them remotely.

## v0.3.0-rc.1 - 2026-06-27

Release candidate for the v0.3 no-code orchestration prototype line.

### Added

- Deep Conductor E2E guidance, package templates, examples, failure examples, evals, and readiness records.
- Context Packet, Context Access, `/pal Name`, and `@Pal` no-code collaboration protocols.
- Owner + Verifier, Parallel Independent Review, Project Conductor, and Cross-Runtime Pal Memory protocols.
- Runtime Skill candidate decision, availability check, fallback package, and Runtime Skill-aware Task Package assets.
- Qualitative Context Budget and Token / Cost-aware Conductor guidance.
- PalBench Collaboration coverage for collaboration, replay, and gap-repair scenarios.

### Clarified

- v0.3.0-rc.1 is a release candidate, not a stable release.
- Deep Conductor is no-code orchestration, not automatic runtime execution.
- AgentPal does not provide automatic execution, a CLI, app, service, scanner, validator, installer, daemon, database, token meter, cost calculator, automatic Subagent launch, automatic external Agent calls, or statistical benchmark proof.

## v0.2.0-rc.1

Release candidate for the v0.2 first-phase no-code Pal layer improvements.

### Added

- PalSmith end-to-end creation flows for a first professional Pal and a small AI team.
- Mira-first usage guides, prompt cards, task package templates, examples, and self-tests.
- Official Pal task example library.
- Minimal Capability Inventory profiles as manual AI judgement inputs.
- PalBench Light as a qualitative release regression suite.
- Runtime Adapter stability guidance, troubleshooting prompt cards, upgrade notes, and thin-binding regression coverage.

### Clarified

- AgentPal remains a Markdown / JSON / protocol Pal layer for existing runtimes.
- Simple Pal Mode remains the active runtime policy.
- Deep Conductor, autonomous multi-agent runtime behavior, automatic capability probing, automatic Routing Reward Memory writeback, and statistical benchmark claims are not current v0.2 behavior.

## v0.1.0-rc.1

Initial public release candidate for AgentPal as a Pal layer and Pal Pack Standard practice.

### Added

- AgentPal Workspace root files for runtime initialization, Pal identity, and release-safe navigation.
- Simple Pal Mode and Mira as the default Main Pal, Leader Pal, and Conductor.
- Official bundled Pal Packs for Mira, Atlas, Vega, Rhea, PalSmith, Quinn, Morgan, Harper, and Nova.
- Contacts and registry files as Pal discovery sources.
- Runtime Response Gate, AI routing judgement rules, Pal context slicing, asset loading budget, memory summary loading, and Task Package output contract protocols.
- External project workgroup binding templates.
- Codex, Claude Code, and Generic CLI Agent prompt-based adapter paths.
- Public release files, third-party notices, and MIT license.

### Clarified

- AgentPal is a Pal layer, not an Agent layer, multi-agent runtime, or execution layer.
- Pal Packs are runtime-readable working assets, not independent agent processes.
- Private memory, private state, real reports, secrets, and internal development notes must not be published.
