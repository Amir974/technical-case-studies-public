# Public Artifact Index

[Case-study home](README.md) | [Main case study](PUBLIC_CASE_STUDY_DRAFT.md) | [How I AI](AI_ASSISTED_WORKFLOW.md) | [Canonical context](CANONICAL_CONTEXT_MODEL.md)

This page lists the public-safe artifacts used in the case study: diagrams, synthetic examples, and supporting explanation pages.

## Public pages

| File | Role |
| --- | --- |
| [PUBLIC_CASE_STUDY_DRAFT.md](PUBLIC_CASE_STUDY_DRAFT.md) | Main technical case study with layered explanation, system context links, composite walkthrough, AI boundary, and claim limits. |
| [SYSTEM_CONTEXT.md](SYSTEM_CONTEXT.md) | Explains the automation/control system behind the debugging layer without exposing infrastructure or private operational details. |
| [AI_ASSISTED_WORKFLOW.md](AI_ASSISTED_WORKFLOW.md) | Explains how I use ChatGPT and Codex while retaining human ownership of goals, validation, and acceptance. |
| [CANONICAL_CONTEXT_MODEL.md](CANONICAL_CONTEXT_MODEL.md) | Explains how transcript material becomes durable guidance over time. |

## Recommended public reading path

1. [Main case study](PUBLIC_CASE_STUDY_DRAFT.md)
2. [System context](SYSTEM_CONTEXT.md)
3. [How I AI](AI_ASSISTED_WORKFLOW.md)
4. [Canonical context model](CANONICAL_CONTEXT_MODEL.md)
5. [Exact-window scenario](synthetic-examples/exact-window-scenario.md)
6. [Operator response](synthetic-examples/operator-response.md)
7. [CLI examples](synthetic-examples/cli-examples.md)
8. [Synthetic evidence packet](synthetic-examples/evidence-packet-shape.json)

## Synthetic examples

| Artifact | Role |
| --- | --- |
| [Exact-window scenario](synthetic-examples/exact-window-scenario.md) | Shows the operator question and exact-window investigation setup. |
| [Operator response](synthetic-examples/operator-response.md) | Shows how bounded evidence becomes a reviewable response with confidence and gaps. |
| [CLI examples](synthetic-examples/cli-examples.md) | Shows non-executable command shapes and output style. |
| [Synthetic evidence packet](synthetic-examples/evidence-packet-shape.json) | Shows the bounded packet shape used by the AI explanation layer: question, exact window, evidence sources, detector events, verdict, confidence, gaps, and next checks. |

## Public-safe visual artifacts

| Diagram | Role |
| --- | --- |
| [Debugging-layer architecture](assets/architecture-overview.png) | Shows the event-driven investigation path from bounded evidence collection through AI-assisted reasoning, explanation, pipeline health, and human review. |
| [Debugging-layer flow](assets/debugging-layer-flow.png) | Shows how an operator question becomes an exact-window evidence packet, detector events, verdict, explanation, and reviewable output. |
| [AI boundary](assets/ai-boundary.png) | Shows the non-actuating AI boundary: AI supports reasoning and explanation while final decisions and actuation remain outside AI ownership. |
| [Context retention loop](assets/context-retention-loop.png) | Shows how reviewed sessions become durable notes, playbooks, checklists, and future AI session context. |
| [Automation/control model](assets/automation-control-model.png) | Shows evidence capture points across staged control logic so investigations can explain the decision path, not only final state. |
| [Investigation evolution](assets/investigation-evolution.png) | Shows the shift from ad hoc reconstruction toward bounded evidence, layered reasoning, reviewable output, and durable lessons. |

## Note

Internal planning and review artifacts are not part of the public artifact set.
