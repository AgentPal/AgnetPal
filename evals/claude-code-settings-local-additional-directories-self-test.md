# Claude Code Settings Local Additional Directories Self-Test

## Purpose

Verify safe merge behavior for `.claude/settings.local.json`.

## Pass

- Missing `.claude/settings.local.json` is created.
- Existing valid JSON is preserved.
- Only `permissions.additionalDirectories` is merged.
- Existing allow / deny / ask rules remain unchanged.
- AgentPal path is appended only once.
- Invalid JSON causes a stop-and-ask response, not overwrite.
- `.gitignore` contains `.claude/settings.local.json`.
- Local AgentPal absolute path is not written to `.claude/settings.json`.

## Fail

- Existing Claude settings are cleared.
- Duplicate AgentPal paths are added.
- Invalid JSON is overwritten.
- Local absolute AgentPal path is committed into team settings.
