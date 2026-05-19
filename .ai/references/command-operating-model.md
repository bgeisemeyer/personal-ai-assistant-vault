# Command Operating Model

## Purpose
- This reference defines the standard model for agent commands in the framework.
- It separates tool-specific wrappers, canonical command content, and optional references.
- It supports reusable command structures across multiple AI tools.

## Principle
- The actual command content lives canonically under `.ai/commands/`.
- Tool-specific wrappers should stay as small as possible.
- Larger, stable, or repeated prompt building blocks can be placed under `.ai/references/`.
- Small, correct, and flat structures are preferred.

## Standard Structure

### Canonical Content
- Location: `.ai/commands/`
- Example: `.ai/commands/New.md`
- Role:
  - contains the real working instruction
  - should be as tool-agnostic as possible
  - may reference governance and reusable references

### OpenCode Wrapper
- Location: `.opencode/commands/`
- Example: `.opencode/commands/new.md`
- Role:
  - provides the OpenCode slash command entry point
  - contains only a minimal wrapper
  - references `.ai/commands/...`

### References
- Location: `.ai/references/`
- Example: `.ai/references/vault-conventions.md`
- Role:
  - larger prompt building blocks
  - stable conventions
  - reusable decision models or operating logic

## Naming Conventions

### `.ai/commands/`
- File names use uppercase names following vault conventions.
- Examples:
  - `New.md`
  - `Topic-Start.md`
  - `Research-Start.md`

### `.opencode/commands/`
- File names use slash-command naming in lowercase.
- Examples:
  - `new.md`
  - `topic-start.md`
  - `research-start.md`

## Standard Patterns

### Pattern For Canonical Content
- Purpose and working instruction come first.
- Prefer tool-agnostic wording.
- Direct references to central rules are allowed.
- Do not duplicate long detail blocks inline without need.

Example:

```md
Read and follow the framework basics first:

@AGENTS.md
@.ai/governance/Index.md
@.ai/governance/Safety.md
@.ai/references/vault-conventions.md

Then work as follows:
- ...
```

### Pattern For OpenCode Wrappers
- Frontmatter with short description
- short entry line
- reference to the canonical content

Example:

```md
---
description: Initializes a new session with framework context
---

Run the standard startup for new sessions.

@.ai/commands/New.md
```

## Decision Logic For References

An additional reference under `.ai/references/` is useful when:
- a prompt block becomes longer
- the same block is needed in multiple commands
- the underlying operating model is stable and self-contained
- the canonical command content would otherwise become unnecessarily cluttered

Do not add an extra reference when:
- the content is small and one-off
- only a few lines are involved
- the extraction creates more complexity than value

## Decision Logic For Structure Changes

Default is flat:
- `.ai/commands/<Name>.md`

Only switch to a more complex structure when:
- a command needs multiple closely related files
- variants or extra building blocks are permanently needed
- a single file becomes too hard to maintain

Then a possible later form would be:
- `.ai/commands/<Name>/Command.md`
- `.ai/commands/<Name>/References.md`
- `.ai/commands/<Name>/Variants.md`

## Quality Criteria
- The wrapper does not duplicate the real command logic.
- Canonical content stays as tool-agnostic as possible.
- The structure remains small and understandable.
- Rules and conventions are not repeated unnecessarily across files.
- Reusable content lives in a stable place.
- The structure stays easy to continue for other AIs or agents.

## Anti-Patterns
- Duplicating the actual prompt logic across multiple wrappers
- Making one local tool syntax the canonical standard
- Building complex folder structures too early
- Extracting references even though the content is small
- Mixing naming conventions without a clear reason
