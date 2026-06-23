# Contributing to AgentPal

Thank you for helping improve AgentPal.

AgentPal v0.1.0-rc.1 is a Pal layer and Pal Pack Standard practice for Markdown/JSON-capable agent runtimes. Contributions should keep the repository release-safe, runtime-readable, and honest about the current Simple Pal Mode boundary.

## Ways To Contribute

- Improve public documentation.
- Improve Pal Pack protocols, templates, or examples.
- Add release-safe examples and evals.
- Propose new Pal Pack templates.
- Improve compatibility notes for Codex, Claude Code, or other Markdown/JSON-capable runtimes.
- Report unclear wording, broken links, version mismatches, or public-safety gaps.

## Contributing Pal Packs

Pal Pack contributions should be valid directory packages under `pals/<Name-role>/`.

Minimum required files:

- `PAL.md`
- `pal.json`
- `SKILL.md`
- `README.md`
- `AGENTS.md`
- `core/output-contract.md`

A useful Pal Pack should also include clear responsibility boundaries, collaboration permissions, safety notes, verification expectations, and public-safe placeholders for memory, state, reports, examples, and evals when those directories are present.

Do not register ordinary Skills, tools, models, MCP servers, plugins, raw repositories, knowledge packs, or persona packs as Pal contacts. Only valid Pal Packs should enter `contacts/` and `registry/`.

## Contributing Documentation

Documentation should be clear, public-facing English unless a file is explicitly Chinese-localized, such as `README.zh-CN.md`.

Good documentation contributions:

- explain current v0.1.0-rc.1 behavior
- distinguish Pal layer responsibilities from execution-runtime responsibilities
- use relative links
- avoid local absolute paths
- mark planned or future work as future, not active
- keep root files short and move deeper explanations into `docs/`

## Contributing Templates And Examples

Templates and examples must use synthetic or placeholder data. They should help users create Pal Packs, Context Packets, output contracts, project bindings, or release-safe documentation without exposing real private information.

## Do Not Submit Private Or Unauthorized Data

Do not submit:

- private user memory
- real user conversation history
- private project information
- internal development reports
- API keys, tokens, passwords, secrets, credentials, or private keys
- customer data
- proprietary documents without permission
- copied internal reference documents
- long third-party README, Skill, source, or documentation text
- copyrighted material without permission and proper license handling

## Runtime Boundary

AgentPal v0.1.0-rc.1 must remain usable as a Markdown/JSON workspace. Do not add required Python, Node.js, Rust, Go, service, daemon, scanner, validator, installer, desktop UI, or web UI dependencies unless a future release explicitly changes that boundary.

## Release Boundary

Everything in the public AgentPal repository is treated as release content. Keep runtime-private memory, private state, real reports, internal notes, and secrets outside the repository or under ignored local-only paths.

Third-party resources keep their original licenses and notices. Prefer short references, summaries, and links over copied third-party text.
