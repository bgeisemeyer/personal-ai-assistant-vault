# Skill Model

## Purpose
- Reusable AI tasks are defined centrally as skills in `.ai/skills/`.
- Topic-specific context remains local in the relevant `Index.md`.
- Structures should allow multiple AI tools to continue work without losing context.

## Model
- **Skill** = reusable workflow, rules, and quality criteria for a task.
- **Local context** = folder-specific constraints, assumptions, and boundaries.
- **Log** = local traceability of work.
- **User profile** = stable user-level defaults from initial configuration.

## What Belongs Where
- Put stable cross-topic rules in governance.
- Put reusable task workflows in skills.
- Put copyable working structures in templates.
- Put topic-specific rules and assumptions in the local `Index.md`.
- Put durable user-wide defaults in `.ai/runtime/User-Profile.md`.

## When To Create A Skill
Create a new skill when:
1. The workflow is reusable across multiple topics.
2. The task has specific quality criteria or a repeated sequence.
3. The behavior should stay consistent across AI tools.

Do not create a skill when:
1. The rule is really governance.
2. The need is specific to one single topic.
3. A template or local context file is enough.

## Standard for New Topics
1. Create the folder.
2. Create files from the relevant template.
3. Add local context in `Index.md`.
4. Use an existing skill or add a new one.
5. Keep a local log.
6. Check whether the structure supports AI-agnostic continuation.

## Skill Application Rules
- Skills must follow `Safety.md`.
- Skills must follow the nearest local `Index.md`.
- Skills must respect `.ai/runtime/User-Profile.md` defaults unless local context overrides them.
- Skills should not assume tool-specific integrations unless explicitly documented.

## Priority in Conflicts
1. `Safety.md`
2. Explicit user instruction
3. Local context in `Index.md`
4. `.ai/runtime/User-Profile.md`
5. Matching skill in `.ai/skills/`
6. `Global.md`
