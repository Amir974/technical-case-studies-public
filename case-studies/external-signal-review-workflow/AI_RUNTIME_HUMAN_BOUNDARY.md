# AI, Runtime, And Human Boundary

This workflow is AI-assisted decision support, not autonomous action. The design separates helper evidence work, AI reasoning, runtime orchestration, human decision, and audited state update.

## Responsibility Model

| Layer | Responsibility | Boundary |
|---|---|---|
| Helper/evidence layer | Gather source coverage, known facts, missing facts, ambiguity flags, and reconciliation hints. | Does not decide or mutate lifecycle state. |
| AI reasoning | Assess the bounded packet, summarize fit, name risks, and recommend a next human action. | Does not own goals, final decisions, outreach, submission, approval, closure, or state mutation. |
| Runtime/orchestration | Route commands, build packets, validate allowed actions, persist state, and record audit. | Does not convert AI recommendation into action without explicit human choice. |
| Human decision | Choose whether to approve, park, close, clarify, or request more evidence. | Owns judgment and final workflow intent. |
| Audited state update | Store before/after state, decision source, evidence reference, and timestamp category. | Records an explicit decision; it is not a hidden AI action. |

> _Visual placeholder: `assets/diagrams/04-ai-runtime-human-boundary.png` -- AI and runtime prepare review material, human decision gates state mutation, and state updates are audited._

## Decision and State Mutation Protocol

1. System ingests/reconciles external signal.
2. System extracts known facts and missing facts.
3. System builds bounded evidence packet.
4. AI produces assessment only.
5. If ambiguity exists, system asks for human clarification and does not mutate lifecycle.
6. Human chooses an allowed action.
7. Runtime applies the explicit state update.
8. Audit ledger records decision source, before/after state, evidence packet reference, and timestamp category.
9. Dry-run reconciliation plans remain separate from applied actions.

## What AI Can Do

- Summarize a packet.
- Compare known facts against the assessment request.
- Name missing facts.
- Identify risks and gaps.
- Recommend an allowed next human action.
- Explain confidence and uncertainty.

## What AI Cannot Do

- Make the final decision.
- Mutate runtime state.
- Treat ambiguous evidence as resolved.
- Convert a dry-run reconciliation plan into an applied action.
- Contact external parties or submit anything.
- Invent an objective score that was not supplied by a human or evaluator.

## Why This Boundary Matters

The workflow is useful because every layer can be inspected. If AI overreaches, the packet and allowed actions show the limit. If evidence is thin, missing facts stay visible. If state changes, the audit record points back to a human decision and a packet reference.
