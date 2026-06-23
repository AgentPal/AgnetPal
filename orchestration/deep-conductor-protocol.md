# Deep Conductor Protocol

Deep Conductor is a future AgentPal orchestration design for complex work that needs topology planning, context separation, independent verification, and routing memory.

It is not active task handling in AgentPal v0.1.0-rc.1.

## Purpose

Deep Conductor studies how a Main Pal can coordinate existing Agent runtimes better without competing with foundation models.

The design separates:

- task judgement
- Capability Inventory lookup
- workflow topology selection
- Context Access Lists
- intra-workflow Pal isolation
- independent review before synthesis
- shared memory across workflows
- routing reward memory from real outcomes

## When It May Be Considered Later

Future Deep Conductor may be useful when:

- the task has multiple independent workstreams
- different Pals, Skills, runtimes, or model profiles must be compared
- false completion risk is high
- verification must be separated from creation
- context leakage or context bloat is a major risk
- previous routing outcomes should influence the next plan

## Required Design Artifacts

A Deep Conductor workflow should define:

- goal and acceptance criteria
- workflow topology
- owner candidate
- verifier candidate when needed
- Context Access List per recipient
- output contract per step
- content read budget per step
- isolation boundary
- summary stage
- routing decision record

## Not Active In v0.1

AgentPal v0.1 remains Simple Pal Mode only. Deep Conductor docs are design foundation and evaluation material. They do not authorize automatic parallel workflows, child-agent calls, external Agent runtime calls, or group chat.

