# Skill Decision Logic

## Purpose
- This reference helps decide whether a new request should be modeled as a skill, a reference, local context, or a topic-adjacent file.
- It supports both new skills and maintenance of existing skills.

## Principle
- Not every recurring requirement automatically deserves a skill.
- Skills are meant for reusable workflows, rules, and quality criteria.
- Local specifics should stay in the topic folder.

## Decision Order

### 1. Is the request recurring?
- If no, it is usually not a skill.
- Then a local note, one-off working file, or direct topic context is often better.

### 2. Does the task need a stable workflow?
- If yes, a skill is probably appropriate.
- If no, a reference or local note is often enough.

### 3. Must the task be handled consistently across multiple AIs or tools?
- If yes, prefer a skill or a reference.
- If no, local context may be enough.

### 4. Is the logic central or topic-specific?
- Central, reusable logic belongs in a skill.
- Topic-specific rules belong in `Index.md` under local context.

### 5. Does the task need extra models or decision trees?
- If yes, create one or more references under `.ai/references/`.
- Keep skills and references intentionally separate.

### 6. Are text blocks or operational templates better placed near the topic?
- If yes, create a topic-adjacent file in the relevant folder.
- Example: `Email-Templates.md`.

## Forms Compared

### Skill
- Suitable for reusable workflows.
- Contains activation, working method, safety rules, ask-before rules, and output format.

### Reference
- Suitable for data models, decision logic, source overviews, and cross-account or cross-system conventions.
- Stabilizes complex skills without overloading `SKILL.md`.

### Local Context In `Index.md`
- Suitable for topic, goal, tone, allowed tools, concrete paths, sources, and exceptions.
- Intentionally stays local.

### Topic-Adjacent File
- Suitable for templates, text snippets, or directly usage-near content.
- Lives close to the place of use.

## Typical Decisions

### A Skill Is Appropriate When
- the task is recurring
- the workflow is clear
- reusable safety rules are needed
- consistent handling across multiple AIs or tools is needed

### An Integration Or MCP Skill Is Appropriate When
- there is an external or local technical dependency
- the workflow depends on accounts, servers, or tools
- early technical availability checks are needed
- clear failure communication is needed when the technical basis is missing

### Special Safety Logic Is Needed When
- deletions or bulk deletions are involved
- risky write operations are involved
- steps are irreversible or difficult to undo

In those cases, the skill must contain conservative approval logic, especially prior listing and explicit confirmation before deletion.

### A Reference Is Appropriate When
- a data model is needed
- a decision tree is needed
- a source collection is needed
- cross-account or cross-system conventions are needed

### Local Context Is Appropriate When
- the tone is topic-specific
- paths are concrete and local
- sources are concrete and local
- thematic exceptions exist
- local permissions or prohibitions exist

### A Topic-Adjacent File Is Appropriate When
- templates are needed
- text snippets are needed
- operational lists are needed
- usage-near working artifacts are needed

## Pragmatic Or Thorough

### Pragmatic
- default mode
- prefers small, correct structures
- suitable for clear, low-risk tasks

### Thorough
- suitable for safety-relevant work, complex integrations, MCP usage, multi-account logic, risky actions, or unclear boundaries
- checks architecture, reference needs, and ask-before rules more deeply

## Anti-Patterns
- creating a skill for one-off or overly local logic
- putting too many topic-specific rules into a skill
- missing a reference despite a complex data model
- centralizing topic-adjacent templates that belong near their usage context
- expanding existing skills without first checking whether they should be split or supported by references

## Review Questions For Existing Skills
- Is activation clear?
- Is the workflow stable and reusable?
- Are there unnecessary overlaps with `Global.md`, `Index.md`, or references?
- Is a reference missing because the skill carries too much domain logic?
- Is an ask-before rule missing?
- Is a useful output format missing?
