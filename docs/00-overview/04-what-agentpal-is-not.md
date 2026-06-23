# What AgentPal Is Not

AgentPal v0.1.0-rc.1 has a strict release boundary. This page states the non-goals clearly so GitHub readers do not mistake future design material for current runtime behavior.

## AgentPal Is Not

- an Agent runtime
- a multi-agent runtime
- an execution layer
- a desktop app
- a web app
- a hosted service
- a marketplace
- an automatic installer
- a daemon, scanner, or validator
- a finished external Agent orchestration platform

## Not Active In v0.1.0-rc.1

- Deep Conductor as an active feature
- Subagent Mode
- parallel child workflows
- external Agent orchestration
- automatic runtime-wide scanning
- automatic project takeover

## Important Language Boundary

- A Pal is not an Agent.
- `/pal Name` does not start a separate agent process.
- Simple Pal Mode is the current active path.
- Future design documents must stay labeled as future or not active in `v0.1.0-rc.1`.

## Related

- [Current Status](01-current-status.md)
- [AgentPal Vs Agent Runtime](03-agentpal-vs-agent-runtime.md)
- [Release Candidate Summary](05-release-candidate-summary.md)
