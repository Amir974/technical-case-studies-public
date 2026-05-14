# Synthetic Example: Helper CLI Flow

Synthetic sample derived from real workflow structure. No real account, company, contact, runtime, command, path, raw record, or personal data included.

These are synthetic command shapes that demonstrate the helper-layer pattern. They are not copied from private tooling.

This example supports the shared `ITEM-123` walkthrough. It shows helper and maintenance steps that prepare review material before Telegram or dashboard decisions. The flow supports review; it does not replace human judgment.

## 1. Dry-Run Source Scan

```bash
workflow scan --source messages --dry-run
```

Synthetic output:

```text
mode: dry-run
source: messages
candidate_items: synthetic summary available
would_create_or_update: review candidates only
state_changed: no
review_note: inspect candidates before importing or evaluating
```

What it solves: source-message intake should be inspectable before it changes the queue.

Where it fits: before a new review cycle or during maintenance.

State behavior: read-only in this synthetic example.

Reviewability benefit: the reviewer can see whether there is enough source coverage to justify creating or updating review items.

## 2. Reconcile Item State

```bash
workflow reconcile ITEM-123 --explain
```

Synthetic output:

```text
item: ITEM-123
stored_state: needs evaluation
source_state: updated summary available
reconciliation: compatible with existing item
ambiguity: ownership scope still missing
state_changed: no
next_step: validate packet before AI evaluation
```

What it solves: stored state and source material can drift, duplicate, or disagree.

Where it fits: after intake and before evaluation.

State behavior: explain-only in this synthetic example.

Reviewability benefit: reconciliation assumptions are visible before the packet becomes the AI handoff.

## 3. Validate Packet

```bash
workflow packet ITEM-123 --validate
```

Synthetic output:

```text
item: ITEM-123
packet_status: reviewable_with_gaps
scope: present
known_facts: present
missing_facts: ownership scope, timeline
source_coverage: partial
allowed_actions: approve, park, close
state_changed: no
recommendation: evaluate, but do not treat missing facts as resolved
```

What it solves: a packet should be checked before AI is asked to reason over it.

Where it fits: before `/evaluate ITEM-123` or dense dashboard evaluation review.

State behavior: read-only in this synthetic example.

Reviewability benefit: the model receives a bounded packet, and the reviewer can challenge recommendations that exceed the packet.

## 4. Inspect Audit Summary

```bash
workflow audit ITEM-123 --summary
```

Synthetic output:

```text
item: ITEM-123
prior_state: reviewed once
last_human_decision: parked pending missing facts
evaluation_history: one bounded evaluation available
state_changed: no
review_note: prior decision should be considered before approval
```

What it solves: prior decisions and review history should be easy to inspect without exposing raw operational records.

Where it fits: item detail review, dashboard review, or maintenance.

State behavior: read-only in this synthetic example.

Reviewability benefit: a reviewer can distinguish a new recommendation from prior human judgment.

## 5. Diagnose Missing Evidence

```bash
workflow diagnose --scope review-window
```

Synthetic output:

```text
scope: review-window
workflow_health: usable with gaps
common_blockers: missing ownership scope, partial source coverage
affected_items: ITEM-123 and related review candidates
state_changed: no
next_step: enrich missing facts or park until evidence is available
```

What it solves: some problems belong to workflow health, not item judgment.

Where it fits: when the queue looks stale, inconsistent, or under-explained.

State behavior: read-only in this synthetic example.

Reviewability benefit: diagnostics keep maintenance concerns separate from AI evaluation and final human decisions.

## Boundary

The helper flow prepares, validates, and diagnoses evidence. It does not approve `ITEM-123`, close it, contact anyone, publish anything, or turn an AI recommendation into action.

The human decision still happens through the review surfaces and explicit lifecycle choices such as `/approve ITEM-123`, `/park ITEM-123`, or `/close ITEM-123`.
