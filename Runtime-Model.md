# Runtime Model

## Purpose

This document defines the difference between framework files and runtime files in a real vault.

## Framework vs Runtime

### Framework Files
Framework files are shipped with the repository.

They include:
- `.ai/governance/`
- `.ai/skills/`
- `.ai/references/`
- `.ai/onboarding/`
- `.ai/templates/`
- root documentation files

### Runtime Files
Runtime files are created in the actual user vault during setup or later operation.

They include:
- `.ai/runtime/User-Profile.md`
- `Migration/` when an existing vault is being assessed or migrated
- topic-specific `Index.md`, `Log.md`, and other working files created from templates

## User Profile Location

The official runtime location for user-wide defaults is:

` .ai/runtime/User-Profile.md `

This keeps the file:
- close to the AI framework
- hidden from normal Obsidian sidebar usage
- separate from normal human-facing vault content

## Template vs Instance

- Template: `.ai/templates/configuration/User-Profile.md`
- Runtime instance: `.ai/runtime/User-Profile.md`

The template defines the structure.
The runtime instance stores the actual user-specific values.

## Runtime Principles
- `.ai/` contains both framework configuration and runtime AI configuration.
- Human-facing work should stay in normal visible vault folders.
- Runtime files should be created intentionally, not implicitly assumed.
- Local topic context can override runtime defaults where needed.

## Related Documents
- [[Setup-Flow]]
- [[Migration-Mode]]
- [[Versioning]]
