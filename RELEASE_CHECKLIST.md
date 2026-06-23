# Release Checklist

Use this checklist before publishing AgentPal v0.1.0-rc.1 as a public MIT GitHub release.

## Root Release Files

- [ ] `README.md` exists and presents AgentPal as a Pal layer and Pal Pack Standard practice.
- [ ] `README.zh-CN.md` exists and matches the English README's current-version boundary.
- [ ] `AGENTS.md` exists and states the Runtime Response Gate, Simple Pal Mode only, Mira default routing, contacts/registry source of truth, and public-safe boundaries.
- [ ] `PAL.md` exists and describes the AgentPal Workspace identity, not a single Pal.
- [ ] `SKILL.md` exists and identifies AgentPal as a Workspace-level Skill entry, not a single-purpose Skill.
- [ ] `INIT_PROMPT.md` can be copied into Codex, Claude Code, or another supported runtime for initialization.
- [ ] `agentpal.json` parses as valid JSON and uses version `v0.1.0-rc.1`.
- [ ] `RESOURCE_INDEX.md` exists as navigation, not a default full-context bundle.

## README And Docs

- [ ] `README.md` and `README.zh-CN.md` do not describe future work as active.
- [ ] `docs/` has a clear user-facing navigation path.
- [ ] Current docs distinguish AgentPal Workspace, Pal Pack, Pal, Skill, and execution runtime.
- [ ] Future design docs are clearly marked as future or not active in v0.1.0-rc.1.
- [ ] Research docs for orchestration methodology and PalBench are present and clearly marked as design foundation.
- [ ] R33 PalBench small-sample report is present, cautious, and does not claim statistical significance or model superiority.
- [ ] R32 Fast Route / Deep Conductor boundary is documented: Fast Route current, Deep Conductor future-only.
- [ ] Mira is documented as Main Pal / Leader Pal / Conductor, with secretary as communication layer.
- [ ] Capability Inventory, Context Access List, Workflow Topology, Pal Isolation, and Routing Reward Memory protocols are present.
- [ ] Context Access List, Pal Isolation, Shared Memory, Routing Reward Memory, and PalBench additions are present.
- [ ] Orchestration templates, capability profile templates, and PalBench result template are present.
- [ ] PalBench eval drafts and orchestration examples are present.
- [ ] PalBench R33 examples are public-safe and use synthetic or placeholder data.
- [ ] No internal development reports are linked from public onboarding navigation.

## Pals

- [ ] Official bundled Pal directories exist: `pals/Mira-main`, `pals/Atlas-developer`, `pals/Vega-research`, `pals/Rhea-system`, `pals/Quinn-quality`, `pals/Morgan-document`, `pals/Harper-writing`, and `pals/Nova-product`.
- [ ] Each official Pal has `PAL.md`, `pal.json`, `SKILL.md`, `AGENTS.md`, `README.md`, and `core/output-contract.md`.
- [ ] Specialist Pals are described as Pal Packs, not independent agent processes.
- [ ] Pal-owned Skills are stored under the owner Pal's own `skills/` directory.
- [ ] Pal memory, state, and report directories contain only public-safe placeholders unless they are ignored runtime-private files.

## Contacts And Registry

- [ ] `contacts/pals.json` contains only valid Pal Packs.
- [ ] `registry/pal.index.json` matches the current official bundled Pal set.
- [ ] Mention aliases resolve `/pal Name` by display name or alias.
- [ ] Contacts and registry are documented as the source of truth for Pal discovery.
- [ ] Individual Pal Packs do not maintain hard-coded route maps for other Pals.

## Runtime Boundary

- [ ] AgentPal v0.1.0-rc.1 uses Simple Pal Mode only.
- [ ] AgentPal is not described as an Agent layer, multi-agent runtime, execution layer, desktop app, web app, marketplace, daemon, scanner, validator, installer, or service.
- [ ] Initialization requires no Python, Node.js, Rust, Go, CLI, UI, or background service.
- [ ] Execution claims require evidence from the host runtime.
- [ ] Exact token metering is not claimed as available in v0.1.0-rc.1.
- [ ] Claude Code project setup is documented as `cd <your-project>` then `claude`, followed by the one-prompt install.
- [ ] `claude --add-dir <path-to-AgentPal>` is documented only as fallback / advanced use, not the required default path.
- [ ] `.claude/settings.local.json` is documented as local machine configuration and not for commit.
- [ ] Generic CLI Agent setup is documented through `AGENTS.md` and `.agentpal/`.
- [ ] Research/future orchestration docs do not activate Subagent Mode, external Agent calls, Deep Conductor, or runtime dependency requirements.

## Project Install Prompts

- [ ] `prompts/claude-code/install-agentpal-current-project.md` exists.
- [ ] `prompts/claude-code/remove-agentpal-current-project.md` exists.
- [ ] `prompts/claude-code/verify-agentpal-current-project.md` exists.
- [ ] `prompts/cli-agent/install-agentpal-current-project.md` exists.
- [ ] `prompts/cli-agent/remove-agentpal-current-project.md` exists.
- [ ] Claude Code install prompt preserves existing `CLAUDE.md`, `AGENTS.md`, and settings content.
- [ ] Claude Code install prompt merges only `permissions.additionalDirectories`.
- [ ] Generic CLI prompt does not depend on Claude Code settings.
- [ ] Install prompts do not copy all Pal Packs into the user project.
- [ ] Install prompts do not import the whole AgentPal workspace into project instruction files.

## Public-Safe Boundary

- [ ] No private user memory is included.
- [ ] No private project state is included.
- [ ] No real task, user, verification, or internal development reports are included.
- [ ] No API keys, tokens, passwords, credentials, secrets, or private keys are included.
- [ ] No customer data or proprietary user project data is included.
- [ ] No local absolute paths are included in public-facing release files.
- [ ] Examples and templates use synthetic or placeholder data.
- [ ] `.gitignore` excludes runtime-private memory, state, reports, raw imports, temporary files, and system files while keeping release-safe README/template files.
- [ ] `.gitignore` excludes `.claude/settings.local.json`.

## License And Notices

- [ ] `LICENSE` exists and is MIT.
- [ ] `THIRD_PARTY_NOTICES.md` exists.
- [ ] Third-party resources keep their original licenses and notices.
- [ ] No long third-party source, README, Skill, or documentation text is copied into the release.

## Release Notes

- [ ] `CHANGELOG.md` records user-visible release changes for `v0.1.0-rc.1`.
- [ ] `RELEASE_NOTES.md` is user-facing and explains who the release is for, who it is not for, what is included, and what is not included.
- [ ] `GITHUB_RELEASE_DRAFT.md` is suitable for manual GitHub Release drafting and includes What's included, Current status, Known limitations, Getting started, and Safety notes.

## Validation

- [ ] JSON parse checks passed.
- [ ] Capability profile JSON templates and examples parse as valid JSON.
- [ ] no-runtime check confirms no scripts, package files, CLI, UI, installer, daemon, scanner, or validator were added.
- [ ] no-hardcoded-routing check confirms no new task/domain fixed route rules.
- [ ] Markdown sanity checks passed.
- [ ] Relative links in root release files were reviewed.
- [ ] Public-safety keyword search was reviewed by a human.
- [ ] Version references in root release files use `v0.1.0-rc.1`.
