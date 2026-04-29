# Canonical Context Model

[Case-study home](README.md) | [Main case study](PUBLIC_CASE_STUDY_DRAFT.md) | [How I AI](AI_ASSISTED_WORKFLOW.md) | [System context](SYSTEM_CONTEXT.md) | [Artifact index](PUBLIC_ARTIFACT_INDEX.md)

## Start here

Long-running AI-assisted work needs a way to keep context current. This page explains the public-safe model I use without publishing the private canonical docs themselves.

## The short version (TL;DR)

Raw transcripts are useful history, but they are not current truth by default. Durable context comes from validated notes, contracts, playbooks, validation rules, summaries, retrospectives, closeouts, and acceptance checklists that future humans and AI sessions can rely on.

## Why raw transcripts are not enough

Transcripts capture how work unfolded, including partial decisions, uncertainty, mistakes, and old assumptions. That makes them useful, but also risky as a primary source of truth.

Older transcripts may be superseded by newer validated decisions. A transcript can explain why something happened, but a current source-of-truth note or contract should carry more weight when it reflects a reviewed and accepted state.

There is also a practical AI limitation. Current AI models have limited working context. Long transcripts can exceed useful context windows, consume unnecessary tokens, and mix current decisions with stale or superseded assumptions.

For that reason, I do not treat raw transcript history as something that should be pasted wholesale into every new session. The better pattern is to keep transcripts and source material available outside the active prompt, then selectively bring in the relevant reviewed context when a new investigation, edit, or explanation needs it.

## What becomes durable context

Durable context includes material that has been reviewed, cleaned up, or accepted as reusable:

- Source-of-truth notes.
- Contracts and interface notes.
- Playbooks.
- Validation rules.
- Current-state summaries.
- Retrospectives.
- Closeouts.
- Acceptance checklists.

The point is not to preserve every conversation. The point is to preserve the parts that should guide future work.

## How transcript material is used

Transcript material can still be useful as historical evidence. I use it based on freshness, validation, and whether its lesson was promoted into durable docs.

If an old transcript conflicts with a newer validated note, the newer validated note should usually win. If the transcript contains a useful lesson that never became durable context, the next step is to extract the lesson, review it, and decide whether it should be promoted.

In practice, transcript material is treated as source material, not authority. It can be searched, summarized, compared, or mined for lessons, but durable context is what future work should rely on by default.

## How lessons become guidance

When a pattern repeats, I turn it into durable guidance. That can mean a source-of-truth update, a playbook note, a validation rule, a contract clarification, or a checklist item.

From that point on, the lesson changes how future work is planned and reviewed. This is how the project reduces drift instead of rediscovering the same lesson in each new AI session.

## Example document types

Public-safe examples of durable context types:

- A current-state summary that says what is trusted now.
- A contract note that defines what an evidence packet must contain.
- A playbook that describes how to run an investigation loop.
- A validation note that records what must be checked before acceptance.
- A retrospective that turns repeated friction into a better rule.
- A closeout that captures what changed and what remains open.
- An acceptance checklist for public-facing material.

## What stays private

This public page is a sanitized model, not a copy of the private canonical docs.

I do not publish raw canonical docs, internal repo paths, machine names, hostnames, IPs, commands, private incident details, runtime paths, security/access details, or raw transcripts.

## How this supports future AI sessions

AI-assisted work is easier to review when a new session starts from current context instead of loose memory.

The canonical context model gives future AI sessions a cleaner starting point: what is trusted, what changed, what boundaries matter, what validation is required, and which old material has been superseded.

That is what keeps the debugging workflow from becoming a chain of disconnected prompts.

## Related pages

- [Main case study](PUBLIC_CASE_STUDY_DRAFT.md)
- [How I AI](AI_ASSISTED_WORKFLOW.md)
- [System context](SYSTEM_CONTEXT.md)
- [Exact-window scenario](synthetic-examples/exact-window-scenario.md)
- [Artifact index](PUBLIC_ARTIFACT_INDEX.md)
