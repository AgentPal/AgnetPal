# Plugin Scan Protocol

When Mira needs current Skill, plugin, or MCP information:

1. Check existing registry files.
2. Ask the current Runtime to list available Skills/plugins if supported.
3. Search runtime-specific configuration only when safe, relevant, named, and within the package scope.
4. Ask the user if runtime inspection is unavailable.
5. Record results in a Host Capability Snapshot or approved capability inventory file.
6. Include scan date, method, evidence, and confidence.
7. Refresh before important dispatch or after runtime configuration changes.

This protocol is bounded discovery, not an automatic scanner. A visible Skill or
plugin is a candidate only. Use
`standards/agent-use/skill-plugin-invocation-record.md` to prove whether a
candidate was invoked, dry-run, handed off, inspected, skipped, or blocked.

