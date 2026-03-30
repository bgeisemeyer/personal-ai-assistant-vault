# Insights

## Summary
- V1 focuses on framework structure, governance, templates, onboarding, and generic skills.

## Important Points
- File-based context is the core mechanism for AI-agnostic continuation.
- Governance and templates should be logically separated but can live together under `.ai/`.
- Language defaults belong in configuration, not as hard-coded user assumptions.

## Decisions
- Decision: Place governance, templates, onboarding, references, and skills under `.ai/`.
  - Rationale: These files primarily serve AI operation and do not need to remain visible in the normal Obsidian sidebar.
  - Evidence: [[Log#30.03.2026 09:04]]
