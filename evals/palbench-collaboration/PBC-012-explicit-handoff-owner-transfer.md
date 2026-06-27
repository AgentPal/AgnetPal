# PBC-012 Explicit Handoff Owner Transfer

## User Input

```text
Mira, hand this release verification task to Quinn.
```

## Expected Context Packet

- `to_pal_candidate: Quinn`
- `mode: handoff` or `owner_transfer`
- `explicit_user_call.type: "handoff"`
- `owner_status: owner_candidate_after_transfer`
- `return_to: user`
- `final_report_required: true`

## Expected Workflow

Mira states the transfer reason and packet boundary. Quinn applies core gates, accepts or limits owner-candidate status, then performs verification.

## Expected Output

Quinn starts with owner acceptance or limitation, then provides verification decision and evidence gaps.

## Failure Modes

- Mira continues writing the verification body.
- Quinn accepts without core gates.
- Handoff becomes a permanent rule for release tasks.

## Scoring Rubric

- 0: no explicit transfer boundary or fixed route appears.
- 1: transfer is present but packet or gates are weak.
- 2: handoff packet and Quinn acceptance are clear.
