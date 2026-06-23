# Claude Code AgentPal Project Verification

Copy this prompt into Claude Code while your shell is inside the target project directory.

```text
Please verify whether AgentPal is correctly connected to the current project.

Check only the current project and the AgentPal path recorded in .agentpal/project.json or .claude/settings.local.json. Do not scan the whole disk.

Verify:
1. Current directory is the active project root and is not the AgentPal workspace itself.
2. .agentpal/project.json exists.
3. .agentpal/project.json contains:
   - active_project_root
   - agentpal_workspace_root
   - runtime or runtime_hint: claude-code
   - mode: simple-pal-mode-only
   - agentpal_is_pal_layer: true
4. CLAUDE.md contains exactly one AgentPal block between:
   - <!-- BEGIN AGENTPAL WORKGROUP -->
   - <!-- END AGENTPAL WORKGROUP -->
5. AGENTS.md contains exactly one AgentPal block between the same markers.
6. .claude/settings.local.json exists and is valid JSON.
7. permissions.additionalDirectories contains the AgentPal workspace path.
8. .gitignore contains .claude/settings.local.json.
9. AgentPal workspace path is readable.
10. AgentPal required files exist:
    - README.md
    - INIT_PROMPT.md
    - agentpal.json
    - RESOURCE_INDEX.md
    - contacts/pals.json
    - registry/pal.index.json
    - pals/Mira-main/PAL.md
11. contacts / registry list exactly 8 default Pals for v0.1.0-rc.1:
    - Mira
    - Atlas
    - Vega
    - Rhea
    - Quinn
    - Morgan
    - Harper
    - Nova
12. Clara is not in the default bundled Pal set.
13. Current mode is Simple Pal Mode only.
14. No active Subagent Mode or external Agent orchestration is required by the binding.
15. The block does not import the whole AgentPal workspace or AgentPal AGENTS.md.

Output a concise checklist:
- pass / fail / warning
- evidence path
- fix suggestion

If the current session cannot access the AgentPal path even though settings.local.json contains it, recommend restarting Claude Code or using temporary /add-dir <path-to-AgentPal> for this session.
```
