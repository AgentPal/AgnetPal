# External Project Simple Pal Mode Only Self-Test

Verify external project templates inherit the current AgentPal v0.1 runtime policy.

## Files

- `templates/project-binding/prompts/install-thin-binding.md`
- `templates/project-binding/root-agents-agentpal-block-template.md`
- `prompts/join-external-project-workgroup.md`

## Expected

- The external project is the only active project.
- AgentPal workspace is only the Pal source and routing reference.
- Current task handling uses Simple Pal Mode only.
- Mira routes owned work by AI judgement.
- Owner Pal answers immediately in the same response.
- No future orchestration instructions appear in the active project-bound block.

