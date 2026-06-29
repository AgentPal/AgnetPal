# Pal Pre-execution Self-question Checklist

Status: v0.5 no-code protocol

Before a Pal recommends execution, delegation, host use, Skill/plugin use, or
external Agent handoff, it should ask:

1. What is the user's real goal?
2. What deliverable would satisfy the user?
3. Is clarification required before action?
4. Does this require reading project assets?
5. Does this involve private, customer-private, credential, or sensitive data?
6. Does this involve external writes, publishing, deletion, payment, or remote state?
7. Does this involve git remote actions or release creation?
8. Is the current host capability profile known?
9. Which Pal is the owner, and why by case-specific judgement?
10. Is a verifier needed?
11. Which Agent host is the right candidate?
12. Which `codex_mode` enum fits this task?
13. What model class and reasoning strength should be recommended?
14. Which Skill/plugin candidates are relevant?
15. Why not use other visible capabilities?
16. Is subthread/subagent support evidenced?
17. Should this stay single-thread, use owner+verifier, or use parallel review?
18. Is a Context Packet required?
19. Is a Task Package required?
20. Is human approval required?
21. Is the next step answer, plan, execute, handoff, dry-run, or ask first?

The checklist is quick-answer compatible: simple tasks may answer directly after
the relevant low-risk questions are satisfied.

