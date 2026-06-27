# Mention Consult Template

Use when a user or owner Pal mentions `@PalName` without explicitly asking for handoff.

```text
Context Packet
- schema: agentpal.context-packet.v0.3
- packet_id: <workflow-local id>
- created_at: <date>
- from_pal: <current owner>
- to_pal_candidate: <mentioned Pal>
- mode: consult | review
- explicit_user_call: @<Pal>
- owner_status: consultant_candidate | reviewer_candidate
- user_goal: <safe summary>
- task_summary: <bounded consult question>
- current_state: <known state and evidence available>
- constraints: <do-not-do list>
- relevant_files: <relative paths or summaries only>
- can_read: <specific files, summaries, evidence>
- cannot_read: <full chat history, private memory, secrets, other reviewer drafts>
- can_receive_outputs_from: <accepted final reports only>
- needed_output: <consult output>
- output_contract: <short structure>
- verification_requirements: <if any>
- privacy_policy: public-safe; sensitive context excluded by default
- sensitive_context: none | excluded | summarized with approval
- expiration: single workflow
- handoff_notes: @Pal consult does not transfer ownership by default
- return_to: <Mira or current owner Pal>
- final_report_required: true

Expected consult output:
- judgement
- evidence or assumptions
- risks
- recommendation
- confidence / uncertainty
- what the current owner should decide next
```

`@Pal` consults do not change ownership unless the user or current owner explicitly requests owner transfer.

Rules:

- `@Pal` is consult / review by default.
- The mentioned Pal receives a Context Packet, not the full chat history.
- The mentioned Pal writes a structured final report for Mira or the owner Pal to summarize.
- If the user says "hand this to Quinn" or equivalent, use `owner_transfer` / `handoff` instead of consult.
- `@Pal` is not group chat and does not start parallel runtimes automatically.
