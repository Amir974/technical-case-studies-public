# Synthetic Example: Observability Investigation

Synthetic sample derived from real workflow structure. No real environment, control detail, raw operational evidence, or personal data included.

This example links conceptually to the already-published observability/debugging deep dive without duplicating it.

## Bounded Question

```text
Command: /investigate

Question:
Why did the workflow choose an unexpected path during the review window?
```

## Evidence

```text
Evidence included:
- expected intent summary
- observed state summary
- relevant decision notes
- source coverage status
- packet completeness note
```

## Hypothesis

```text
AI hypothesis:
The most likely explanation is a mismatch between expected intent and observed state. The packet suggests the workflow followed a fallback path because one required signal was unavailable.
```

## Uncertainty

```text
Uncertainty:
- The packet does not include every guard signal.
- The explanation should be treated as a hypothesis, not a final determination.
- Confidence is limited by incomplete source coverage.
```

## Missing Signal

```text
Missing signal:
One relevant guard indicator is not present in the packet.
```

## Human Next Check

```text
Human next check:
Review the missing guard indicator and compare it with the decision notes before accepting the explanation.
```

## Boundary

The investigation provides a reviewable explanation. It does not take action, change state, or claim certainty beyond the packet.
