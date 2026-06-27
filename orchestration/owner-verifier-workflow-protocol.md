# Owner + Verifier Workflow Protocol

Owner + Verifier is a v0.3 no-code staged workflow for work where false completion risk, release quality, safety, or acceptance evidence matters.

It does not automatically run multiple Pals, Subagents, external Agents, or runtimes. A runtime may follow the package sequentially as an execution layer and return evidence to the Pal layer.

## When To Use

Use when:

- a release, safety, quality, or acceptance gate needs evidence;
- the owner can produce the work but should not verify only its own conclusion;
- completion claims must be checked against files, command output, source references, screenshots, user acceptance criteria, or other reviewable evidence;
- a prior completion report may be incomplete or overconfident.

Do not use when:

- the task is simple, low-risk, and single-stage;
- no independent evidence is available and the user only wants a quick ordinary answer;
- the user explicitly asks for a lightweight consult rather than verification.

## Required Stages

1. User Goal Intake
   - Capture the user's goal, constraints, requested deliverable, and risk level.
   - Distinguish the user goal from any owner or runtime completion claim.
2. Owner Task Judgement
   - Select an owner Pal candidate by case-specific judgement from current contacts or registry.
   - State why the owner candidate fits this case.
   - Keep candidates as candidates, not permanent route rules.
3. Owner Task Package
   - Owner prepares the plan, scope, allowed evidence sources, acceptance criteria, and do-not-do list.
   - Owner may produce the work or a completion claim, but that claim is not itself verification evidence.
4. Verifier Context Packet
   - Owner, Mira, or the current coordinator prepares a bounded verifier context packet.
   - The packet includes expected criteria, changed files or artifacts, test results or `not-run`, source references, known risks, and evidence to check.
   - The packet excludes unrelated private memory, secrets, and full chat history unless directly required.
5. Verifier Independent Review
   - Verifier checks evidence against criteria and does not rely only on the owner conclusion.
   - Verifier can request missing evidence instead of guessing.
   - A completion report may guide what to inspect, but it is not proof by itself.
6. Verification Result Record
   - Verifier outputs a structured record with verdict `pass`, `fail`, or `blocked`.
   - `pass` requires evidence.
   - `fail` requires concrete mismatch or defect evidence.
   - `blocked` names missing evidence, unavailable checks, or boundary constraints.
7. Owner / Mira Synthesis
   - Mira or the current owner summarizes the owner claim, verifier result, evidence, gaps, risks, and recommended next action.
   - The synthesis must not upgrade a blocked or failed verification to pass.
8. Repair Package if fail / blocked
   - If verification fails or is blocked, owner or Mira prepares a repair package with required evidence, fixes, or follow-up owner candidate.
   - The repair package stays no-code unless the user explicitly asks the runtime to perform the repairs.
9. Routing Memory optional writeback
   - If the task reveals a reusable judgement pattern, record a routing memory candidate.
   - Do not write private user facts, secrets, or internal runtime paths into public release content.

## Owner Responsibility

The owner Pal is responsible for:

- understanding the task and user constraints;
- preparing plan, task package, or deliverable;
- naming expected deliverables and acceptance criteria;
- stating what evidence should prove completion;
- separating completion claim from evidence;
- responding to verifier findings with a repair package when needed.

## Verifier Responsibility

The verifier Pal is responsible for:

- checking evidence against the expected criteria;
- requesting missing evidence when the packet is insufficient;
- catching false completion patterns;
- producing a `pass`, `fail`, or `blocked` result record;
- avoiding judgement based only on owner self-report.

The verifier is not a universal business approver. The verifier checks evidence within the supplied verification scope.

## Verifier Context

The verifier should receive:

- original goal or safe summary;
- owner task package and owner claim;
- expected deliverables and acceptance criteria;
- changed files, produced artifacts, command outputs, source references, screenshots, or explicit `not-run` entries when relevant;
- known constraints, risks, and do-not-do list.

The verifier should not receive:

- unrelated private memory;
- raw secrets;
- drafts that are not needed for verification;
- full chat history by default;
- only a completion report without evidence.

## Verifier Output

Required verifier result fields are defined in `templates/orchestration/verification-result-record.md`.

The verdict must be one of:

- `pass`: evidence supports the checked criteria;
- `fail`: evidence shows at least one required criterion is unmet;
- `blocked`: evidence is missing, unavailable, out of scope, or unsafe to inspect.

## False Completion Patterns

Common patterns include:

- completion report treated as evidence;
- "all checks passed" without command output, file evidence, or source references;
- hidden `not-run` checks;
- changed files not listed in the verifier context;
- owner and verifier using the same unsupported claim as their only basis;
- release readiness claimed before release blockers are inspected.

## Boundary

Owner + Verifier is a no-code staged protocol. It does not create an automated CI system, scanner, validator, release robot, background worker, or parallel runtime. Quinn is a common quality verifier candidate, but the verifier candidate is selected by case-specific judgement from current contacts or registry.
