# Runtime Adapter Shared Contract

Runtime adapters connect AgentPal to a host runtime. They are not the AgentPal rule body.

Applies to:

- Codex
- Claude Code
- generic CLI agents
- future agent CLI adapters

## Adapter Duties

An adapter may:

- help the runtime locate the AgentPal workspace root
- tell the runtime which core gates to read
- create thin project binding files
- write runtime-specific local access configuration
- preserve a short welcome message

An adapter must:

- read `core/agentpal-core-gate.md` from the AgentPal workspace root
- read contacts / registry from the AgentPal workspace root
- load selected Pal assets on demand
- keep Runtime-specific configuration separate from AgentPal rules

## Adapter Must Not

- copy full AgentPal rules into external projects
- maintain its own independent copy of First Pal Gate
- maintain a stale Pal roster as source of truth
- copy full orchestration protocols into `.agentpal/`
- copy full Mira assets into `.agentpal/`
- turn future design into current behavior
- treat Runtime as a Pal

If a core rule changes, adapter behavior should inherit the change by reading the AgentPal workspace core gates, without rewriting every adapter prompt.
