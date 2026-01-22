---
applyTo: "docs/test-cases/**/*.md,docs/test-cases/*.md,tests/**/*"
---

# Test Case and Test Generation Rules

## Goal
Turn requirements into verifiable tests (human-readable + automated).

## Test case format (docs)
Each test case must have:
- ID: TC-###
- Linked requirements: FR-### and/or NFR-###
- Preconditions
- Steps
- Expected results
- Data variations (at least 1 negative case)
- Notes (risk/coverage gaps)

## Coverage expectations
- For every FR: at least
  - 1 happy path
  - 1 validation/error path
  - 1 boundary/edge path (where applicable)
- For NFRs: specify measurement test or check (load, security, etc.) even if not automated now.

## Traceability
- Update `docs/test-cases/TraceabilityMatrix.md`:
  - Requirement ID -> Test case ID -> Automated test reference (file + test name)
- If automation is not added, mark as `MANUAL` with rationale.

## Automated tests
- Prefer deterministic tests (no sleeps, no real network calls).
- Use fakes/mocks for external dependencies.
- Name tests to reflect requirement IDs (e.g., `FR_012_CreatesProject_WhenValidInput`).
