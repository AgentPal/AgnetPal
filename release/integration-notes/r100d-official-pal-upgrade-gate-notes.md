# R100-D Official Pal Upgrade Gate Notes

Date: 2026-06-28

## Purpose

These notes define the safe order for future official Pal v0.5 metadata or `asset-manifest.json` upgrade rounds.

R100-D itself does not upgrade official Pals, does not generate real manifests, and does not modify the central roster.

## Required Upgrade Order

1. Run the R100-D compatibility gate before changes.
2. Apply one Pal or a small batch.
3. Rerun the R100-D compatibility gate.
4. Rerun selected R95 tests.
5. Only then commit.
6. Never push, tag, or create a release in normal development rounds.

## Gate Before Changes

Before editing any official Pal metadata, collect baseline evidence:

- `git status --short --branch`
- central roster parse and count
- official Pal directory count
- all official Pal `pal.json` parse
- root entry reachability for all official Pals
- current thin binding template parse
- exact route-map declaration check
- connector / scanner / credential check
- current R95 reference status

Use:

- `evals/palbench/pal-asset/r100d-pal-metadata-upgrade-compatibility-gate.md`
- `evals/palbench/pal-asset/r100d-pal-manifest-backward-compatibility-cases.md`

## Apply One Pal Or Small Batch

Keep batches small enough that failures can be attributed.

Recommended sequence:

1. one Pal first;
2. review `pal.json` metadata compatibility;
3. add or update `asset-manifest.json` only after schema is stable;
4. check root entries and fallback loading;
5. avoid touching unrelated Pal assets.

Do not batch all official Pals unless a previous one-Pal pilot has passed this gate.

## Rerun Gate After Changes

After each Pal or small batch:

- rerun central roster checks;
- rerun per-Pal loadability checks;
- verify manifest fallback behavior;
- verify no external project asset copy;
- verify no connector, scanner, auto execution, keyword routing, or credential storage;
- verify changed files match the allowed scope.

## Rerun Selected R95 Tests

At minimum rerun these R95 groups after official Pal metadata changes:

- Group 2: External project thin binding
- Group 3: Central Pal roster
- Group 4: No keyword routing
- Group 5: Official Pal integrity
- Group 10: Public safety / internal leak

Rerun Group 9 if public docs, README, navigation, or user reading paths changed.

## Commit Rule

Only commit after:

- R100-D gate passes;
- selected R95 groups pass or have explicit accepted `not-run` status;
- changed file scope is reviewed;
- no official Pal outside the intended small batch changed;
- no central roster change occurred unless a separate approved registration task allowed it.

Suggested future commit messages:

- `docs: add v0.5 metadata for <pal-id>`
- `docs: add asset manifest for <pal-id>`
- `test: validate official pal metadata upgrade batch`

## Forbidden In Normal Development Rounds

Do not:

- `git push`
- `git pull`
- `git fetch`
- create or modify tags
- create or modify GitHub Releases
- perform release/tag migration
- overwrite local work from remote
- modify all official Pals in an unbounded batch
- modify `workspace/organization/contacts/pals.json` without a separate approved registration task
- copy Pal assets into external projects
- create project-local `.agentpal/pals`
- create project-local `.agentpal/skills`
- introduce keyword routing
- introduce connector / scanner / validator / daemon / marketplace / auto execution behavior
- store credentials, tokens, cookies, passwords, API keys, or secrets

## Failure Handling

If the gate fails:

1. stop the metadata upgrade;
2. identify affected Pal or shared boundary;
3. do not hide the issue by editing central roster;
4. repair the smallest affected file set;
5. rerun the gate;
6. record `not-run`, `blocked`, or `missing` explicitly if evidence is unavailable.

## Integration Reminder

R100-D is a compatibility gate, not the upgrade itself. Future upgrade threads should reference this note before changing `official/pals/**`.
