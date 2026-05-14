# Synthetic Command Examples

These commands are generic examples for the public-safe case study. They are not tied to a live system.

```text
/sync
```
Refresh external signal reconciliation and report what would change. A sync report is not the same thing as an applied lifecycle action.

```text
/review
```
Show the current review queue with items needing facts, assessment, decision, clarification, or cleanup.

```text
/details ITEM-123
```
Show compact details: summary, known facts, missing facts, ambiguity flags, latest assessment, allowed actions, and audit preview.

```text
/evaluate ITEM-123
```
Build a bounded evidence packet and request an AI assessment. The assessment does not mutate runtime state.

```text
/approve ITEM-123
```
Apply an explicit human decision to mark the item ready for action, if the current state allows it.

```text
/park ITEM-123
```
Apply an explicit human decision to defer the item while keeping it visible.

```text
/clarify CLAR-001
```
Resolve an ambiguity before lifecycle mutation.

```text
/close ITEM-123
```
Apply an explicit human decision to close the item as not worth further action.
