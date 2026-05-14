# Diagram Specs

Shared style direction for all diagrams: hand-drawn whiteboard, simple black marker lines, light color highlights, sticky-note or marker annotations, short labels, one idea per diagram, informal but clear. Avoid corporate architecture styling and avoid a single poster that tries to explain everything.

The approved draft PNGs live in [diagrams/](diagrams/). Do not add or regenerate image assets from this file until a separate publication review approves the labels and safety boundary.

## 01-durable-split

Purpose: Show the durable role split: Telegram is the fast control surface, dashboard is the dense review surface, evidence helpers gather context, AI reasons over bounded packets, runtime handles retrieval, routing, state, and audit, and human review owns decisions.

Filename: [diagrams/01-durable-split.png](diagrams/01-durable-split.png)

Placement: [README.md](../README.md) near the top.

Must-show: Telegram, dashboard, evidence helpers, AI, runtime, human decision owner, bounded evidence packet.

Must-not-show: private topology, filesystem locations, private system names, product UI, personal data, real external-signal details, private environment details, or operational records.

Suggested visual layout: Six sticky notes arranged around a simple evidence packet in the center. Use light highlights to separate fast action, dense review, evidence gathering, reasoning, runtime, and decision ownership.

Alt text: Hand-drawn sketch showing Telegram for fast control, dashboard for dense review, evidence helpers gathering context, AI reasoning over a bounded packet, runtime handling routing and audit, and a human owning final decisions.

Prompt draft: Create a hand-drawn whiteboard explainer diagram with simple black marker lines and light color highlights. Show six labeled sticky notes: Telegram fast control, Dashboard dense review, Evidence helpers, AI reasoning, Runtime routing and audit, Human decision owner. Put a small bounded evidence packet in the middle. Use short labels and an informal explainer style. Do not include real UI, private details, or implementation identifiers.

Safety notes: Keep all labels generic. Do not imply that AI owns final decisions.

## 02-how-a-request-flows

Purpose: Show request -> route -> workflow module -> evidence gatherers -> evidence packet -> AI reasoning -> human decision -> audit/status update.

Filename: [diagrams/02-how-a-request-flows.png](diagrams/02-how-a-request-flows.png)

Placement: [ARCHITECTURE.md](../ARCHITECTURE.md).

Must-show: request, command router, workflow module, evidence gatherers, evidence packet, AI reasoning/evaluation, human decision, audit/status update.

Must-not-show: real commands beyond the approved generic examples, private identifiers, private system names, raw records, screenshots, or exact operational values.

Suggested visual layout: A left-to-right marker flow with eight small boxes and a final arrow returning status to Telegram/dashboard.

Alt text: Hand-drawn flow showing a request moving through routing, a workflow module, evidence gathering, evidence packet creation, AI reasoning, human decision, and audited status update.

Prompt draft: Draw a simple whiteboard flow with black marker arrows and light highlights. Label the steps Request, Route, Workflow, Evidence Gatherers, Evidence Packet, AI Review, Human Decision, Audit/Status. Keep the diagram compact, friendly, and clear. Use no private names, screenshots, or real data.

Safety notes: Use only generic labels. Keep AI before human decision and audit after human decision.

## 03-three-workflows-one-pattern

Purpose: Show three verticals sharing the same operating pattern: External Signal Review, Observability Investigation, and Control Workflow Review.

Filename: [diagrams/03-three-workflows-one-pattern.png](diagrams/03-three-workflows-one-pattern.png)

Placement: [ARCHITECTURE.md](../ARCHITECTURE.md).

Must-show: three workflow lanes feeding evidence gatherers, evidence packets, AI review, human decision, and audited state.

Must-not-show: real item names, private environment details, account data, implementation identifiers, screenshots, or operational records.

Suggested visual layout: Three stacked lanes on the left converging into one shared review loop on the right.

Alt text: Hand-drawn sketch showing External Signal Review, Observability Investigation, and Control Workflow Review feeding the same evidence gathering, evidence packet, AI review, human decision, and audit loop.

Prompt draft: Create a whiteboard-style explainer with three simple lanes labeled External Signal Review, Observability Investigation, and Control Workflow Review. Have all three feed a shared loop labeled Evidence Gatherers, Evidence Packet, AI Review, Human Decision, Audited State. Use black sketch lines, light highlights, and short sticky-note labels. Avoid detailed infrastructure or real data.

Safety notes: Keep each vertical generic. Do not reveal private operational details.

## 04-telegram-vs-dashboard

Purpose: Show why Telegram is fast, mobile, and action-oriented while the dashboard is dense, context-rich, and comparison-oriented.

