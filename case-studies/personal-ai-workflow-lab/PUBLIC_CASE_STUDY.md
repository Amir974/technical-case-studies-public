# Companion Notes: Design Tradeoffs And Evidence Discipline

[Case-study home](README.md) | [Architecture](ARCHITECTURE.md) | [Control surfaces](CONTROL_SURFACES.md) | [AI/runtime/human boundary](AI_RUNTIME_HUMAN_BOUNDARY.md) | [Workflow evolution](WORKFLOW_EVOLUTION.md) | [Artifact index](PUBLIC_ARTIFACT_INDEX.md)

The main case-study narrative now lives in [README.md](README.md). These notes keep the deeper design tradeoffs in one place so the landing page can read as a flowing article instead of a directory.

## The Product Shape

The workflow lab grew from a simple question: could AI help me operate real workflows if the surrounding product kept the work bounded?

The answer was not to make a chatbot more powerful. It was to make the surrounding loop more explicit. The loop needs a surface to start from, a router to resolve intent, workflow modules that know their scope, helpers that gather evidence, a packet builder that shapes the handoff, AI that reasons inside the packet, and a human decision that records what happened next.

That shape matters because most AI workflow failures are not only model failures. They are context failures, authority failures, or product-surface failures. The system tries to make those boundaries visible.

## Why The Packet Became The Contract

The evidence packet is the most important artifact in the system. It is where vague context becomes reviewable input.

A useful packet says what is being reviewed, which workflow it belongs to, what evidence was checked, what is known, what is missing, what prior state exists, what AI is being asked to do, and which actions are allowed afterward.

That contract gives me something to challenge. If the AI recommendation is too strong, I can check whether the packet actually supports it. If the packet is thin, the right answer is often not a bolder model response. The right answer is better evidence gathering or a parked decision.

## Evidence Gathering Is Product Work

The helper layer is easy to miss because the user-facing flow looks compact. In practice, evidence gathering is a product layer of its own.

For external signal review, the helper work includes source-message intake, source reconciliation, stored item state, prior decisions, missing-fact checks, and manual assists where external pages or source cards are not reliable enough for full automation.

For observability investigation, the helper work includes exact-scope evidence collection, recent state, prior decisions, diagnostic summaries, and packet trust checks. The already-published observability/debugging case study goes deeper on that vertical.

For control workflow review, the public-safe story is deliberately generic: state, intent, guard behavior, uncertainty, and human next checks. The public draft does not expose private environment details or claim that the assistant controls the underlying system.

The design lesson is that packet generation should be treated as a visible workflow stage, not as a black box before AI.

## Surface Split

Telegram was valuable because it made the workflow reachable. It is good for status, one-item lookup, compact evaluation requests, and explicit decisions.

The dashboard became necessary when review density increased. Dense review needs table space, filters, lifecycle state, evidence coverage, missing-fact visibility, and summary/detail navigation. Those are not failures of chat; they are different product needs.

Keeping both surfaces avoids forcing one interface to do every job. Telegram stays fast. The dashboard stays deliberate. Both feed the same bounded workflow loop.

## AI Boundary

AI is the reasoning layer, not the layer with authority.

The model can synthesize, explain, evaluate, and name gaps. It should not approve an item, mutate state, contact anyone, publish anything, or turn a recommendation into action. Those exclusions are not cosmetic. They are how the workflow remains inspectable.

Runtime code also has a boundary. It routes requests, gathers context, builds packets, records state, and returns updates. It should not pretend that routing or storage logic is a human judgment call.

## What Stayed Qualitative

This artifact avoids exact claims about duration, adoption, time saved, reliability, accuracy, production readiness, or automation success. Those would require a separate validation pass.

The public claims are qualitative and architectural: the workflow became more structured, more reviewable, easier to repeat, and clearer about the boundary between evidence, AI interpretation, runtime behavior, and human decision.

## How To Read The Synthetic Examples

The examples are intentionally connected through `ITEM-123`.

Start with [telegram-command-flow.md](synthetic-examples/telegram-command-flow.md) to see fast control. Move to [dashboard-review-flow.md](synthetic-examples/dashboard-review-flow.md) for dense review. Read [external-signal-review.md](synthetic-examples/external-signal-review.md) for the lifecycle decision. The JSON packet in [evidence-packet-shape.json](synthetic-examples/evidence-packet-shape.json) is the packet shape used by that walkthrough.

The examples preserve workflow structure, command shape, evidence categories, gap handling, and human decision boundaries. They do not preserve private source values.
