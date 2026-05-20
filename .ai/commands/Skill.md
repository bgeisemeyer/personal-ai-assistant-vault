Use the skill `skill-development` as the governing workflow for this task.

@.ai/skills/skill-development/SKILL.md
@.ai/governance/Skill-Model.md
@.ai/references/skill-decision-logic.md
@.ai/references/skill-quality-criteria.md

Interpret the input like this:

- The first passed argument is the skill name.
- The remaining text is the request for creation, extension, maintenance, or restructuring.

Then work as follows:

- First check whether a skill with this name already exists under `.ai/skills/<skill-name>/SKILL.md`.
- If the skill exists, treat the request by default as an update, extension, or maintenance task for that existing skill.
- If the skill does not exist, treat the request by default as development of a new skill.
- Briefly check whether a reference, local context, or topic-adjacent file would be more appropriate than a skill.
- Prefer small, correct changes and avoid unnecessary skill inflation.
- Reuse existing references and similar skills when helpful.
- Ask questions only when the request, the skill cut, the boundary, or risky effects are unclear.
- If the request is clear enough, implement the required files directly.
- Respond briefly, precisely, and with the result first.
