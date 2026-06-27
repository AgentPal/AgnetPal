# Subagent / External Agent Handoff Unavailable Example

## User input

The current Runtime does not support subagents. Please generate an external Agent work split.

## Expected AgentPal response shape

```yaml
handoff_status: unavailable
status_reason: current host Runtime does not provide approved subagent or external Agent execution evidence
allowed_output: manual_external_agent_handoff_package
execution_claim:
  agentpal_called_subagent: false
  agentpal_called_external_agent: false
fallback:
  - prepare bounded handoff package
  - mark execution as not-run
  - require future host Runtime availability evidence before use
```

## Manual handoff summary

- Goal: review a Deep Conductor E2E package for no-code boundary and verification gaps.
- Can read: approved package, public protocols, returned host evidence.
- Cannot read: private memory, secrets, peer drafts, unrelated project files.
- Required output: verdict, checked evidence, missing evidence, boundary risks, repairs.

## Failure Modes

- claiming the subagent was started;
- probing host tools outside the package;
- reporting unavailable as pass;
- treating this example as proof that every host Runtime can call external Agents.
