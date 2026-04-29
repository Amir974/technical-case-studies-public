# The Automation System Behind the Debugging Layer

[Case-study home](README.md) | [Main case study](PUBLIC_CASE_STUDY_DRAFT.md) | [How I AI](AI_ASSISTED_WORKFLOW.md) | [Canonical context](CANONICAL_CONTEXT_MODEL.md) | [Artifact index](PUBLIC_ARTIFACT_INDEX.md)

## Status

This page gives context for the automation system behind the AI-assisted debugging layer.

I keep operational details out of the public version. The goal here is to show the architecture pattern without exposing private details.

## Why this page exists

The debugging layer makes more sense when the underlying system is not treated as a toy example.

The project behind it is a real, multi-layered personal automation system with production-style operating constraints and enough moving parts to create genuine ambiguity: staged decisions, guard behavior, observed state, retries, reconciles, external inputs, and operator-facing questions.

This page gives enough safe context to explain why current-state debugging was not enough.

The automation/control model itself could become a deeper case study later; here I only include enough context to explain the debugging layer.

## The short version (TL;DR)

At the center is a Home Assistant-based automation system. Around it, I built additional observability, metrics, and AI-assisted investigation workflows.

The automation system is event-driven. It reacts to changing conditions, evaluates whether action is allowed, decides what the effective intent should be, and then routes or wraps actuation through safer control points.

That shape creates useful observability opportunities, but it also creates ambiguity. A final observed state does not explain which layer made the decision, whether the decision was expected, whether a guard intervened, or whether the evidence is incomplete.

The AI-assisted debugging layer sits beside this system. It does not replace the controller. It helps explain what happened by collecting bounded evidence and turning it into a reviewable response.

## Runtime environment

The environment is split across:

- A compact automation host.
- A separate higher-capacity AI/observability machine.
- Supporting VMs for metrics, runtime services, and analysis workflows.

This separation keeps control automation apart from heavier analysis and AI-assisted work. It also lets observability, indexing, evidence handling, and reasoning workflows grow without overloading the control host.

No public page should include internal hostnames, IPs, machine identifiers, exact paths, remote access details, tunnel details, security configuration, or device names.

## Automation/control model, high level

The control model is staged rather than one big rule.

This staged model is not a native Home Assistant control model. [Home Assistant](https://www.home-assistant.io/) provides the automation platform, integrations, scripts, templates, entity model, and execution surface. The layered control logic described here was built on top of those primitives using automations, scripts, templates, and supporting code.

That staged model exists because the system should not jump directly from "condition changed" to "actuator changed." It first needs to decide whether the relevant profile or scope is active, whether demand exists, whether a guard blocks action, whether escalation or routing is needed, and whether observed state matches effective intent.

At a high level, the system has concepts such as:

- Eligibility: whether a target is allowed to participate.
- Demand: whether current conditions suggest action.
- Effective intent: what the controller appears to want after inputs and constraints are considered.
- Guard behavior: checks that can approve, defer, suppress, or block action.
- Actuation wrapper: the safer boundary around sending or routing an action.
- Retry/reconcile behavior: mechanisms for dealing with mismatch, delay, or uncertainty.
- Escalation or routing decisions: deciding whether a condition needs attention or should remain local.

The details are generic on purpose. The architecture pattern is what matters here.

## Where decisions can be observed

Each layer creates a place where evidence can be captured:

- Input conditions.
- Eligibility and demand signals.
- Effective intent.
- Guard result.
- Requested action.
- Observed state.
- External or out-of-band influence.
- Retry, reconcile, or escalation signals.
- Operator-facing explanation.

Good observability does not require exposing raw logs publicly. It requires preserving enough structure to reconstruct why a decision was likely made.

The investigation layer can draw from high-level sources such as:

- Observability decision records.
- Metrics in VictoriaMetrics.
- Operational database/history where appropriate.
- Runtime status and pipeline-health outputs.
- Curated source-of-truth and playbook documents.

Those inputs are described here only at the category level. This page does not expose queries, schema names, paths, hostnames, or operational records.

## Why this creates debugging ambiguity

The same observed state can have several meanings.

It might be the expected result of the controller. It might be a valid guard outcome. It might reflect an external input. It might be stale. It might be a mismatch. Or the evidence might be too incomplete to decide.

That is why debugging from current state alone breaks down. The system needs expected-vs-actual reasoning: compare what the system appeared to intend with what was actually observed, then check whether the evidence is complete enough to trust the answer.

## How this connects to the AI-assisted debugging layer

The debugging layer turns this ambiguity into a bounded investigation:

1. Start with an operator question.
2. Resolve the question to an exact time window.
3. Build an evidence packet from the relevant layers.
4. Identify detector events such as expected-vs-observed mismatch or incomplete context.
5. Produce a verdict with confidence and gaps.
6. Use AI to explain the bounded packet in plain language.
7. Keep the human/operator responsible for decisions.

AI is useful here because the packet gives it structure. It is not reading unlimited history or acting on the system directly.

## What stays private

To keep the public version useful but safe, I leave out operational details such as:

- Raw source code.
- Raw runtime records, logs, traces, or transcripts.
- Internal hostnames, IPs, paths, internal machine identifiers, or remote access details.
- Security configuration.
- Real entity identifiers, device names, room details, routines, or household-sensitive information.
- Exact operational timelines or incident records.
- Public claims of production completeness, reliability, or quantified impact.

The public pages use sanitized and composite examples: rewritten to remove private details while preserving the technical pattern.

## Related pages

- [Main case study](PUBLIC_CASE_STUDY_DRAFT.md)
- [How I AI](AI_ASSISTED_WORKFLOW.md)
- [Canonical context model](CANONICAL_CONTEXT_MODEL.md)
- [Exact-window synthetic scenario](synthetic-examples/exact-window-scenario.md)
- [Synthetic operator response](synthetic-examples/operator-response.md)
- [Artifact index](PUBLIC_ARTIFACT_INDEX.md)
