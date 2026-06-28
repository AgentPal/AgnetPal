# R118 Pal Metadata Pause And Org Pack Return Decision

Date: 2026-06-28

## Decision

```text
pal_metadata_pilot_status: observation_passed
pause_full_pal_metadata_rollout: true
do_not_start_9_pal_manifest_rollout_now: true
recommended_next_focus: org_pack_and_fde_delivery_pack
```

## Rationale

PalSmith's official manifest survived post-writeback observation:

- manifest parses;
- official manifest count remains `1`;
- only PalSmith has an official manifest;
- central roster remains unchanged;
- official Pal `pal.json` files remain unchanged;
- no route maps, credential leak, connector behavior, scanner behavior, marketplace behavior, or external project thick binding was introduced;
- PalSmith keeps `asset_manifest_required=false` and `directory_convention_fallback=true`.

The pilot has enough evidence to prove the v0.5 metadata / manifest model for one carefully governed Pal. Continuing immediately into Mira metadata or a full 9 Pal manifest rollout would broaden risk without improving the current v0.5 Org Pack/FDE delivery path.

## Explicit Non-start Decisions

- Do not start Mira metadata update now.
- Do not start a full 9 official Pal manifest rollout now.
- Do not modify central contacts.
- Do not make manifests runtime-required.
- Do not copy official Pal manifests into external project `.agentpal/`.
- Do not create `.agentpal/pals`, `.agentpal/asset-manifest`, `.agentpal/skills`, `.agentpal/workflows`, or `.agentpal/evals` in external projects by default.
- Do not create a marketplace, hub, connector, scanner, validator, installer, daemon, or auto-execution program.

## Preserved Pilot Evidence

PalSmith remains the single official pilot evidence case:

- `official/pals/PalSmith-pal-governor/pal.json`
- `official/pals/PalSmith-pal-governor/asset-manifest.json`
- R113 through R118 PalBench, validation, integration notes, and internal reports

## Restart Condition

A future metadata or manifest batch may restart only through an explicit batch gate that names:

- target Pal(s);
- reason the Org Pack/FDE mainline needs the metadata change;
- pre-change compatibility gate;
- post-change selected R95 surfaces;
- rollback plan;
- confirmation that central roster, `pal.json`, thin binding, no-keyword-routing, no-credential, and no-connector boundaries are preserved.

## Conclusion

Pause full Pal metadata / manifest rollout now and return to Org Pack / FDE delivery pack work.
