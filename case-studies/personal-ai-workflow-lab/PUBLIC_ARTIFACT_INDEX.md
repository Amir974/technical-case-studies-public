# Public Artifact Index

[Main case study](README.md) | [Companion notes](PUBLIC_CASE_STUDY.md) | [Architecture](ARCHITECTURE.md) | [Control surfaces](CONTROL_SURFACES.md) | [Supporting tools](SUPPORTING_TOOLS.md) | [Implementation evidence](IMPLEMENTATION_EVIDENCE.md) | [Activity ledger](IMPLEMENTATION_ACTIVITY_LEDGER.md) | [Boundary](AI_RUNTIME_HUMAN_BOUNDARY.md) | [Workflow evolution](WORKFLOW_EVOLUTION.md)

Public-safe artifacts in this public artifact include the main narrative, companion notes, support pages, synthetic examples, diagram assets, visual specs, and publication notes.

## Start Here

Start with [README.md](README.md). It is now the main reader experience and explains why the system exists, how Telegram and dashboard split responsibilities, why the evidence-gathering layer matters, where AI fits, and why human review remains explicit.

## Main Pages

| File | Role |
| --- | --- |
| [README.md](README.md) | Main public-facing case-study narrative. |
| [PUBLIC_CASE_STUDY.md](PUBLIC_CASE_STUDY.md) | Companion notes on design tradeoffs and evidence discipline. |
| [ARCHITECTURE.md](ARCHITECTURE.md) | System/product architecture and design decisions. |
| [CONTROL_SURFACES.md](CONTROL_SURFACES.md) | Telegram vs dashboard product lesson. |
| [SUPPORTING_TOOLS.md](SUPPORTING_TOOLS.md) | Helper and maintenance layer that prepares evidence behind the visible surfaces. |
| [IMPLEMENTATION_EVIDENCE.md](IMPLEMENTATION_EVIDENCE.md) | Public-safe proof layer summarizing private implementation history by category. |
| [IMPLEMENTATION_ACTIVITY_LEDGER.md](IMPLEMENTATION_ACTIVITY_LEDGER.md) | Scan-friendly sanitized activity appendix with a representative trail, synthetic IDs, work-type classification, helper mapping, and component support. |
| [AI_RUNTIME_HUMAN_BOUNDARY.md](AI_RUNTIME_HUMAN_BOUNDARY.md) | AI, runtime, and human responsibility split. |
| [WORKFLOW_EVOLUTION.md](WORKFLOW_EVOLUTION.md) | How the workflow lab evolved. |
| [SYNTHETIC_EXAMPLES.md](SYNTHETIC_EXAMPLES.md) | Compatibility index pointing to split examples. |
| [PUBLICATION_NOTES.md](PUBLICATION_NOTES.md) | Publication stance and safety notes. |

## Synthetic Examples

| Artifact | Role |
| --- | --- |
| [telegram-command-flow.md](synthetic-examples/telegram-command-flow.md) | Shows compact mobile-readable control for the `ITEM-123` walkthrough. |
| [dashboard-review-flow.md](synthetic-examples/dashboard-review-flow.md) | Shows dense review for the same walkthrough item. |
| [evidence-packet-shape.json](synthetic-examples/evidence-packet-shape.json) | Shows the synthetic packet contract used by the walkthrough. |
| [helper-cli-flow.md](synthetic-examples/helper-cli-flow.md) | Shows synthetic helper commands for dry-run intake, reconciliation, packet validation, audit inspection, and diagnostics. |
| [external-signal-review.md](synthetic-examples/external-signal-review.md) | Shows incoming-item triage, evaluation, lifecycle decision, and audit note. |
| [observability-investigation.md](synthetic-examples/observability-investigation.md) | Shows bounded investigation with evidence, hypothesis, uncertainty, and next check. |
| [control-workflow-review.md](synthetic-examples/control-workflow-review.md) | Shows generic state, intent, guard, explanation, and human approval boundary. |

## Visual Assets

| Visual | Placement | Status |
| --- | --- | --- |
| [01-durable-split.png](assets/diagrams/01-durable-split.png) | [README.md](README.md) | Integrated draft image. |
| [02-how-a-request-flows.png](assets/diagrams/02-how-a-request-flows.png) | [ARCHITECTURE.md](ARCHITECTURE.md) | Integrated draft image. |
| [03-three-workflows-one-pattern.png](assets/diagrams/03-three-workflows-one-pattern.png) | [ARCHITECTURE.md](ARCHITECTURE.md) | Integrated draft image. |
| [04-telegram-vs-dashboard.png](assets/diagrams/04-telegram-vs-dashboard.png) | [CONTROL_SURFACES.md](CONTROL_SURFACES.md) | Integrated draft image. |
| [05-evidence-packet-anatomy.png](assets/diagrams/05-evidence-packet-anatomy.png) | [SYNTHETIC_EXAMPLES.md](SYNTHETIC_EXAMPLES.md) | Integrated draft image. |
| [06-human-in-the-loop-boundary.png](assets/diagrams/06-human-in-the-loop-boundary.png) | [AI_RUNTIME_HUMAN_BOUNDARY.md](AI_RUNTIME_HUMAN_BOUNDARY.md) | Integrated draft image. |
| [07-full-workflow-architecture.png](assets/diagrams/07-full-workflow-architecture.png) | [ARCHITECTURE.md](ARCHITECTURE.md) | Integrated draft image. |
| [08-evidence-gathering-layer.png](assets/diagrams/08-evidence-gathering-layer.png) | [ARCHITECTURE.md](ARCHITECTURE.md) | Integrated draft image. |
| [09-helper-and-maintenance-tools.png](assets/diagrams/09-helper-and-maintenance-tools.png) | [SUPPORTING_TOOLS.md](SUPPORTING_TOOLS.md) | Integrated draft image. |

The Mermaid skeleton is [assets/architecture.mmd](assets/architecture.mmd). The designed visual specs are in [assets/diagram_specs.md](assets/diagram_specs.md). These images remain part of the curated public artifact until a separate publication review approves export.

## Publication And Safety Notes

Use [PUBLICATION_NOTES.md](PUBLICATION_NOTES.md) before any public export. The draft uses synthetic and public-safe composite examples, qualitative claims, generic labels, and explicit human-review boundaries.

Private working material exists outside this public case-study artifact to support internal review. It is not part of the public artifact map and should not be exported. Private proof ledgers remain private working material, not public artifacts.

## Related Case Studies

- **Published:** AI-Assisted Debugging Layer for Complex Automation.
- **Forthcoming/planned:** External Signal Review.
- **Forthcoming/planned:** Control Workflow Review.
- **Forthcoming/planned:** AI Workflow Operations.

## What Is Intentionally Not Included

This public artifact does not include private source material, raw operational evidence, account data, contact data, exact internal identifiers, private commands, screenshots, generated images outside the reviewed diagram set, or implementation-specific access details.
