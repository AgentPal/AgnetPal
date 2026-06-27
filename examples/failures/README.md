# Failure Examples

These examples describe incorrect AgentPal behavior and the corrected behavior.

They are release-safe, synthetic examples. They must not be used as routing rules or runtime instructions.

Use them when reviewing regressions around fake Pal responses, Mira over-answering, hard-coded routing, Subagent Mode evidence, external project context, Codex generic labeling, contact boundaries, no-code future boundaries, Pal Skill / Runtime Skill separation, Deep Conductor executor confusion, skipped Capability Inventory, context overload, missing verification plans, missing memory writeback, cross-runtime memory loss, Runtime Skill memory confusion, fixed-route routing memory, and private memory leaks.

R57 memory-continuity examples:

- `runtime-switch-loses-pal-memory.md`
- `routing-memory-becomes-fixed-route.md`
- `runtime-skill-memory-confused-with-pal-skill.md`
- `project-memory-leaks-private-data.md`
