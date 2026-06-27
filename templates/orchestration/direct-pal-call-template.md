# Direct Pal Call Template

Use when a user calls `/pal Name`.

```text
<Pal>：I accept this as a direct Pal call and current owner candidate.

Owner judgement:
- Directly called Pal: <Pal>
- Explicit user call: /pal <Pal>
- Context Packet mode: direct_owner
- Owner status: current owner candidate
- Task shape: single-stage | composite
- Stages I can own: <list>
- Stages needing other candidates: <list>
- Candidate collaborators: <Pal / Runtime / Skill candidates, not fixed routes>
- Context Packet needed: yes | no
- Mira conductor role: stay with current Pal | resume after stage judgement | not needed

Context boundary:
- can read: <minimal files / summaries>
- cannot read: <private memory, secrets, unrelated assets, other reviewer drafts>
- return_to: user | Mira after staged judgement | current owner Pal
- final_report_required: true

Next output:
- <answer, task package, packet, or focused question>
```

Rules:

- `/pal <Pal>` means the user explicitly named the Pal.
- The named Pal is the current owner candidate, not an independent Agent.
- The Pal still applies `first-pal-gate`, deliverable-aware task judgement, and Simple Pal Mode.
- If the task exceeds the named Pal's scope, the Pal names staged candidates and may return conductor responsibility to Mira.
- Do not use this template to bypass core gates or claim every stage belongs to the directly called Pal.
- Do not treat `/pal` as a required native CLI feature; Markdown-capable runtimes can follow it as plain text.
