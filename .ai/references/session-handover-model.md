# Session Handover Model

## Purpose

- This reference defines the working model for `Session-Export` and `Session-Import`.
- Both names are intentionally familiar and practical.
- In substance, they are not technical import/export operations of an OpenCode session, but structured handovers for continuation in another session.

## Principle

- `Session-Export` creates an explicit handover file.
- `Session-Import` reads such a handover file and uses it as a structured re-entry point.
- In both commands, it must always be stated clearly that this is not a true technical export or import.
- The goal is continuity without silent dependence on chat history or implicit session memory.

## Storage Location

- Session exports are stored centrally under `.ai/runtime/session-exports/`.
- This folder is a runtime workspace for AI continuity and not a normal topic folder in the vault.

## File Format

- Format: Markdown (`.md`)
- Only Markdown files in the export folder count as importable session exports.

## File Names

- Standard pattern:
  - `Session-Export - <Session-Name> - DD.MM.YYYY HH-mm.md`
- The timestamp follows the vault convention, but uses `HH-mm` instead of `HH:mm` so the file name stays valid on Windows.
- The session name should stay short, readable, and unambiguous.
- Invalid Windows file name characters must be replaced or removed.

## Display In Selection Lists

- In numbered import lists, the prefix `Session-Export - ` is hidden.
- The displayed entry shows only the recognizable remainder without `.md`.
- Example:
  - `1. Vault Move - 12.05.2026 14-20`
  - `2. Eurover Vertical Slice - 12.05.2026 11-05`

## Minimum Content Of An Export File

Each export file contains at least:

- session name
- export timestamp
- original workspace path
- related topic or area
- reason for export
- goal
- current status
- decisions made
- open points
- next steps
- relevant files
- risks and assumptions
- recommended re-entry

## Export File Template

```md
# Session-Export: <Session-Name>

## Note
This is not a technical session export. This file is a structured handover for continuation in another session.

## Metadata
- Session-Name:
- Exported at:
- Original workspace path:
- Related topic / area:
- Reason for export:

## Goal
...

## Current Status
...

## Decisions
- ...

## Open Points
- ...

## Next Steps
1. ...
2. ...
3. ...

## Relevant Files
- `...`
- `...`

## Risks And Assumptions
- ...

## Recommended Re-entry
...
```

## Session-Export Behavior

- Always begin by stating that no true technical export is taking place.
- Form a default file name according to the naming pattern.
- Show the complete target path.
- Then ask the user whether the file name should be changed.
- Write the export file only after that response.
- If no useful session name can be derived, ask the user for a short session name.

## Session-Import Behavior

- Always begin by stating that no true technical import is taking place.
- Check the folder `.ai/runtime/session-exports/`.
- If the folder contains no Markdown files, state this clearly and abort the import.
- If files are present, list them in numbered form.
- Sort the list by recency by default, newest first.
- The selection is made by number.
- Then read the selected file and interpret it as a handover.

## Deletion Logic After Import

- After a successful import, ask whether the used export file should be deleted.
- Show the exact path before deletion.
- Delete only after explicit confirmation.
- Without explicit confirmation, the file stays in place.

## Privacy And Compression

- No full session transcript by default.
- Keep only the context that is actually needed for continuation.
- Include sensitive data only if it is truly necessary for further work.
- Unverified points or assumptions must be marked as such.

## Quality Criteria

- The export file is short enough to stay quickly readable.
- The export file is complete enough to make another session operational.
- Decisions and open points are clearly separated.
- Relevant files are named concretely.
- The next re-entry step is immediately actionable.
