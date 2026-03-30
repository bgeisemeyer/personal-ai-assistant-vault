# Architecture

## Goal
Define a vault framework that can be continued by different AI tools without depending on the memory of one chat session.

## Core Mechanisms
- Global framework rules live in `.ai/governance/`.
- Reusable workflows live in `.ai/skills/`.
- Supporting references live in `.ai/references/`.
- Initial configuration lives in `.ai/onboarding/` and `User-Profile.md`.
- Local working context remains in the relevant topic or project `Index.md`.

## Continuity Model
- Rules are stored in files.
- Status is stored in files.
- Decisions are stored in files.
- Templates enforce repeatable structure.
- Skills define reusable operating logic.

## Language Model
- Framework default: English.
- User language: configured via `User-Profile.md`.
- Local overrides: allowed in the nearest `Index.md`.

## V1 Boundaries
- No runtime-specific launcher layer.
- No built-in email or calendar automation.
- No personal data or example data in the framework scaffold.
