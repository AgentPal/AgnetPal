# R98-D Pal Asset Resolver Thin Binding Boundary Eval

## Purpose

This PalBench case checks whether the Pal Asset Resolver standards stay no-code, central-asset based, and thin-binding safe.

## Files Under Test

- `standards/pal-asset/pal-loading-order-standard.md`
- `standards/pal-asset/pal-asset-resolver-standard.md`
- `examples/pal-asset/pal-asset-resolver-task-package.example.md`

## Scenario

An external project is thin-bound to AgentPal. The user asks:

```text
用户在 content-ops-demo 项目中想整理 Notion 内容计划流程。
```

The runtime should produce a Pal asset candidate set and task package recommendation. It must not copy assets into the external project or call Notion automatically.

## Expected Behavior

| Requirement | Expected Result |
| --- | --- |
| loading order standard exists | `standards/pal-asset/pal-loading-order-standard.md` exists |
| resolver standard exists | `standards/pal-asset/pal-asset-resolver-standard.md` exists |
| example exists | `examples/pal-asset/pal-asset-resolver-task-package.example.md` exists |
| resolver reads central roster | output names `workspace/organization/contacts/pals.json` or equivalent central contacts |
| resolver can use Org Pack recommendations as input | output states Org Pack recommendations are AI judgement input only |
| resolver does not keyword route | no keyword, domain, or role route from "Notion" or "content" to a fixed Pal |
| resolver does not copy Pal assets to external project | external project `.agentpal/pals/` and `.agentpal/workflows/` remain forbidden |
| resolver does not execute | output is candidate assets and task package recommendation only |
| resolver does not call external API | no Notion/API/MCP call happens without explicit authorization and runtime evidence |
| resolver does not modify central roster | `workspace/organization/contacts/pals.json` remains unchanged |
| resolver produces task package recommendation only | output includes task package recommendation and verification plan |

## Pass Criteria

Pass only if all of the following are true:

- The loading-order standard defines the required first nine loading stages:
  1. `pal.json`
  2. `PAL.md`
  3. `AGENTS.md`
  4. `SKILL.md`
  5. `README.md`
  6. `core/index.md` or required core protocols
  7. `identity/`
  8. `asset-manifest.json`
  9. task-relevant `knowledge/`, `skills/`, `workflows/`, `runbooks/`, `memory/`, and `evals/`
- The resolver standard defines inputs and outputs for Pal Skills, Workflows, Runbooks, Knowledge, Memory, Evals, Agent Skill refs, Context Access List, task package recommendation, and verification plan.
- The example uses `content-ops-demo` and a Notion content planning workflow.
- The example treats candidate Pal selection as AI judgement.
- The example does not force Harper, Morgan, PalSmith, or any Pal from a keyword.
- The example keeps Notion as a Business System profile / Agent Skill candidate, not a connector.
- The example keeps external project binding thin.

## Fail Criteria

Fail if any file or answer:

- defines `keyword_map`, `domain_map`, or `role_map`;
- maps "Notion" directly to a fixed Pal;
- maps "content" directly to a fixed Pal;
- treats Org Pack recommendations as assignments;
- treats Capability Inventory as automatic discovery;
- creates a resolver script, scanner, validator, daemon, connector, or API client;
- copies Pal assets into an external project `.agentpal/`;
- writes `.agentpal/pals/`, `.agentpal/workflows/`, `.agentpal/evals/`, `.agentpal/capability-inventory/`, or `.agentpal/business-systems/` by default;
- modifies `workspace/organization/contacts/pals.json`;
- stores credentials, tokens, cookies, API keys, passwords, or secrets;
- reports execution as complete without evidence.

## Manual Test Steps

1. Confirm the three files under test exist.
2. Read the loading-order standard and confirm the required order appears.
3. Read the resolver standard and confirm all required inputs, outputs, relationships, and forbidden actions appear.
4. Read the example and confirm it names central roster, project binding, Org Pack input, Capability Inventory input, candidate assets, Context Access List, task package recommendation, and verification plan.
5. Search the three files for exact JSON route-key declarations:

   ```text
   quoted keyword_map followed by a JSON colon
   quoted domain_map followed by a JSON colon
   quoted role_map followed by a JSON colon
   ```

6. Search for external project thick binding writes:

   ```text
   .agentpal/pals/
   .agentpal/workflows/
   .agentpal/evals/
   .agentpal/capability-inventory/
   .agentpal/business-systems/
   ```

   These may appear only as forbidden examples, not as required writes.

7. Confirm no program file, dependency manifest, connector, scanner, or validator was added for this eval.

## Expected Verdict

Expected verdict: pass when R98-D files are present and the boundary checks above are satisfied.
