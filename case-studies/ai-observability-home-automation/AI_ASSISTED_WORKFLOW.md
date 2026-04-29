# How I AI: My AI-Assisted Workflow

[Case-study home](README.md) | [Main case study](PUBLIC_CASE_STUDY_DRAFT.md) | [System context](SYSTEM_CONTEXT.md) | [Canonical context](CANONICAL_CONTEXT_MODEL.md) | [Artifact index](PUBLIC_ARTIFACT_INDEX.md)

## Status

This page explains how I work with AI on this project.

The goal is to show the working pattern: AI helps with reasoning, editing, review, and synthesis, while I keep ownership of goals, validation, acceptance, and publication decisions.

## Why this matters

The debugging layer is not only about an automation system. It is also about how I work with AI on a project that has real constraints, long memory, evolving decisions, and a need for careful review.

At some point, just opening a new chat and asking a broad question stopped being enough. The project needed a way to carry context forward, keep edits scoped, and make every AI-assisted step reviewable.

## The short version (TL;DR)

ChatGPT is the primary reasoning and synthesis partner in this workflow. Codex is the primary repo-editing agent for code, documentation, and bounded validation work.

I sometimes use Gemini and Claude for second opinions, evaluation, or alternative reasoning. I do not treat this as a vendor comparison; different models are useful for different review angles.

AI helps me move through investigation, writing, refactoring, and review with more structure. It does not own the system.

## My role

I own:

- Goals and priorities.
- Domain judgment.
- Acceptance criteria.
- Runtime validation.
- Safety boundaries.
- Publication decisions.
- Final approval or rejection of proposed changes.

In practice, that means I decide what problem matters, what tradeoff is acceptable, what evidence is enough, and whether a result is actually usable.

My developer background matters here: I started my career as a developer, so I still use that background when reviewing architecture, debugging logic, and challenging implementation choices. I do not usually code directly anymore; I work through AI-assisted development loops where I define intent, constraints, and acceptance, then review and validate the output.

## The role model

The work often moves across roles that would normally be split across several people:

| Role | My responsibility | AI/tool responsibility |
| --- | --- | --- |
| Product owner | Define the outcome, priority, and acceptable tradeoffs. | Help clarify options, risks, and decision points. |
| Architect | Set boundaries, contracts, and system direction. | Challenge assumptions and propose alternative shapes. |
| Developer / senior developer | Review technical fit, logic, and implementation choices. | Draft scoped changes and surface likely edge cases. |
| QA / reviewer | Decide what needs validation and whether the result is acceptable. | Run bounded checks, inspect diffs, and summarize risks. |
| Technical writer | Decide what the public or internal explanation should communicate. | Draft, restructure, and simplify docs. |
| Retrospective / process owner | Decide which lessons should change future work. | Help identify repeated patterns and turn them into guidance. |

Some of those roles are shared between me and the AI tools. I still own the goals, judgment, validation, acceptance, and publication decisions.

## ChatGPT’s role

ChatGPT acts as:

- A reasoning partner.
- An investigation partner.
- A planner.
- A reviewer.
- A writer and synthesis layer.
- A way to turn messy context into clearer decisions and next steps.

It is most useful when the question is bounded and the relevant context has already been distilled into durable notes, contracts, or examples.

## Codex’s role

I use Codex as the primary editing agent for code and documentation changes, while I remain responsible for goals, review, validation, and acceptance.

In this project, AI-assisted implementation includes more than prose editing. ChatGPT helps reason through automation behavior, edge cases, architecture, validation strategy, and debugging plans. Codex is used to make scoped repository edits across documentation and implementation surfaces such as automations, scripts, Python utilities, templates, configuration, and validation checks.

Codex is useful for:

- Editing repo files.
- Rebuilding docs.
- Applying scoped changes.
- Running bounded validation commands.
- Checking links, headings, and privacy patterns.
- Keeping changes inside an explicit file scope.

Codex does not decide what should ship. It prepares changes for review.

## What AI does not own

AI does not own:

- Final decisions.
- Production authority.
- External actuation.
- Safety approval.
- Runtime acceptance.
- Publication approval.
- Claims about impact, reliability, or completeness.

AI can propose, summarize, edit, and explain. I remain responsible for deciding whether the result is correct and safe.

## How context is retained

Raw chat history is not the source of truth.

Important decisions and lessons are distilled into state-of-truth docs, playbooks, contracts, validation notes, and canonical references. These documents are written so both humans and future AI sessions can use them.

That reduces drift across long-running AI-assisted work. Instead of asking a future session to infer the project from old conversation fragments, the project keeps current references that say what is trusted, what changed, what is still uncertain, and what boundaries matter.

From time to time, I run retrospectives on the AI-assisted workflow itself. When a lesson is reusable, I turn it into durable guidance: source-of-truth notes, playbooks, validation rules, or canonical docs. From that point on, the lesson changes how future work is planned and reviewed.

## How a typical investigation/fix loop works

A typical loop looks like this:

1. Ask a bounded question.
2. Gather a packet or evidence summary.
3. Reason over the packet and curated context.
4. Identify likely cause, confidence, and gaps.
5. Prepare a bounded fix plan.
6. Use Codex for scoped repo changes where relevant.
7. Validate behavior or review the result.
8. Accept, reject, or revise.
9. Turn reusable lessons into durable docs.

The same pattern applies to documentation work. The question is bounded, the context is explicit, the edit surface is scoped, and the result is validated before acceptance.

## Why this is different from just prompting

Just prompting often produces a plausible answer with unclear evidence.

This workflow tries to make the evidence and boundaries visible:

- What question is being answered?
- What files or system areas are in scope?
- What evidence is available?
- What is missing?
- What did AI infer?
- What did a human validate?
- What should become durable context for next time?

That is the connection between the engineering workflow and the observability layer. Both rely on bounded context, explicit evidence, and reviewable conclusions.

## Why this is not just vibe coding

There is nothing wrong with quick exploratory AI coding, but this project needs a more controlled loop: define the intent, limit the edit surface, validate the result, and turn reusable lessons into durable guidance.

The difference is not whether AI writes code. In many cases it does. The difference is that the work is bounded by explicit goals, file scope, validation expectations, review checkpoints, and human acceptance. The AI may draft automations, scripts, Python code, templates, or documentation, but it does not decide what is correct or safe to ship.

## Boundaries I keep

The same boundaries apply throughout the project:

- No raw private records in public examples.
- No direct publication of raw transcripts or logs.
- No private paths, hostnames, IPs, entity IDs, device names, contacts, or household-sensitive details.
- No autonomous actuation.
- No public claims of quantified impact, production completeness, or reliability without separate validation.
- No publication without review.

Public examples are sanitized or composite: rewritten to remove private details while preserving the technical pattern.

## Related pages

- [Main case study](PUBLIC_CASE_STUDY_DRAFT.md)
- [System context](SYSTEM_CONTEXT.md)
- [Canonical context model](CANONICAL_CONTEXT_MODEL.md)
- [Exact-window synthetic scenario](synthetic-examples/exact-window-scenario.md)
- [Synthetic CLI examples](synthetic-examples/cli-examples.md)
- [Artifact index](PUBLIC_ARTIFACT_INDEX.md)