Filename: [diagrams/04-telegram-vs-dashboard.png](diagrams/04-telegram-vs-dashboard.png)

Placement: [CONTROL_SURFACES.md](../CONTROL_SURFACES.md).

Must-show: Telegram side for quick commands/status/actions; dashboard side for comparison, ranking, lifecycle context, and evidence review.

Must-not-show: real UI screenshots, account details, item names, private workflow labels, or source-specific data.

Suggested visual layout: Split whiteboard panel with Telegram on the left and dashboard on the right, connected by the same review loop.

Alt text: Hand-drawn comparison of Telegram as the fast action surface and dashboard as the dense review surface.

Prompt draft: Draw a hand-drawn split-panel whiteboard diagram. Left side: Telegram fast action with short command/status bubbles. Right side: Dashboard dense review with comparison, ranking, lifecycle, and evidence notes. Use simple black lines and light highlights. Keep labels generic and avoid real UI.

Safety notes: Do not recreate a real screen. Keep this as conceptual layout only.

## 05-evidence-packet-anatomy

Purpose: Show bounded packet contents: request, source coverage, relevant facts, missing facts, prior state, AI task, risks/gaps, allowed next actions, and audit policy.

Filename: [diagrams/05-evidence-packet-anatomy.png](diagrams/05-evidence-packet-anatomy.png)

Placement: [SYNTHETIC_EXAMPLES.md](../SYNTHETIC_EXAMPLES.md).

Must-show: a single packet with labeled sections for request, source coverage, known facts, missing facts, prior state, AI task, risks/gaps, allowed actions, and audit policy.

Must-not-show: real records, verbatim transcripts, private source names, private identifiers, exact operational values, or personal data.

Suggested visual layout: One large sketched packet page with sticky-note callouts attached to each section.

Alt text: Hand-drawn evidence packet showing request, source coverage, known facts, missing facts, prior state, AI task, risks and gaps, allowed actions, and audit policy.

Prompt draft: Create a whiteboard sketch of an evidence packet as a page with simple labeled sections: Request, Source Coverage, Known Facts, Missing Facts, Prior State, AI Task, Risks/Gaps, Allowed Actions, Audit Policy. Use black marker lines, light highlights, and sticky-note annotations. Keep the content synthetic and generic.

Safety notes: Use category labels only. Do not include example values that look real.

## 06-human-in-the-loop-boundary

Purpose: Show where AI stops and human approval begins: AI can explain/evaluate, runtime can prepare/record, and human approves, parks, or closes.

Filename: [diagrams/06-human-in-the-loop-boundary.png](diagrams/06-human-in-the-loop-boundary.png)

Placement: [AI_RUNTIME_HUMAN_BOUNDARY.md](../AI_RUNTIME_HUMAN_BOUNDARY.md).

Must-show: AI explanation/evaluation, runtime prepare/record, clear human approval boundary, approve/park/close choices, audit after decision.

Must-not-show: autonomous action, private controls, private environment details, real system state, or operational records.

Suggested visual layout: A vertical boundary line. Left side: AI explains and runtime prepares. Right side: human decides. Below: audit/state after the decision.

Alt text: Hand-drawn boundary diagram showing AI and runtime preparing a recommendation, a clear human approval line, and audited state after the human decision.

Prompt draft: Draw a simple whiteboard boundary diagram with a bold marker line labeled Human Decision Boundary. On the left, show AI Explain/Evaluate and Runtime Prepare/Record. On the right, show Human Approve, Park, or Close. Add Audited State below the human decision. Use light highlights and short labels. Do not show autonomous action or private system details.

Safety notes: The diagram must make human ownership visually obvious.

## 07-full-workflow-architecture

Purpose: Turn [architecture.mmd](architecture.mmd) into a reader-facing hand-drawn architecture visual.

Filename: [diagrams/07-full-workflow-architecture.png](diagrams/07-full-workflow-architecture.png)

Placement: [ARCHITECTURE.md](../ARCHITECTURE.md) near the top.

Must-show: Human Operator, Telegram Control Surface, Dashboard Review Surface, Command Router, Workflow Orchestrator, External Signal Review, Observability Investigation, Control Workflow Review, Evidence Gatherers / Enrichment Helpers, Evidence Packet Builder, AI Reasoning / Evaluation, Human Review / Approval, Audit Log / State Store, Status / Queue Updates.

Must-not-show: private topology, filesystem paths, internal machine names, network addresses, product UI, personal data, real external-signal details, private environment details, or real records.

