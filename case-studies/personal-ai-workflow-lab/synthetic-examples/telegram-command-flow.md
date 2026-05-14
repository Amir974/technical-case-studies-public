# Synthetic Example: Telegram Command Flow

Synthetic sample derived from real workflow structure. No real account, company, contact, runtime, or personal data included.

This is the fast-control stage of the shared `ITEM-123` walkthrough. Continue with [dashboard-review-flow.md](dashboard-review-flow.md), [evidence-packet-shape.json](evidence-packet-shape.json), and [external-signal-review.md](external-signal-review.md).

## Status

```text
Command: /status

Workflow status:
- External signal review: 3 items need attention
- Observability investigation: 1 open question
- Control workflow review: no pending decision

Next useful command:
/review
```

## Queue

```text
Command: /review

Review queue:
1. ITEM-123 - needs evaluation
2. ITEM-124 - missing facts
3. ITEM-125 - ready for decision

Commands:
/details ITEM-123
/evaluate ITEM-123
```

## Detail

```text
Command: /details ITEM-123

ITEM-123
Status: needs evaluation
Known: category, summary, prior state
Missing: ownership scope, timeline

Suggested:
/evaluate ITEM-123
```

## Decision

```text
Command: /evaluate ITEM-123

Evaluation:
Potentially relevant, but missing facts make approval uncertain.

Next actions:
/approve ITEM-123
/park ITEM-123
/close ITEM-123
```

```text
Command: /park ITEM-123

Recorded:
ITEM-123 is parked.

Reason:
Missing facts need review before approval.
```

## Why This Fits Chat

The messages stay short. Each response has one job: summarize status, show the next queue, inspect one item, request evaluation, or record a decision.

When the review needs comparison across many items, the dashboard is the better surface.
