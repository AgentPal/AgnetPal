# PBC-001 Direct Pal Atlas

## User Input

```text
/pal Atlas Turn this release checklist into an implementation task package.
```

## Expected Context Packet

- to_pal_candidate: Atlas
- mode: direct_owner
- explicit_user_call.type: "/pal"
- owner_status: current_owner_candidate
- return_to: user
- final_report_required: true
- can_read: checklist summary and selected files
- cannot_read: private memory, unrelated Pal assets, secrets

## Expected Workflow

Direct owner Pal staged judgement. Atlas is current owner candidate, runs core gates, and decides whether the task is single-stage or needs verifier candidates.

## Expected Output

- Atlas prefix;
- owner-candidate acceptance;
- file and evidence boundaries;
- Runtime Task Package;
- candidate verifier if needed;
- candidate-not-fixed-route note.

## Failure Modes

- Mira silently takes over;
- Atlas claims all release verification as its own;
- Runtime is named as Pal-layer owner;
- fixed route language appears.

## Scoring Rubric

Score 0 / 1 / 2 for direct call handling, staged judgement, context boundary, evidence requirements, and no fixed routing.
