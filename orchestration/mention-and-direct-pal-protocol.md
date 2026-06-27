# Mention And Direct Pal Protocol

This protocol defines v0.3 no-code behavior for `/pal Name` and `@PalName`.

It works through current contacts / registry and Context Packets. It does not create a native slash command, automatic Pal process, background worker, or runtime-level message bus.

## Entry Forms

### `/pal Name`

`/pal Name` is a direct Pal call. The named Pal becomes the current owner candidate for the request.

Rules:

- resolve by display name and aliases from `contacts/pals.json` and `registry/pal.index.json`;
- do not invent missing Pals;
- the directly called Pal must still apply core gates;
- the Pal must judge whether the task is single-stage or composite;
- if some stages exceed the Pal's scope, it names other Pal, Runtime, Skill, plugin, or MCP candidates and may recommend Mira resume conductor responsibility;
- direct call does not let the Pal bypass privacy, evidence, no-code, or fixed-routing boundaries.

### `@PalName`

`@PalName` is consult by default unless the user explicitly says delegate, handoff, review, owner transfer, or takeover.

Rules:

- consult means the current owner remains responsible for final synthesis;
- the mentioned Pal receives a Context Packet;
- the mentioned Pal answers only the requested perspective;
- if the user asks for handoff or owner transfer, the current owner must state the transfer reason and packet boundary.

## Collaboration Modes

| Mode | Meaning | Owner after mode |
| --- | --- | --- |
| `consult` | Ask for a bounded perspective | current owner |
| `delegate` | Ask another Pal to produce a bounded sub-output | current owner until accepted transfer |
| `handoff` | Transfer active ownership for the task or stage | target Pal candidate after acceptance |
| `review` | Ask a verifier/reviewer to judge evidence or risk | current owner or verifier stage owner |
| `owner_transfer` | User or owner explicitly moves ownership | target Pal candidate after core gates |

All modes use Context Packet. None of these modes automatically runs another Agent, subagent, or external runtime.

## Mira Default Entry

Ordinary messages go to Mira. Mira judges ownership case by case. Mira must not silently override an explicit `/pal Name` unless the named Pal is missing, unavailable, or the user asks Mira to resume conductor responsibility.

## Direct Owner Pal Judgement

When a specialist receives a direct call, it must answer from its own perspective and state:

- whether it accepts current owner-candidate status;
- whether the task has multiple stages;
- which stages it can own;
- which stages need other candidates;
- what Context Packet or evidence is needed;
- whether Mira should remain or resume conductor role.

## Explicit User Override

If the user explicitly says "let Atlas own this" or "ask Quinn only as reviewer", honor that as an instruction unless it conflicts with safety, missing Pal state, privacy, or impossible scope.

The Pal still reports if the requested owner is only a candidate and not sufficient for all stages.

## Unknown Pal

If a Pal is not in contacts / registry:

- do not pretend it exists;
- do not answer in that Pal's voice;
- say it is not currently indexed;
- suggest adding a valid Pal Pack and refreshing registry if appropriate.

## Boundary

Forbidden:

- keyword trigger routing;
- fixed collaborator maps;
- `@Pal` group chat without packets;
- direct runtime execution without Pal-layer judgement;
- transfer of full chat history or private memory.
