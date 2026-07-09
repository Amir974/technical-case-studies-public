# Examples

The examples below are reconstructed at the pattern level. They focus on the product decisions, not on the original assignment prompts or submitted materials.

## Example A - FARO: Progressive Value Under Incomplete Coverage

### Assignment Pattern

The first example pattern comes from a data-security style problem. The system is trying to surface risk before it has full coverage of the environment. The obvious pressure is speed: how quickly can it scan, classify, and show useful results? But the deeper product problem is trust. If the system only sees part of the picture, what can it responsibly tell the user? What actions are safe? What must be labeled as incomplete?

The product concept I used was **FARO - First-wave Assisted Risk Orientation**.

The name gave me a short presentation hook: a lighthouse does not remove fog or ensure safe passage. It gives ships a fixed point of orientation when visibility is limited.

That was the product metaphor: do not pretend the first wave of coverage is complete; help the user orient under uncertainty.

### Trap

The trap was treating visible scan speed as the main product value. Speed matters, but speed without trust can create false confidence. The harder product work was deciding how the product should communicate confidence, prioritize what mattered, and route users toward safe action when coverage was still incomplete.

### Core Reframe

- **Not:** How do we show a complete report faster?
- **Instead:** How do we create useful, confidence-labeled orientation before coverage is complete?

The product work was about controlling the promise. A weaker answer would make the early result sound complete. A stronger answer makes incompleteness visible and still creates value through orientation, prioritization, and safe next actions.

### Product Decisions

This example forced several concrete PM decisions:

- What counts as a confirmed signal versus a likely signal?
- How should the product label coverage gaps without making the experience feel broken?
- Which actions are safe when coverage is partial?
- Which recommendations should be blocked until there is stronger evidence?
- How should the user move from first-wave orientation to deeper investigation?

### Evidence States

A progressive-value product can expose evidence states instead of hiding them:

- **Observed:** directly supported by available evidence.
- **Inferred:** reasonable but dependent on assumptions or partial signals.
- **Missing:** necessary to make a stronger recommendation but not currently available.
- **Conflicting:** sources disagree or imply different interpretations.
- **Stale:** evidence exists but may no longer describe the current state.

### Coverage, Confidence, And Safe Action

The product should separate coverage from confidence:

- **Coverage** describes how much of the relevant surface has been evaluated.
- **Confidence** describes how strongly the available evidence supports a conclusion.
- **Action safety** describes what the user should or should not do given that combination.

High confidence with narrow coverage is not the same as broad confidence. Low coverage should shape the recommendation, the visual language, and the allowed next action.

The product can create value before full coverage by recommending safe, bounded actions:

- act now when evidence is strong and the action is reversible or low-risk;
- prioritize human review when evidence is partial but the potential impact is high;
- request more evidence when the missing information would change the decision;
- monitor when the signal is weak, stale, or not yet actionable;
- block automation when the system cannot justify a safe next step.

### MVP / Later / Non-Goals

The MVP should make uncertainty usable:

- evidence-state labels;
- coverage and confidence shown separately;
- a short reason for each recommendation;
- safe next-action categories;
- visible gaps that would improve confidence;
- a review queue that prioritizes high-impact uncertainty.

Later capabilities could include richer source reconciliation, team-specific policies, historical learning, explainability improvements, integrations into existing workflows, and stronger automation once evidence quality is strong enough.

The product should not imply total visibility, hide missing evidence, automate high-risk decisions without review, or treat a confidence score as a substitute for product judgment.

### What I Would Defend Live

I would defend the choice to create first-wave orientation rather than a premature complete report. I would expect questions about false positives, partial scans, and user trust, so the live defense would center on confirmed versus likely signals, visible coverage gaps, blocked recommendations, and the path from initial orientation to deeper investigation.

The value was not pretending to know everything. The value was helping the user make a better next decision despite incomplete coverage.

## Example B - Standards-To-Roadmap Mapping

### Assignment Pattern

The second example pattern comes from a technical platform assignment. The input is a standard, framework, or capability expectation. The tempting move is to treat the standard as a backlog: find gaps, list features, and call it a roadmap.

