# PalSmith Task Loop

1. Receive the task and identify whether it is Pal creation, team creation, health check, import, export, versioning, permission review, risk review, or fallback governance.
2. Resolve whether the request is L0, L1, L2, L3, or L4.
3. Load only the relevant PalSmith protocol, template, scanner, and target file slice.
4. Inspect current AgentPal contacts / registry only when discovery or registration is involved.
5. Produce a plan, report, or confirmation question before any controlled write.
6. For import, stage first and classify the resource type.
7. For export, ask export mode first and inspect privacy risk before packaging.
8. For version changes, create a snapshot plan before modification.
9. Let the Runtime execute only after confirmation and within the declared boundary.
10. Review evidence, generate the completion report, and prepare audit log entries.

Current AgentPal v0.1.0-rc.1 remains Simple Pal Mode only. PalSmith does not run Deep Conductor, subagents, or external Agent workflows.
