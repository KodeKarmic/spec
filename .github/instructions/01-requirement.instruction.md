---
applyTo: "docs/requirements/**/*.md,docs/requirements/*.md"
---

# Requirements Authoring Rules (PRD/SRS/NFR)

## Goal
Produce requirements that are implementable, testable, and traceable.

## Format rules
- Every functional requirement must have:
  - ID: FR-###
  - Title
  - Description
  - Acceptance Criteria (Given/When/Then preferred)
  - Out of Scope (explicit, if relevant)
  - Edge cases / failure modes
- Every non-functional requirement must have:
  - ID: NFR-###
  - Metric + target (latency, throughput, availability, cost, security, privacy, etc.)
  - Measurement method (how we verify)
- Define terms in `docs/requirements/Glossary.md`.

## Anti-patterns (avoid)
- Vague words: “fast”, “intuitive”, “secure” without metrics.
- Mixing design decisions into requirements (those go to ADRs unless required by constraints).
- Implicit scope. If it matters, write it.

## Required outputs
- Update `docs/requirements/Decisions.md` with open questions + chosen options.
- If any architectural constraint emerges, add an ADR stub under `docs/architecture/ADR/`.
