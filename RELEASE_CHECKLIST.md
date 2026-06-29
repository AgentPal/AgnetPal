# AgentPal v0.5.0-rc.1 Release Checklist

Use this checklist before publishing AgentPal v0.5.0-rc.1 as a public GitHub pre-release.

This checklist does not authorize `git push`, `git pull`, `git fetch`, tag creation, or GitHub Release creation by itself.

## Required Local Checks

- [ ] `README.md` presents AgentPal as a no-code Pal organization layer.
- [ ] `README.zh-CN.md` matches the English README's current v0.5 boundary.
- [ ] `START_HERE.md` exists for fresh-clone onboarding.
- [ ] `AGENTS.md`, `PAL.md`, `SKILL.md`, `agentpal.json`, and `RESOURCE_INDEX.md` exist.
- [ ] `prompts/codex/initialize-agentpal-workspace.md` is the current Codex initialization entry.
- [ ] `INIT_PROMPT.md` is absent.
- [ ] `LICENSE` is MIT.
- [ ] `THIRD_PARTY_NOTICES.md` exists.
- [ ] `CHANGELOG.md`, `RELEASE_NOTES.md`, `RELEASE_MANIFEST.md`, and `GITHUB_RELEASE_DRAFT.md` use v0.5.0-rc.1 release-candidate wording.

## Official Pal Checks

- [ ] Official Pal directory count is 10.
- [ ] Central active contact count is 10.
- [ ] Faye is included.
- [ ] README and README.zh-CN Pal tables each list 10 Pals.
- [ ] Each official Pal has `PAL.md`, `pal.json`, `SKILL.md`, `AGENTS.md`, `README.md`, and `core/output-contract.md`.
- [ ] `workspace/organization/contacts/pals.json` is the source of truth.

## Runtime And Claim Boundary

- [ ] Codex is stated as the verified first path.
- [ ] Claude Code is limited / minimal handoff evidence only.
- [ ] Generic CLI Agent is a compatibility prompt path.
- [ ] DeepSeek / DeepSeek-TUI are experimental or version-help only.
- [ ] OpenCode and Gemini are unavailable in current evidence.
- [ ] Plan Mode UI evidence is unavailable.
- [ ] Goal Mode evidence is limited.
- [ ] External write systems are not generally validated.
- [ ] AgentPal is not described as an Agent runtime, multi-Agent runtime, execution layer, app runtime, CLI installer, daemon, scanner, connector layer, marketplace, or hosted executor.

## Public-Safe Package Checks

- [ ] No `.git/` is included in the release package.
- [ ] No internal development directory or local report path is included.
- [ ] No local clean-copy directory is included.
- [ ] No private memory, private project facts, real customer data, credentials, secrets, tokens, or API keys are included.
- [ ] No temporary files, caches, or system artifacts are included.
- [ ] No deprecated `INIT_PROMPT.md` entry is included.
- [ ] No generated external-project `.agentpal/` test folders are included.

## Validation Checks

- [ ] JSON parse checks pass.
- [ ] Markdown link checks pass.
- [ ] Claim guard scan passes.
- [ ] Internal/local path leak scan passes.
- [ ] Credential scan passes.
- [ ] Added executable artifact check passes.
- [ ] Clean-copy validation passes.
- [ ] Zip content check passes.
- [ ] `git diff --check` passes before publication.
- [ ] `git status --short --branch` is reviewed before publication.

## Publication Gate

Do not publish until maintainers explicitly authorize all intended remote actions.

- [ ] Confirm final intended release commit.
- [ ] Confirm intended tag name.
- [ ] Confirm remote repository.
- [ ] Push branch only after authorization.
- [ ] Create or push tag only after authorization.
- [ ] Create GitHub Release only after authorization.
- [ ] Mark the GitHub Release as a pre-release unless maintainers decide otherwise.
