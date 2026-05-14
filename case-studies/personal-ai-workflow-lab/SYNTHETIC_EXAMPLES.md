# Synthetic Examples

The detailed examples now live in [synthetic-examples/](synthetic-examples/).

These are synthetic or public-safe composite examples. They preserve workflow shape, command style, evidence categories, and review boundaries without exposing private data or operational records.

The first five examples share one coherent `ITEM-123` walkthrough. Read them in order to see the same item move from fast command control, to dense dashboard review, to helper-layer validation, to packet-backed AI evaluation, to a human lifecycle decision.

For the helper and maintenance layer behind these examples, see [SUPPORTING_TOOLS.md](SUPPORTING_TOOLS.md).

![Hand-drawn evidence packet showing context, facts, assumptions, gaps, sources, and clarification needs flowing into AI reasoning, human review, and runtime or workflow update.](assets/diagrams/05-evidence-packet-anatomy.png)

## Start With This Walkthrough

For the most coherent read, follow the same synthetic `ITEM-123` through:

1. [Telegram command flow](synthetic-examples/telegram-command-flow.md) — fast control and request entry.
2. [Dashboard review flow](synthetic-examples/dashboard-review-flow.md) — dense review and comparison.
3. [Evidence packet shape](synthetic-examples/evidence-packet-shape.json) — bounded AI handoff contract.
4. [External signal review](synthetic-examples/external-signal-review.md) — lifecycle decision and audit note.

## How The Examples Map To The Architecture

The examples are a concrete walkthrough of the architecture rather than separate demo material.

The Telegram example shows the fast control surface and router entry point. The dashboard example shows the dense review surface. The helper flow shows evidence gathering, reconciliation, missing-fact checks, packet validation, and audit inspection. The packet JSON shows the bounded AI handoff contract. The external signal review example shows AI synthesis staying inside that packet while the human owns the lifecycle decision.

Together, the examples make the architecture inspectable: each synthetic artifact maps to one stage of the loop from request, to evidence, to packet, to AI reasoning, to human decision, to saved state.

## Example Index

- [Telegram command flow](synthetic-examples/telegram-command-flow.md): compact mobile-readable control for `ITEM-123`.
- [Dashboard review flow](synthetic-examples/dashboard-review-flow.md): dense comparison and evidence review for the same item.
- [Helper CLI flow](synthetic-examples/helper-cli-flow.md): synthetic dry-run scan, reconciliation, packet validation, audit summary, and diagnostic checks for `ITEM-123`.
- [Evidence packet shape](synthetic-examples/evidence-packet-shape.json): synthetic JSON packet used by the walkthrough.
- [External signal review](synthetic-examples/external-signal-review.md): lifecycle decision flow using `/review`, `/details ITEM-123`, `/evaluate ITEM-123`, and explicit human decisions.
- [Observability investigation](synthetic-examples/observability-investigation.md): bounded investigation with evidence, hypothesis, uncertainty, and next check.
- [Control workflow review](synthetic-examples/control-workflow-review.md): generic state, intent, guard, AI explanation, and human approval boundary.

## Next Step

Next step in the core path: [IMPLEMENTATION_EVIDENCE.md](IMPLEMENTATION_EVIDENCE.md).
