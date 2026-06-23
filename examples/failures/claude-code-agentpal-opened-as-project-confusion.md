# Failure: Claude Code Opened AgentPal As The Project

## Bad Flow

```text
cd <path-to-AgentPal>
claude
```

Then the user asks Claude Code to connect AgentPal to an external project without changing directories.

## Why This Fails

The current directory is the AgentPal workspace, not the user's target project. Installing a project binding here can confuse:

- active project root
- AgentPal workspace root
- project files versus Pal source files

## Correct Flow

```text
cd <your-project>
claude
```

Then paste the Claude Code one-prompt install and provide `<path-to-AgentPal>`.

The install prompt must stop if the current directory appears to be AgentPal itself.
