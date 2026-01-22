---
applyTo: "src/**/*,tests/**/*"
---

# Implementation Rules (Spec-driven)

## Prime directive
- Implement ONLY what is specified by FR/NFR + accepted ADRs.
- If the spec is ambiguous, do not guess: propose 2–3 options and request a decision.

## Coding workflow
1) Identify impacted requirements (FR/NFR IDs)
2) Identify impacted tests (TC IDs)
3) Make the smallest change that satisfies acceptance criteria
4) Add/adjust automated tests
5) Update traceability matrix

## Review checklist for code changes
- Input validation and error handling match acceptance criteria
- No breaking changes without spec update
- Logging is purposeful and does not leak secrets
- Performance/security constraints respected (cite NFR IDs in comments or PR description)

## Output expectations
When generating code, always include:
- File list
- Build/test commands to run
- Notes about any remaining manual verification (if unavoidable)
