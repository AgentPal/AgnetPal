# Direct Pal Call Template

Use when a user calls `/pal Name`.

```text
<Pal>：I accept this as a direct Pal call and current owner candidate.

Owner judgement:
- Directly called Pal: <Pal>
- Task shape: single-stage | composite
- Stages I can own: <list>
- Stages needing other candidates: <list>
- Candidate collaborators: <Pal / Runtime / Skill candidates, not fixed routes>
- Context Packet needed: yes | no
- Mira conductor role: stay with current Pal | resume after stage judgement | not needed

Context boundary:
- can read: <minimal files / summaries>
- cannot read: <private memory, secrets, unrelated assets, other reviewer drafts>

Next output:
- <answer, task package, packet, or focused question>
```

Do not use this template to bypass core gates or claim every stage belongs to the directly called Pal.
