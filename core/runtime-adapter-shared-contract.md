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
- parse `/pal Name` and `@Pal` as AgentPal plain-text protocols when they appear in user input
- resolve named Pals through current contacts / registry instead of copied Pal lists
- follow `orchestration/mention-and-direct-pal-protocol.md` and `orchestration/context-packet-protocol.md` for direct calls, consults, reviews, handoffs, and owner transfers

## Adapter Must Not

- copy full AgentPal rules into external projects
- maintain its own independent copy of First Pal Gate
- maintain a stale Pal roster as source of truth
- copy full orchestration protocols into `.agentpal/`
- copy full Mira assets into `.agentpal/`
- turn future design into current behavior
- treat Runtime as a Pal
- treat `/pal` or `@Pal` as required native CLI features
- copy full chat history into Context Packets
- present Context Packet as an automatic message bus

If a core rule changes, adapter behavior should inherit the change by reading the AgentPal workspace core gates, without rewriting every adapter prompt.

## `/pal` And `@Pal` Handling

If the host runtime has no native slash-command or mention support, it should still treat `/pal Name` and `@Pal` as user text:

- `/pal Name` means direct owner-candidate mode for the named Pal after core gates.
- `@Pal` means consult or review by default and must use a bounded Context Packet.
- explicit handoff or takeover wording may become `handoff` or `owner_transfer`.
- all named Pals are resolved from `contacts/pals.json` and `registry/pal.index.json`.
- Context Packets must use `can_read`, `cannot_read`, `needed_output`, and `verification_requirements`; they must not copy full chat history.

This remains no-code protocol behavior. It does not start background Pals, Subagent Mode, external Agent calls, Deep Conductor automation, or runtime parallelism.
