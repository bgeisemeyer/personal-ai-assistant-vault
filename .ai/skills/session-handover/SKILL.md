---
name: session-handover
description: >
  Performs structured Session-Export and Session-Import handovers.
  Uses central handover files under .ai/runtime/session-exports/,
  manages selection, clarification, and optional deletion approvals
  conservatively.
---

# Session Handover

## Purpose

This skill performs `Session-Export` and `Session-Import` as structured handover processes.

It exists to preserve or resume working context so that another session can continue without implicit memory.

A `Session-Export` or `Session-Import` is not a technical OpenCode session dump or restore, but a structured handover.

## References

Before working, consider these foundations:

- `.ai/governance/Skill-Model.md`
- `.ai/governance/Global.md`
- `.ai/governance/Safety.md`
- `.ai/references/session-handover-model.md`
- local context from the relevant `Index.md` if a clear topic relationship is recognizable during import

## Activation

Activate this skill for:

- `Session-Export`
- `Session-Import`
- structured session handover between sessions or AI tools
- resuming work after path changes, vault moves, or interrupted sessions

## Mode

- Default is pragmatic.
- Prefer small, clear, and easily resumable handovers.
- Switch to more thorough handling when:
  - deletion after import is possible
  - the session name is unclear
  - several export files are ambiguous
  - the content is sensitive
  - the topic relationship is unclear

## Working Method

1. Always state clearly at the beginning that no technical export or import is happening.
2. Determine the mode: `Export` or `Import`.
3. Use `.ai/references/session-handover-model.md` as the binding reference model.
4. Only use local special rules from the relevant `Index.md` when they matter for this handover.
5. Ask questions as soon as name, selection, topic relationship, or deletion is unclear.

## Export Mode

1. Derive a session name from the current context.
2. If no meaningful name can be derived, ask the user for a short session name.
3. Build a default file name according to the reference model.
4. Show the complete target path.
5. Ask the user whether the file name should be changed.
6. Only create the export file after the response.
7. Write the content according to the reference model.
8. Distill the working state so another session can continue without implicit memory.
9. Do not generate a full transcript by default.
10. After writing, confirm briefly where the export was stored.

## Import Mode

1. Check the folder `.ai/runtime/session-exports/`.
2. Consider only Markdown files (`*.md`).
3. If no importable files exist, state this clearly and do not continue the import.
4. If files exist, list them in numbered form.
5. Sort the list by recency by default, newest first.
6. In the display, hide the prefix `Session-Export - ` and the `.md` suffix.
7. Ask for the selection by number.
8. Read the selected file and interpret it as a handover.
9. If the file reveals a clear topic relationship, additionally use local context from the relevant `Index.md`.
10. Structure the re-entry clearly by goal, status, decisions, open points, and next steps.
11. After a successful import, ask whether the used export file should be deleted.

## Safety Rules

- Never claim that a real technical OpenCode export or import is happening.
- Never delete export files automatically.
- Always show the exact path before deletion.
- Delete only after explicit confirmation.
- When unclear, act conservatively and ask.

## Ask Before When

Questions are required when:

- no useful session name can be derived
- several export files are easy to confuse
- the user wants a different file name
- the export folder is missing or unexpectedly structured
- the topic relationship during import is unclear
- sensitive content must be included
- an export file should be deleted

## Output Format

### For Export

- short note about the handover nature
- suggested file name
- complete target path
- rename question
- short confirmation after creation

### For Import

- short note about the handover nature
- numbered list or empty-folder notice
- selection question by number
- short re-entry summary:
  - goal
  - status
  - decisions
  - open points
  - next steps
- then deletion question with the exact path

## Quality Criteria

- The handover is short enough to stay quickly readable.
- The handover is complete enough for operational continuation.
- Decisions, open points, and next steps are clearly separated.
- Relevant files are named concretely.
- The re-entry is immediately actionable.

## Limits

- No technical session restore
- No reconstruction of implicit memory
- No automatic repair of incomplete export files without asking
