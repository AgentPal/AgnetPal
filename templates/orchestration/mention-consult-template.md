# Mention Consult Template

Use when a user or owner Pal mentions `@PalName` without explicitly asking for handoff.

```text
Context Packet
- from_pal: <current owner>
- to_pal_candidate: <mentioned Pal>
- mode: consult
- user_goal: <safe summary>
- task_summary: <bounded consult question>
- can_read: <specific files, summaries, evidence>
- cannot_read: <full chat history, private memory, secrets, other reviewer drafts>
- needed_output: <consult output>
- output_contract: <short structure>
- verification_requirements: <if any>

Expected consult output:
- judgement
- evidence or assumptions
- risks
- recommendation
- confidence / uncertainty
- what the current owner should decide next
```

`@Pal` consults do not change ownership unless the user or current owner explicitly requests owner transfer.