That is not product judgment. A standard describes a world of possible requirements. A roadmap chooses which product bets are worth making for specific customers, constraints, and sequencing logic.

### Trap

The trap was over-abstracting the standard into a neat capability inventory and then treating every gap as a priority. Capability gaps are inputs. They do not become roadmap items until they are tested against customer value, feasibility, sequencing, evidence quality, trust, and compliance needs.

### Core Reframe

- **Not:** Which standard gaps exist?
- **Instead:** Which gaps represent valuable, feasible, and defensible product opportunities, and in what order should they be pursued?

This is where AI is useful but dangerous. It can help summarize the standard, extract capability language, and suggest gap taxonomies. But it can also make every gap sound equally important. The PM work is to decide which gaps should become product bets, which should become evidence or export improvements, which should remain later, and which should be ignored.

### Product Decisions

This example forced a different set of decisions:

- Which capabilities are table stakes versus differentiators?
- Which gaps create user value, and which only create checklist completeness?
- Which gaps are evidence, trust, or compliance inputs rather than product priorities?
- Which work improves customer trust through better evidence, reporting, or attestation?
- Which opportunities are feasible within the likely engineering and UX constraints?
- Which sequence creates a coherent roadmap instead of a feature pile?

### Pattern

```text
external standard
-> capability map
-> gap classes
-> opportunity classes
-> prioritization logic
```

![Roadmap Filter diagram showing an external standard translated through capability mapping, gap classes, and a PM translation filter into focused roadmap bets.](assets/diagrams/04-roadmap-filter.png)

*A standard is input, not the roadmap. The PM translation filter turns many possible gaps into focused roadmap bets, including the choice not to build.*

### Capability Map

A pattern-level capability map might include:

- evidence collection;
- state assessment;
- gap explanation;
- workflow routing;
- policy mapping;
- reporting and auditability;
- integration with existing systems;
- exception handling;
- human approval for high-impact actions.

The map is not a commitment list. It is a translation layer between external requirements and possible product capabilities.

### Gap Classes

Useful gap classes include:

- **Visibility gaps:** the user cannot see the relevant state or evidence.
- **Workflow gaps:** the user can identify a problem but cannot route or resolve it efficiently.
- **Trust gaps:** the system cannot explain why a state or recommendation matters.
- **Control gaps:** the user lacks policy, approval, or exception handling.
- **Integration gaps:** the product does not connect cleanly to systems where work already happens.
- **Validation gaps:** the product cannot yet support the proof burden required for higher-risk automation.

### Product Opportunity Classes

Not every gap is equally product-relevant. Useful opportunity classes include:

- gaps that create buyer urgency;
- gaps that reduce repeated manual work;
- gaps that improve trust or explainability;
- gaps that unlock adjacent workflows;
- gaps that differentiate the product without overextending the platform;
- gaps that are better handled through partners, documentation, or services.

Opportunity classes convert a technical map into product strategy. They ask whether a gap matters enough, repeats enough, and fits the product's durable advantage well enough to earn roadmap weight.

### Prioritization Logic

The roadmap should weigh:

- customer pain and frequency;
- severity of the unmanaged risk;
- technical feasibility;
- proof burden;
- integration cost;
- implementation sequencing;
- sales or adoption leverage;
- risk of building a checklist feature with weak product pull.

The output is a decision set:

- **Build now:** high customer value, clear feasibility path, strong fit with product strategy.
- **Build later:** useful but dependent on adoption, data quality, technical readiness, or workflow maturity.
- **Enable:** better solved through docs, configuration, services, or partner motion.
- **Do not build:** too bespoke, too speculative, too far from the product's advantage, or too risky to automate.

### What I Would Defend Live

I would defend the roadmap as a set of product bets, not a standard converted into tasks. The live discussion would need to test why some gaps became product priorities, why some remained evidence or compliance inputs, and why the sequence created more customer value and trust than a broader checklist implementation.

The private assignment details are not needed for this practice case study to demonstrate the judgment.

[Back to case study README](README.md) · [Back to repository index](../../README.md)
