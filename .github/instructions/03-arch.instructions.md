---
applyTo: "docs/architecture/**/*.md,docs/architecture/*.md"
---

# Architecture Documentation Rules (C4 + ADR)

## Goal
Explain “how the system works” enough that implementation choices are constrained and reviewable.

## Minimum architecture set
- `Overview.md`: goals, scope, constraints, key quality attributes (from NFRs).
- C4 docs: Context, Container, Component (as applicable).
- ADRs: one per meaningful decision.

## ADR format (required)
- Title
- Status: Proposed / Accepted / Deprecated
- Context
- Decision
- Consequences (positive/negative)
- Alternatives considered

## Consistency checks
- Every architectural component must map back to one or more requirements.
- If a requirement introduces a new constraint, reflect it in Overview + relevant ADR.

## Anti-patterns
- Hand-wavy diagrams with no ownership of data flow or failure modes.
- Decisions with no trade-offs documented.
