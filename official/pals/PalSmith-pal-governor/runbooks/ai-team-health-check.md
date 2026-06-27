# AI Team Health Check Runbook

Use this runbook after designing or creating an AI team.

## Inputs

- team goal;
- team asset path;
- member Pal paths;
- current contacts and registry evidence when existing Pals are reused;
- runtime evidence;
- privacy and publication boundary.

## Checks

1. Team purpose and success criteria are clear.
2. The Main Pal / leader / Conductor role is named and bounded.
3. Mira remains the default entry Pal unless the user and current registry support a different entry.
4. Each member Pal has a job, non-job, target user, and first usage example.
5. Members are described as candidate capability holders, not permanent route targets.
6. Team collaboration rules define context sharing, escalation, review, and stopping conditions.
7. Responsibility overlap is named and either accepted or repaired.
8. Team-level examples show realistic task flow.
9. Team evals test missing owner, duplicate owner, unsafe sharing, weak handoff, and bad publish claims.
10. Private or internal-only source material does not leak into public team files.
11. No Deep Conductor or multi-agent execution behavior is presented as current runtime behavior.
12. Registration and contacts changes are recommendations only unless handled by a separate confirmed package.

## Risk Flags

- missing leader or entry boundary;
- fixed route claim;
- duplicate responsibility;
- member Pal is an empty shell;
- team examples skip privacy boundaries;
- team publish status lacks evidence;
- execution capability is attributed to the Pal layer instead of the runtime.

## Output

Use `templates/health-check-report.md` for the team and `templates/repair-package.md` for blocking issues.