Suggested visual layout: Human Operator at the top left with two arrows to Telegram and Dashboard. Telegram and Dashboard connect to the Command Router. Router connects to Workflow Orchestrator. Three workflow lanes feed Evidence Gatherers / Enrichment Helpers, which feed Evidence Packet Builder. Packet flows to AI Reasoning / Evaluation, then to Human Review / Approval, then to Audit Log / State Store, then Status / Queue Updates back to Telegram and Dashboard.

Alt text: Hand-drawn architecture map showing a human operator using Telegram and dashboard surfaces, routed workflows using evidence gatherers to build packets for AI reasoning, human review, audited state, and status updates.

Prompt draft: Create a hand-drawn whiteboard architecture map, not a corporate diagram. Use black marker lines, light highlights, and short labels. Show Human Operator, Telegram Control Surface, Dashboard Review Surface, Command Router, Workflow Orchestrator, three workflow lanes, Evidence Gatherers / Enrichment Helpers, Evidence Packet Builder, AI Reasoning / Evaluation, Human Review / Approval, Audit Log / State Store, and Status / Queue Updates. Keep the arrows clear and avoid private topology, real UI, personal data, or implementation-specific labels.

Safety notes: Keep the architecture generic. Make human review the visible acceptance point and avoid any implication of autonomous outreach or autonomous state mutation.

## 08-evidence-gathering-layer

Purpose: Show how a useful packet is assembled from source messages, prior state, local context, browser/manual assists, diagnostic helpers, and workflow state before AI sees it.

Filename: [diagrams/08-evidence-gathering-layer.png](diagrams/08-evidence-gathering-layer.png)

Placement: [ARCHITECTURE.md](../ARCHITECTURE.md). [README.md](../README.md) links to the architecture section instead of embedding a duplicate image.

Must-show: source messages, prior state, local context, manual/browser assist, diagnostic helper, workflow state, evidence packet builder, AI reasoning.

Must-not-show: specific source-system names, company names, real URLs, private paths, local machine names, raw records, exact counts, real UI, or personal data.

Suggested visual layout: Evidence sources on the left as small sticky notes. A middle grouping labeled Evidence Gatherers / Enrichment Helpers. A single Evidence Packet Builder on the right feeding AI Reasoning. Add a small "missing facts" note to show gap visibility.

Alt text: Hand-drawn evidence-gathering layer showing source messages, prior state, local context, manual assists, diagnostic helpers, and workflow state being assembled into a bounded evidence packet before AI reasoning.

Prompt draft: Create a hand-drawn whiteboard explainer diagram with simple black marker lines, light highlights, and short labels. Show source messages, prior state, local context, manual/browser assist, diagnostic helper, and workflow state feeding Evidence Gatherers / Enrichment Helpers, then Evidence Packet Builder, then AI Reasoning. Include a small Missing Facts note. Use one clear idea. Do not show real source names, URLs, paths, screenshots, private data, or corporate architecture styling.

Safety notes: Keep all sources generic. Do not imply that all context search is universally implemented; use category labels rather than product-specific source names.

## 09-helper-and-maintenance-tools

Purpose: Show Telegram/dashboard as visible surfaces and helper/CLI tools as support tools underneath: intake, reconciliation, packet validation, audit inspection, diagnostics.

Filename: [diagrams/09-helper-and-maintenance-tools.png](diagrams/09-helper-and-maintenance-tools.png)

Placement: [SUPPORTING_TOOLS.md](../SUPPORTING_TOOLS.md).

Must-show: visible surfaces, helper CLI, source intake, reconciliation, packet validation, audit inspection, diagnostics, evidence packet.

Must-not-show: real command names, private paths, source systems, logs, screenshots, internal component names.

Suggested visual layout: Telegram and dashboard as two visible surface cards at the top. Underneath, a small toolbox labeled Helper CLI / maintenance tools. Toolbox callouts feed source intake, reconciliation, packet validation, audit inspection, diagnostics, and evidence packet.

Alt text: Hand-drawn whiteboard sketch showing Telegram and dashboard as visible surfaces above helper and maintenance tools that prepare and validate evidence packets.

Prompt draft: Create a hand-drawn whiteboard diagram with a small toolbox metaphor. Show Telegram and Dashboard as visible surfaces at the top. Under them, show Helper CLI / Maintenance Tools feeding Source Intake, Reconciliation, Packet Validation, Audit Inspection, Diagnostics, and Evidence Packet. Use short labels, black marker lines, and light highlights. Do not show real command names, private paths, source systems, logs, screenshots, or internal identifiers.

Safety notes: Keep all labels generic. Make helper tools visibly supportive, not authoritative.
