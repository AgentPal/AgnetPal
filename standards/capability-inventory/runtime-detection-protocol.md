# Runtime Detection Protocol

Before routing important work, Mira should determine bounded runtime evidence:

1. current Runtime
2. current model
3. reasoning strength or effort controls
4. visible or named Skills, plugins, MCP servers, and commands
5. tool access: shell, browser, file system, git, GUI, or MCP
6. context limits and privacy boundaries
7. cost or latency constraints

For R157 and later, prefer a Host Capability Snapshot:

- `standards/capability-inventory/host-capability-snapshot.md`
- `templates/capability-inventory/host-capability-snapshot-template.json`

Write confirmed results only when the task package authorizes writeback and the
privacy boundary allows it.

If inspection is unavailable, ask the user or write `unknown until verified`.
Do not auto-scan the machine, invent installed capabilities, or treat a minimal
command check as full host acceptance.
