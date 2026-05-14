# Synthetic Example: Dashboard Review Flow

Synthetic textual wireframe. No real UI screenshot, source data, account data, or personal data included.

This is the dense-review stage of the shared `ITEM-123` walkthrough. It follows [telegram-command-flow.md](telegram-command-flow.md) and uses the packet shape in [evidence-packet-shape.json](evidence-packet-shape.json).

## Queue Review

```text
External Signal Review

Filters:
[Needs evaluation] [Missing facts] [Ready for decision] [Parked] [Closed]

Table:
| Item | Assessment | Source coverage | Lifecycle state | Missing facts | Decision prep |
| ---- | ---------- | --------------- | --------------- | ------------- | ------------- |
| ITEM-123 | Potential fit | partial | needs evaluation | scope, timeline | evaluate |
| ITEM-124 | Weak fit | partial | missing facts | summary | park or close |
| ITEM-125 | Stronger fit | complete | ready for decision | none listed | approve or close |
```

## Summary / Detail Split

```text
Selected item: ITEM-123

Summary:
- Assessment: potential fit
- Source coverage: partial
- Lifecycle state: needs evaluation
- History availability: prior state available

Known facts:
- Category appears relevant.
- Public summary is present.
- Prior review state is available.

Missing facts:
- Ownership scope
- Timeline

Decision prep:
- Ask AI to evaluate the current packet.
- Park if missing facts are required.
- Close if the item no longer matches the review goal.
```

## Evidence Inspection

```text
Evidence panel:
- Request: review ITEM-123
- Workflow: external signal review
- Evidence gatherers: source messages, stored item state, prior decisions, manual assist note
- Source coverage: partial
- Known facts: category, summary, prior state
- Missing facts: ownership scope, timeline
- AI task: evaluate relevance and name gaps
- Allowed actions: approve, park, close
```

## Why This Belongs In A Dashboard

The dashboard supports review tasks that are awkward in chat:

- compare multiple items
- scan missing facts
- inspect lifecycle state
- check history availability
- move between summary and detail
- prepare decisions without losing context

Telegram can still execute the final command. The dashboard makes the decision better prepared.
