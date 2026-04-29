# Synthetic CLI Examples

[Case-study home](../README.md) | [Main case study](../PUBLIC_CASE_STUDY_DRAFT.md) | [How I AI](../AI_ASSISTED_WORKFLOW.md) | [Artifact index](../PUBLIC_ARTIFACT_INDEX.md)

## Synthetic sample disclaimer

> Public-safe composite example: This sample was created for public documentation. It is not copied from production data, private logs, personal records, chat transcripts, or operational systems. Details are sanitized: rewritten to remove private details while preserving the technical pattern.

## Purpose

These examples show a public-safe command-line shape for the debugging and observability workflow. Commands and outputs are illustrative, synthetic, and non-executable. They do not represent real tools, real files, real runtime records, or real operational systems.

The examples refer to the same bounded packet shape shown in the [Synthetic evidence packet](evidence-packet-shape.json). The current public sample is synthetic; a real runtime packet could be published later only after separate privacy and security review.

## Example 1: exact-window investigation request

Command shape or pseudo-command:

```bash
observability-demo investigate --scenario synthetic-actuator-mismatch --window 2026-03-18T14:20:00Z..2026-03-18T14:35:00Z
```

Synthetic output excerpt:

```text
sample_type: synthetic_exact_window_investigation
window: 2026-03-18T14:20:00Z..2026-03-18T14:35:00Z
operator_question: Why did the primary actuator change state while expected intent remained hold?
packet_status: created
pipeline_health: degraded_but_usable
```

What it demonstrates:

The investigation starts from a bounded operator question and an exact window before explanation begins.

What it does not prove:

This does not prove a real CLI exists, that a runtime system was queried, or that any production data was inspected.

## Example 2: evidence packet preview

Command shape or pseudo-command:

```bash
observability-demo packet preview --packet synthetic-packet.json --fields intent,state,sources,gaps
```

Synthetic output excerpt:

```text
expected_intent.state: hold
observed_state.transition: hold -> active
observed_state.transition_time: 2026-03-18T14:27:12Z
evidence_sources.complete: intent_evaluator_summary, actuator_state_history
evidence_sources.partial: guard_evaluator_summary
evidence_gaps.count: 2
```

What it demonstrates:

The packet keeps expected intent, observed state, source coverage, and gaps visible before verdict or explanation.

What it does not prove:

This does not prove source coverage in a real deployment, real field names, or a complete evidence model.

## Example 3: detector/verdict/explanation summary

Command shape or pseudo-command:

```bash
observability-demo explain --packet synthetic-packet.json --format summary
```

Synthetic output excerpt:

```text
detector_events:
  - expected_vs_observed_mismatch: medium
  - external_input_possible: low
  - guard_context_incomplete: low

verdict:
  classification: unexpected_state_change_with_external_input_possible
  confidence: medium

explanation:
  The actuator changed to active while expected intent remained hold.
  A nearby synthetic external input marker may explain the divergence.
  Partial guard evidence prevents a final conclusion.
```

What it demonstrates:

Detector events, verdict classification, and explanation are related but separate layers.

What it does not prove:

This does not prove model accuracy, incident causality, or end-to-end production behavior.

## Example 4: pipeline-health distinction

Command shape or pseudo-command:

```bash
observability-demo health --packet synthetic-packet.json --show-domain-status
```

Synthetic output excerpt:

```text
pipeline_health.status: degraded_but_usable
pipeline_health.warning: guard evaluator coverage is partial near the transition
domain_verdict.severity: medium
domain_verdict.requires_human_review: true
health_note: pipeline health describes investigation completeness, not whether a domain issue exists
```

What it demonstrates:

Pipeline health is a separate signal from domain severity. A result can identify a likely issue while still showing incomplete evidence coverage.

What it does not prove:

This does not prove reliability, uptime, test pass rates, or complete pipeline coverage.

## Example 5: operator response

Command shape or pseudo-command:

```bash
observability-demo respond --packet synthetic-packet.json --audience operator
```

Synthetic output excerpt:

```text
short_answer:
  Expected intent stayed hold, but observed actuator state changed to active during the exact window.

confidence:
  Medium, because intent and observed-state evidence are complete, while guard coverage is partial.

next_checks:
  - Review the bounded external input summary for the transition minute.
  - Re-run the packet when complete guard evidence is available.
  - Compare the command surface against observed state for the same exact window.

ai_boundary:
  This response explains evidence only. It does not actuate or mutate control state.
```

What it demonstrates:

The operator response converts structured evidence into a reviewable explanation with confidence, gaps, next checks, and an explicit AI boundary.

What it does not prove:

This does not prove that an operator should take a specific control action, that the AI has authority to act, or that the sample came from a real system.

Previous: [Operator response](operator-response.md) | Packet: [Synthetic evidence packet](evidence-packet-shape.json) | Next: [Artifact index](../PUBLIC_ARTIFACT_INDEX.md)
