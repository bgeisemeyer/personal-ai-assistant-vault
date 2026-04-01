# Architecture

## Goal
Define a vault framework that can be continued by different AI tools without depending on the memory of one chat session.

## Core Mechanisms
- Global framework rules live in `.ai/governance/`.
- Reusable workflows live in `.ai/skills/`.
- Supporting references live in `.ai/references/`.
- Initial configuration lives in `.ai/onboarding/` and `.ai/runtime/User-Profile.md`.
- Local working context remains in the relevant topic or project `Index.md`.

## Continuity Model
- Rules are stored in files.
- Status is stored in files.
- Decisions are stored in files.
- Templates enforce repeatable structure.
- Skills define reusable operating logic.

## Language Model
- Framework default: English.
- User language: configured via `.ai/runtime/User-Profile.md`.
- Local overrides: allowed in the nearest `Index.md`.

## Current Operating Model
- The current baseline is a single-user vault model.
- Session context assumes one active user perspective at a time.
- User-wide defaults are stored in `.ai/runtime/User-Profile.md`.

## Shared Vault Direction
- Shared or multi-user vault support may become a future expansion of the framework.
- It is not part of the current baseline model.
- The preferred direction, if added later, is a shared vault with exactly one active user per session.
- In that model, the session should identify the active user before normal work begins.

## Mixed Private And Shared Areas
- A vault that is partly private and partly shared is not the recommended default model.
- If multiple people can access the same vault, the framework should not treat that vault as a secure privacy boundary between those people.
- The preferred baseline remains either a private vault or a fully shared vault.

## V1 Boundaries
- No runtime-specific launcher layer.
- No personal data or example data in the framework scaffold.
- No official shared-vault or multi-user operating model yet.
