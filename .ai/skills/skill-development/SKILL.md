---
name: skill-development
description: >
  Develops new skills for the framework and maintains existing ones.
  Checks suitability, architecture, and reference needs first, asks
  focused questions when needed, and then delivers a full draft for the
  skill, references, and supporting files.
---

# Skill Development

## Purpose

This skill develops and maintains skills for the framework skill system.

It helps with:
- new skills
- refactoring existing skills
- splitting or merging skills
- deciding between a skill, a reference, local context, or a topic-adjacent file
- clean integration of new MCPs, tools, and working models into the skill system

## References

Before working, consider these foundations:
- `.ai/governance/Skill-Model.md`
- `.ai/governance/Global.md`
- `.ai/references/skill-decision-logic.md`
- `.ai/references/skill-quality-criteria.md`
- existing skills under `.ai/skills/`
- existing references under `.ai/references/`
- local context in `Index.md`, if it already exists for the target area

## Activation

Activate this skill when:
- a new skill is requested
- an existing skill should be extended, unified, slimmed down, or split
- the boundary between skill, reference, local context, or topic-adjacent file is unclear
- a new MCP, tool, or process integration should enter the skill system

## Working Modes

### Pragmatic
- default mode
- prefers small, correct structures
- suitable for clear, low-risk requests

### Thorough
- suitable for safety-relevant, integration-near, or structurally critical topics
- checks reference needs, ask-before rules, and architecture more deeply

### Mode Selection
- Default is `pragmatic`.
- Switch to `thorough` or suggest it when:
  - safety relevance is involved
  - sending, deletion, downloads, or other risky actions are involved
  - MCP integration is involved
  - multi-account, multi-folder, or multi-system logic is involved
  - a new data model is involved
  - the central-vs-local boundary is unclear

## Working Method

1. Clarify the goal, problem, and expected value.
2. Choose the appropriate mode: pragmatic or thorough.
3. Check whether the request should really be modeled as a skill.
4. Determine the skill type.
5. Define the architecture split:
   - `SKILL.md`
   - `.ai/references/...`
   - local context in `Index.md`
   - topic-adjacent files
6. Define safety rules and ask-before requirements.
7. For MCP- or tool-near skills, include early technical availability checks by default.
8. Define the output format.
9. Check existing skills and references for duplication or gaps.
10. Ask open questions.
11. Then deliver the full draft.

## Default For Deletion Actions

- If a skill could delete files, elements, emails, entries, or other artifacts, the default rule is:
  - clearly list what would be deleted first
  - then obtain explicit confirmation
  - only then delete
- The skill must not perform deletions implicitly.
- For bulk deletions, the prior list is especially important.

## Skill Suitability Check

Before every draft, check:
- Is the task recurring?
- Does it have a stable workflow?
- Does it need reusable rules or quality criteria?
- Must it be handled consistently across multiple AIs or tools?

If the answer is mostly no, do not design a skill by default. Suggest an alternative such as:
- a reference under `.ai/references/`
- local context in `Index.md`
- a topic-adjacent file
- a simple working note

## Skill Types

### Process Skill
- for standardized workflows with clear steps and documentation rules

### Domain Skill
- for domain-specific working logic with sources, models, or specialized rules

### Integration Skill
- for MCP-, tool-, or system-near workflows with safety and approval logic
- for such skills, an early technical availability check is standard

### Maintenance Skill
- for consistency, small corrections, structure maintenance, and governance-near work

### Tool Skill
- for concrete external or local tools with setup, fallback, or usage logic

### Hybrid Skill
- when several types need to be combined meaningfully

## Architecture Split

### In `SKILL.md`
- reusable workflow
- activation
- safety rules
- ask-before rules
- output format
- references to supporting materials
- for integration or MCP skills: early technical availability checks and clear failure communication
- for potential deletions: prior listing of affected objects and explicit confirmation

### In `.ai/references/`
- data models
- decision logic
- source collections
- account- or system-crossing conventions

### In local `Index.md`
- topic and goal
- local tone
- concrete sources
- concrete paths
- approvals and exceptions

### In topic-adjacent files
- templates
- sample texts
- operational lists
- files needed directly at the usage context

## Maintaining Existing Skills

When an existing skill should be changed, check:
- Is activation clear?
- Are there overlaps with `Global.md`, local `Index.md`, or references?
- Is a reference missing because the skill carries too much domain logic?
- Is a useful output format missing?
- Is an ask-before rule missing?
- Has the skill grown too large?

Possible outcomes:
- sharpen
- slim down
- extract references
- split
- merge

## Ask Before Finalizing When
- it is unclear whether a skill is appropriate at all
- several skill cuts are plausible
- it is unclear what belongs centrally and what belongs locally
- safety or approval logic is critical
- integrations or MCP usage are still unclear
- deletions or bulk deletions are planned

## Default For MCP And Tool Skills

- If a skill depends on MCPs, external servers, local services, or special tools, an early availability check is standard.
- That check happens before deeper content work and before follow-up clarification loops.
- If the technical basis is missing, the skill should:
  - state that clearly
  - not pretend to continue substantive work
  - avoid clarification chains that only make sense once the connection works

Typical cases:
- MCP not connected
- server not reachable
- required tool not available
- required account or resource not accessible

## Default For Risky Actions

- For potentially irreversible actions, conservative behavior is mandatory.
- Especially for deletions:
  - show the list first
  - then obtain confirmation
  - then execute

## Standard Output

Provide output in three parts:

### 1. Concept In Prose
- understanding of the problem
- whether a skill is appropriate or an alternative is better
- chosen skill type
- selected mode: pragmatic or thorough
- architecture decision

### 2. Structured Specification
- skill name
- purpose
- skill type
- mode
- required references
- expected local files
- safety rules
- ask-before rules
- output format
- file proposal

### 3. Full Draft
- `SKILL.md`
- required references
- optional proposals for local files or topic-adjacent templates

## Quality Criteria

Check every draft against `.ai/references/skill-quality-criteria.md`.

Especially important:
- no unnecessary centralization
- no unnecessary duplication
- clear separation of skill, reference, and local context
- prefer small, correct solutions
- preserve AI-agnostic continuity

## Limits

- Do not create skill inflation.
- Do not copy global rules into new skills unnecessarily.
- Do not centralize local specifics without need.
- Do not only polish wording when the structural problem lies elsewhere.
- Structure and architecture matter more than cosmetic formatting.
