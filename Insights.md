# Insights

## Summary
- V1 should focus on framework structure, governance, templates, onboarding, and generic skills.
- Tool-specific runtime integrations are intentionally deferred.

## Important Points
- File-based context is the core mechanism for AI-agnostic continuation.
- Governance and templates should be logically separated but can live together under `.ai/`.
- Language defaults belong in configuration, not as hard-coded user assumptions.

## Decisions
- Decision: Place governance, templates, onboarding, references, and skills under `.ai/`.
  - Rationale: These files primarily serve AI operation and do not need to remain visible in the normal Obsidian sidebar.
  - Evidence: [[Log#30.03.2026 09:04]]
- Decision: Exclude email, CalDAV, ACA, training-specific content, and OpenCode runtime files from V1.
  - Rationale: V1 should stay generic, portable, and publication-ready.
  - Evidence: [[Log#30.03.2026 09:04]]
