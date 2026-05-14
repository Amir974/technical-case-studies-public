# Synthetic Example: Control Workflow Review

Synthetic sample derived from workflow structure. No real environment details, device labels, location labels, entity identifiers, schedules, or operational records included.

This example shows a generic control-state review without claiming autonomous actuation.

## State

```text
Command: /explain

Control state:
Generic control mode is active.

Review state:
Awaiting human confirmation before any next step.
```

## Intent

```text
Intent:
Maintain the current target while respecting guard behavior and incomplete evidence.
```

## Guard

```text
Guard review:
The packet indicates that a guard condition may be limiting the next step. Source coverage is partial, so the guard explanation should remain tentative.
```

## AI Explanation

```text
AI explanation:
The workflow appears to be holding because the current packet does not contain enough evidence to confirm that the next step is allowed. The safest interpretation is to keep the state unchanged until the missing guard evidence is reviewed.
```

## Human Approval Boundary

```text
Human boundary:
AI can explain the packet and name the gap.
Runtime can record the reviewed state.
The human reviewer decides whether to approve, park, close, or investigate further.
```

## Next Check

```text
Next check:
Inspect the missing guard evidence before accepting the recommendation.
```

No action is taken by this example. It shows a review pattern, not an actuation flow.
