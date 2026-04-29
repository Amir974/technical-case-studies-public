# Exact-Window Synthetic Scenario

[Case-study home](../README.md) | [Main case study](../PUBLIC_CASE_STUDY_DRAFT.md) | [How I AI](../AI_ASSISTED_WORKFLOW.md) | [Canonical context](../CANONICAL_CONTEXT_MODEL.md) | [Artifact index](../PUBLIC_ARTIFACT_INDEX.md)

## Synthetic sample disclaimer

> Public-safe composite example: This sample was created for public documentation. It is not copied from production data, private logs, personal records, chat transcripts, or operational systems. Details are sanitized: rewritten to remove private details while preserving the technical pattern.

## Scenario purpose

This scenario demonstrates how an AI-assisted debugging workflow can turn an ambiguous event-driven control question into a bounded, reviewable investigation packet.

The example focuses on evidence structure and operator explanation. It does not describe a real deployment, a real incident, or a real control rule.

## Operator question

Why did the primary actuator change from `hold` to `active` during the requested window when the expected intent appeared to remain `hold`?

## Exact window

Requested investigation window:

- Start: `2026-03-18T14:20:00Z`
- End: `2026-03-18T14:35:00Z`
- Window type: operator-specified exact interval

## System context, generic

The synthetic system is an event-driven control platform with these generic components:

- An intent evaluator that calculates the expected control intent.
- A guard evaluator that can approve, defer, or veto actuator changes.
- An actuator command surface that records requested state changes.
- An external input surface that can influence observed state outside the main controller path.
- An observability pipeline that gathers bounded evidence, detector events, verdicts, explanations, and pipeline-health signals.

The AI layer receives structured evidence only. It investigates and explains the observed behavior, but it does not send commands, mutate controller state, or override operator authority.

## Synthetic packet sample

The scenario is represented as a bounded evidence packet. The packet is not raw history and it is not a real runtime export. It is a public-safe packet sample that shows the kind of structured input the AI explanation layer receives.

See: [Synthetic evidence packet](evidence-packet-shape.json)

At a high level, the packet includes:

- Operator question.
- Exact investigation window.
- Evidence-source coverage.
- Expected intent.
- Observed state.
- Detector events.
- Verdict classification.
- Explanation inputs.
- Pipeline-health status.
- Confidence.
- Evidence gaps.
- Recommended next checks.
- Explicit excluded actions.

To analyze this kind of packet correctly, the AI also needs current context about the system's concepts, boundaries, and interpretation rules. In the private workflow, that comes from reviewed source-of-truth notes, contracts, playbooks, and validation guidance. In this public example, those are represented only at a high level.

The current public sample is synthetic. A real runtime packet could be published later only after separate privacy and security review.

## What the packet should answer

The evidence packet should answer:

- Whether the expected intent changed during the exact window.
- Whether the observed actuator state changed during the same window.
- Whether a detector identified a mismatch between expected intent and observed state.
- Whether guard behavior explains the observed state.
- Whether an external input or missing evidence could explain the state change.
- Whether the pipeline was healthy enough to support a conclusion.
- What confidence level and evidence gaps should be shown to the operator.

## Why this is useful for the case study

This scenario shows the case study's core workflow in public-safe form:

1. Start with a precise operator question.
2. Resolve the question to an exact time window.
3. Gather only bounded, relevant evidence.
4. Normalize findings into detector events.
5. Produce a verdict with confidence and gaps.
6. Generate an operator-readable explanation.
7. Keep AI on investigation and explanation paths, separate from control authority.

The value is not the domain-specific actuator behavior. The value is the evidence discipline: the system separates raw evidence, detector interpretation, verdict classification, explanation, and pipeline health.

## What this does not prove

This synthetic sample does not prove production completeness, runtime reliability, test coverage, adoption, time savings, or incident-resolution outcomes.

It also does not prove that an actuator should change state. The example only demonstrates the shape of a bounded investigation and a reviewable explanation generated from invented, sanitized evidence.

Next: [Synthetic evidence packet](evidence-packet-shape.json) | Then: [Operator response](operator-response.md)
