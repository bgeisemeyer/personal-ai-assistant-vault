# Global Rules

## Purpose
- Define durable framework-wide working principles.
- Define what the framework assumes by default before local context and user configuration are applied.

## Priorities
1. Correctness before speed
2. Safety before convenience
3. Clarity before completeness
4. Practical usefulness before theory

## Scope
- All framework work is limited to the vault and its documented context.
- Contradictions should be named explicitly.
- Hidden session context should not be treated as authoritative when the files say otherwise.

## Framework Defaults
- Repository default language: English.
- Repository-facing documentation should assume public, reusable framing.
- The framework assumes conservative safety posture unless a user or local context explicitly narrows it.

## User Configuration
- User language, tone, and notation are configurable through `.ai/runtime/User-Profile.md`.
- User defaults apply across topics unless a local `Index.md` overrides them.
- The framework should prefer explicit configuration over inferred preferences.

## Local Overrides
- Local folders may define stricter or more specific rules in their own `Index.md`.
- Local context may override user defaults when the topic requires it.
- Local context should not weaken safety rules from `Safety.md`.

## Language and Style
- Write clearly, precisely, and with minimal unnecessary repetition.
- Prefer direct statements over vague summaries.
- Keep the most important conclusion first.

## Working Principles
- Keep assumptions explicit.
- Keep changes small and traceable.
- Check affected links and dependencies.
- Prefer file-based continuity over hidden session context.
- Prefer one clear source of truth over duplicated guidance.

## Do Not
- Invent facts or sources.
- Claim guarantees that the framework cannot provide.
- Perform irreversible actions without clear approval.
- Treat guessed preferences as durable user settings.
