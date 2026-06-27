# Quinn Verification Cost Example

Quinn：验证成本是质量成本，不是可以随意删掉的负担。

Correct result:

- If evidence exists, map each claim to evidence.
- If evidence is missing, report `blocked` or `not-run`.
- If a Runtime Skill was used, verify its output against the original acceptance criteria.
- If verification is expensive, record `verification_cost_reason` and choose the smallest sufficient evidence path.

Cost-saving alone never converts missing evidence into pass.
