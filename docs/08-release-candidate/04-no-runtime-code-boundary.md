# No-Runtime-Code Boundary

AgentPal v0.1.0-rc.1 is a Markdown / JSON / protocol workspace.

It does not add runtime code, an app, or a background execution system.

## Current Boundary

AgentPal provides:

- Pal identity files
- Pal Pack structure
- public knowledge and Skill entries
- context and memory boundary rules
- output contracts
- contacts and registry files
- coordination and verification protocols
- prompts, templates, examples, and evals
- public release notes and audit summaries

AgentPal does not provide:

- desktop UI
- web UI
- CLI runtime
- daemon
- service
- scanner
- validator
- installer
- automatic file/system execution engine
- active multi-agent runtime

## Execution Responsibility

When files are read or changed, commands are run, systems are configured, or releases are published, those actions belong to the host runtime and user-controlled tooling.

AgentPal can define how a Pal should reason, package context, request evidence, and report boundaries. It does not execute actions by itself.

## Why This Matters

The no-runtime-code boundary keeps v0.1.0-rc.1 easy to inspect and conservative to release. Public users can review the workspace as files and protocols without installing a service or trusting a background process.
