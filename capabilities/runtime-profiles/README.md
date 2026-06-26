# Runtime Profiles

Runtime profiles describe what a host Agent runtime may support: instruction files, project binding, file access, command execution, external directory configuration, Skill/plugin/MCP support, limits, risks, and evidence.

These profiles are illustrative examples unless explicitly maintained by the user for a concrete environment. AgentPal does not automatically probe runtime capabilities.

Use runtime profiles to inform judgement about whether a Runtime is a candidate executor for a Task Package. Do not treat them as proof that a capability is available in the current session.

## Examples

- `codex.example.json`
- `claude-code.example.json`
- `generic-cli.example.json`

Each example must include:

- `example_status: illustrative`
- `not_auto_detected: true`
- `used_for: AI judgement input, not fixed routing`
- `not_a_fixed_route: true`

## Loading Rule

Read only the relevant runtime profile for the current task. If the task does not involve Runtime execution, do not load runtime profiles by default.
