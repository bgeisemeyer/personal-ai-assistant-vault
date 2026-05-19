---
name: command-development
description: >
  Develops and maintains reusable agent commands for the framework.
  Separates tool-specific wrappers, canonical command content, and
  optional references while preserving tool-agnostic structure.
---

# Command Development

## Purpose

This skill develops and maintains agent commands for the framework.

It helps with:
- new slash commands
- maintenance of existing command structures
- consistent separation of wrappers and canonical command files
- deciding between `.ai/commands/`, `.opencode/commands/`, and `.ai/references/`
- tool-agnostic structure for multiple AI tools or agents

## References

Before working, consider these foundations:
- `.ai/governance/Skill-Model.md`
- `.ai/governance/Global.md`
- `.ai/references/command-operating-model.md`
- existing files under `.ai/commands/`
- existing files under `.opencode/commands/`
- existing references under `.ai/references/`
- local context in `Index.md`, if the command is meant for a specific topic area

## Activation

Activate this skill when:
- a new agent command is requested
- an existing command should be extended or unified
- a tool-agnostic command structure is needed for multiple AI tools
- the boundary between wrapper, canonical command content, and reference is unclear
- `.ai/commands/` or `.opencode/commands/` need maintenance or refactoring

## Mode

- Default mode is pragmatic.
- Prefer small, correct structures.
- Prefer flat structure by default.
- Only expand to folders or extra references when the need is clear.

## Suitability Check

Before designing a command, check:
- Is the command meaningfully reusable?
- Does the command have a stable purpose?
- Should multiple AI tools or agents use it consistently?
- Would a simple local note be enough instead?

If the answer is mostly no, prefer an alternative such as:
- a topic-local file
- a reusable reference under `.ai/references/`
- a local note
- an extension of an existing command

## Working Method

1. Clarify purpose, value, and trigger of the command.
2. Check whether a new command is needed or an existing one should be extended.
3. Clarify tool reach:
   - OpenCode only
   - OpenCode plus other tools later
   - intentionally tool-agnostic
4. Define the file split:
   - canonical content under `.ai/commands/`
   - OpenCode wrapper under `.opencode/commands/`
   - optional references under `.ai/references/`
5. Prefer flat structure by default:
   - `.ai/commands/<Name>.md`
   - `.opencode/commands/<slash-name>.md`
6. Check the size of the canonical command content:
   - if small and stable, keep it in `.ai/commands/<Name>.md`
   - if larger or reused often, extract references
7. Keep wrappers intentionally thin:
   - no duplicated command logic
   - only tool-specific entry behavior
   - reference the canonical file
8. Apply naming conventions:
   - `.ai/commands/` uses uppercase names following vault conventions
   - `.opencode/commands/` uses lowercase slash-command naming
9. Check existing commands for duplication or easier extension paths.
10. Ask questions if the split is unclear.
11. Then provide the full design for all required files.

## Standard Architecture

### Canonical Command Content
- lives under `.ai/commands/`
- contains the actual working instruction
- should be as tool-agnostic as possible
- may reference reusable references

### OpenCode Wrapper
- lives under `.opencode/commands/`
- stays as small as possible
- contains only the OpenCode-specific entry layer
- references the canonical content under `.ai/commands/`

### References
- live under `.ai/references/`
- contain longer, stable, or reusable prompt building blocks
- should only be extracted when they provide clear reuse or simplification

## Ask Before Finalizing When
- the command purpose is unclear
- several slash names seem plausible
- it is unclear whether an existing command should be extended instead
- it is unclear whether the command should stay tool-agnostic or OpenCode-specific
- local topic conventions matter
- the command triggers, prepares, or automates risky actions
- deletions or bulk removals are involved

## Safety Rules
- Do not make unrequested mass changes to existing commands.
- Do not make destructive changes without clear instruction.
- Before deletions or bulk deletions, always:
  - list affected files or commands
  - obtain explicit confirmation
  - only then delete
- For risky or irreversible command purposes, prefer conservative approval logic.
- Do not copy global rules into every command unnecessarily.

## Output Format

Provide output in three parts:

### 1. Decision
- Is a new command justified?
- Why create a new command, extend an existing one, or choose an alternative?
- Which file split was chosen?

### 2. Structure
- slash name
- canonical file name
- required wrappers
- required references
- open risks or questions

### 3. Full Draft
- `.ai/commands/...`
- `.opencode/commands/...`
- optional `.ai/references/...`

## Quality Criteria
- clear separation between wrapper and canonical content
- no unnecessary duplication
- small, correct structure preferred
- tool-agnostic continuity preserved
- stay flat first and only grow when needed

## Limits
- No skill inflation through trivial single-purpose commands.
- No unnecessary centralization of local special cases.
- No extraction of large references when the content can stay small.
- No complex command folder structures without clear need.
- Do not overload wrappers with the actual domain logic.
