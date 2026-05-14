# Synthetic Example: External Signal Review

Synthetic sample derived from real workflow structure. No real account, company, contact, runtime, or personal data included.

This is one stage of the shared `ITEM-123` walkthrough. It connects the fast command flow in [telegram-command-flow.md](telegram-command-flow.md), the dense review flow in [dashboard-review-flow.md](dashboard-review-flow.md), and the synthetic packet in [evidence-packet-shape.json](evidence-packet-shape.json).

## Incoming Item Triage

```text
Command: /review

Queue summary:
- ITEM-123 - needs evaluation
- ITEM-124 - missing core facts
- ITEM-125 - ready for human decision

Suggested next command:
/details ITEM-123
```

## Item Details

```text
Command: /details ITEM-123

Item: ITEM-123
Status: needs evaluation
Workflow: external signal review

Facts known:
- Category appears relevant to the current review goal.
- The item has a concise public summary.
- Prior state is available.
- Source-message intake found enough context to create the item.
- A manual assist note is present because one source was not reliable enough for full automation.

Facts missing:
- Ownership scope is unclear.
- Timeline is unclear.
- Decision urgency is unknown.

Available actions:
- /evaluate ITEM-123
- /approve ITEM-123
- /park ITEM-123
- /close ITEM-123
```

## AI Evaluation

```text
Command: /evaluate ITEM-123

AI evaluation:
ITEM-123 appears potentially relevant, but approval would be premature because the packet lacks ownership scope and timeline. The strongest next step is to clarify the missing facts or park the item until the facts are available.

Risks and gaps:
- Fit is plausible but not proven.
- The item may be low priority if the missing timeline is not near-term.
- The packet does not include enough evidence to recommend approval.
- Manual assist evidence should be reviewed before treating the item as ready.

Allowed next actions:
- /approve ITEM-123 only if the human reviewer accepts the uncertainty.
- /park ITEM-123 if missing facts are needed.
- /close ITEM-123 if the item is no longer relevant.
```

## Lifecycle Decision

```text
Command: /park ITEM-123

Decision recorded:
ITEM-123 moved from needs evaluation to parked.

Reason:
Missing ownership scope and timeline.

Audit/state note:
Human reviewer made the lifecycle decision. AI evaluation remains advisory.

Next visible state:
ITEM-123 will remain parked until new facts are added or a reviewer closes it.
```

Alternative decisions:

```text
/approve ITEM-123
/close ITEM-123
```
