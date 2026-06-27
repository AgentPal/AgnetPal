# Token / Cost-aware Conductor Policy

AgentPal should conserve context and cost without weakening verification.

This policy guides Mira, owner Pals, and Deep Conductor-style planning when deciding how much to read, which profiles to open, what model or reasoning strength to suggest, and when to reuse memory.

## Reading Policy

Use index-only reading when:

- the user asks for navigation, scope, or a file list;
- the task only needs candidate discovery;
- the current index already identifies the right file.

Read full text when:

- the file is an instruction, protocol, contract, or acceptance source for the current task;
- a claim must be verified from exact wording;
- the Runtime will edit or review that file.

Summarize first when:

- a large source may contain relevant sections but full reading would exceed the budget;
- the task needs topic discovery before exact verification;
- multiple long sources compete for attention.

Reuse memory when:

- prior routing, user preference, or verification history is relevant;
- the memory is fresh enough for the task risk;
- the response states when memory is unverified or may be stale.

## Model And Reasoning Policy

Prefer a stronger model or higher reasoning when:

- ownership, safety, release, legal, security, or architecture risk is high;
- multiple candidate routes conflict;
- verification quality matters more than speed or cost;
- a task has many dependencies or ambiguous acceptance criteria.

Prefer a lower-cost model or lower reasoning when:

- the task is mechanical, low-risk, and well-scoped;
- acceptance criteria are explicit;
- a verifier will review the output;
- the work can be safely retried.

Use a Runtime-installed Skill candidate when:

- the host Runtime has current evidence that the Skill is available;
- the Skill materially reduces manual context or tool work;
- the Skill has clear inputs, outputs, and evidence requirements.

Do not use a Runtime-installed Skill merely because a profile exists.

## Required Counts

Reports for conductor-shaped tasks should record:

- `context_read_count`: number of files or artifacts actually opened for content;
- `profile_read_count`: number of Capability Inventory or Runtime / Model / Skill / Plugin / MCP profiles actually opened;
- `memory_used`: yes/no, with a short source description.

Known-through-index paths are not content reads.

## Verification Boundary

Token savings cannot sacrifice verification quality.

If a task needs exact evidence, read the exact evidence. If a check was skipped to save context or cost, report it as `not-run` with the reason.

## Anti-patterns

Do not:

- read all Pal Packs by default;
- forward full chat history into every packet;
- use memory as proof of current Runtime capability;
- skip verification because the plan sounds plausible;
- claim a Skill, plugin, or MCP was available without current evidence.
