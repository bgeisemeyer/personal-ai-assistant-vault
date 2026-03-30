# AI Governance

This folder defines the active governance model for the framework.

## What This Governs
- Framework-wide rules and priorities
- How local context overrides are applied
- How skills relate to governance and templates
- How user defaults are set through onboarding and `.ai/runtime/User-Profile.md`

## Rule Priority
1. `Safety.md`
2. Explicit user instruction
3. Local context in the nearest `Index.md`
4. User defaults from `.ai/runtime/User-Profile.md`
5. Matching skill in `.ai/skills/`
6. `Global.md`

If two sources conflict, the higher rule wins. Lower layers should refine, not contradict, higher layers.

## Active Structure
- Reusable workflows live in `.ai/skills/`.
- Local topic or project context lives in the nearest `Index.md`.
- Reusable file structures live in `.ai/templates/`.
- Initial user configuration is captured through onboarding and `.ai/runtime/User-Profile.md`.

## Responsibilities
- `Global.md`: stable framework-wide defaults and working principles
- `Safety.md`: safety boundaries, escalation rules, and risky action rules
- `Skill-Model.md`: what skills are, when to create them, and how they interact with local context
- local `Index.md`: task- or folder-specific constraints, goals, permissions, and assumptions
- `.ai/runtime/User-Profile.md`: durable user-level preferences such as language, structure, and safety posture

## Purpose
- Keep work traceable.
- Keep context in files.
- Make handoff between different AI tools possible.

## How An AI Should Work Here
1. Read this folder first through `Index.md`.
2. Apply `Safety.md` before taking any risky action.
3. Read the nearest local `Index.md` before doing topic-specific work.
4. Use `.ai/runtime/User-Profile.md` for user-level defaults such as language and structure preferences.
5. Apply a matching skill only after governance and local context are clear.
6. Record ongoing work in local working files instead of relying on hidden session memory.

## Files
- [[.ai/governance/Global|Global.md]]
- [[.ai/governance/Safety|Safety.md]]
- [[.ai/governance/Skill-Model|Skill-Model.md]]
