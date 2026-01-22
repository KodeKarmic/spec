# Copilot Instructions — Spec-Driven Development (Repo-wide)

## Prime directive
- Spec first. If behavior changes, update specs and tests before implementation.
- Do not invent requirements. If missing, ask targeted questions and propose explicit options.

## Required artifacts (keep in sync)
- Requirements: `docs/requirements/`
- Architecture: `docs/architecture/`
- Test cases + traceability: `docs/test-cases/`
- Executable tests: under `tests/`

## Traceability rules
- Every requirement must have:
  - A stable ID (e.g., FR-001, NFR-004)
  - Acceptance criteria
  - Linked test cases (TC-###)
- Maintain `docs/test-cases/TraceabilityMatrix.md` mapping:
  - FR/NFR -> TC -> automated test file(s) and test name(s)

## Definition of Done (DoD) for any change
- Updated relevant requirement(s) + acceptance criteria
- Updated or added test cases + traceability
- Updated architecture/ADR if design or constraints changed
- Implemented code
- Added/updated automated tests and they pass
- No TODOs for core logic unless explicitly approved in the spec

## Output conventions for Copilot
When asked to produce anything substantial, respond in this order:
1) Clarifying questions (only if necessary)
2) Plan (short, checklist)
3) Files to create/update (explicit paths)
4) The content changes

## Quality and safety constraints
- Prefer deterministic, testable behavior.
- Avoid hidden side effects. Log/telemetry must be intentional and documented.
- Handle errors explicitly; no silent failures.
