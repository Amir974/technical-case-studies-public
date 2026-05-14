# Building an AI-Assisted Debugging Layer for Complex Automation

## Overview

The public-facing material explains the technical pattern without exposing private systems. Synthetic and composite examples show the workflow shape; private summaries and support docs stay out of the main reading path.

![Debugging-layer architecture showing an event-driven automation system feeding observability records and metrics into an evidence packet builder, AI-assisted detector, verdict, and explanation layers, and human operator review, with pipeline health and a non-actuating AI boundary.](assets/architecture-overview.png)

Debugging-layer architecture: the underlying automation system produces events and evidence, which are shaped into bounded packets before AI-assisted reasoning, explanation, and human review.

The diagram shows the debugging layer, not the full automation/control system; the underlying system is represented only as the source of events and evidence.

## Where This Fits In The Series

This is the observability and diagnosis layer of the series. It shows how a complex automation system can produce bounded evidence for AI-assisted explanation while keeping actuation and final decisions outside the AI boundary.

In the broader pattern, this case study proves the diagnostic side: exact-window evidence, visible gaps, confidence-aware explanation, and human operator review.

## Start here

Start with [Building an AI-Assisted Debugging Layer for Complex Automation](PUBLIC_CASE_STUDY_DRAFT.md).

That page is the main reference/blog-style case study. It explains why current-state debugging was not enough, how I moved toward exact-window evidence packets, where AI fits, where it does not, and how curated context keeps future AI-assisted work grounded.

For more background, read [The Automation System Behind the Debugging Layer](SYSTEM_CONTEXT.md), [How I AI](AI_ASSISTED_WORKFLOW.md), and the [Canonical Context Model](CANONICAL_CONTEXT_MODEL.md).

## Recommended reading path

1. [Main case study](PUBLIC_CASE_STUDY_DRAFT.md)
2. [System context](SYSTEM_CONTEXT.md)
3. [How I AI](AI_ASSISTED_WORKFLOW.md)
4. [Canonical context model](CANONICAL_CONTEXT_MODEL.md)
5. [Exact-window composite scenario](synthetic-examples/exact-window-scenario.md)
6. [Composite operator response](synthetic-examples/operator-response.md)
7. [Synthetic CLI examples](synthetic-examples/cli-examples.md)
8. [Public artifact index](PUBLIC_ARTIFACT_INDEX.md)

## Main Pages

- [Main case study](PUBLIC_CASE_STUDY_DRAFT.md): the main public technical narrative.
- [System context](SYSTEM_CONTEXT.md): a safe preview of the automation/control system behind the debugging layer.
- [How I AI](AI_ASSISTED_WORKFLOW.md): how I use ChatGPT and Codex while keeping ownership and validation human-led.
- [Canonical context model](CANONICAL_CONTEXT_MODEL.md): how long-running AI-assisted work keeps context current without relying on raw transcript memory.
- [Public artifact index](PUBLIC_ARTIFACT_INDEX.md): a map of the public-safe pages, diagrams, synthetic examples, and packet sample.
- [Visual artifact set](PUBLIC_ARTIFACT_INDEX.md#public-safe-visual-artifacts): the approved public-safe diagrams used by the case study.

## Synthetic examples

- [Exact-window composite scenario](synthetic-examples/exact-window-scenario.md)
- [Composite operator response](synthetic-examples/operator-response.md)
- [CLI examples](synthetic-examples/cli-examples.md)
- [`evidence-packet-shape.json`](synthetic-examples/evidence-packet-shape.json)

These examples are public-safe composite/synthetic examples. They are rewritten to remove private details while preserving the technical pattern. They are not copied from private logs, runtime records, source records, transcripts, or operational systems.

## Safety and Scope

This case study uses sanitized, synthetic, and composite examples. It is intended to show the architecture and reasoning pattern without exposing private systems, raw logs, source code, or operational records.
