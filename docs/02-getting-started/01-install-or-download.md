# Install Or Download

AgentPal v0.5 does not have a package-manager install, app installer, CLI installer, daemon, scanner, connector setup, or marketplace account.

You use it by placing the AgentPal workspace on your machine and opening it in a host runtime that can read Markdown and JSON files.

## Option A: Clone

```text
git clone <AgentPal-repository-url>
cd AgentPal
```

Use this when you want Git history and local commits.

## Option B: Download A Release Or Zip

Download the archive, extract it, and keep the extracted folder as your AgentPal workspace.

Before sharing or re-publishing a copy, check that it does not contain private project files, credentials, local settings, customer data, or machine-specific paths.

## What Should Be In The Workspace

A normal AgentPal workspace contains Markdown and JSON assets such as:

- `README.md` and `README.zh-CN.md`
- `prompts/`
- `core/`
- `docs/`
- `official/pals/`
- `workspace/organization/contacts/`
- `templates/`

You do not need Python, Node.js, Rust, Go, a web server, or a background service for ordinary initialization.

## What Not To Install

Do not install AgentPal as if it were:

- an Agent runtime
- a tool connector
- a file scanner
- an app runtime
- a model router
- a marketplace package
- a background sync service

If a host runtime has its own tools or plugins, those belong to that host runtime. AgentPal may record or reason about visible capability evidence, but it does not provide those tools itself.

## Next Links

- [Quick start](00-quick-start.md)
- [Use with Codex](02-open-in-codex.md)
- [Use with Claude Code](03-open-in-claude-code.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
