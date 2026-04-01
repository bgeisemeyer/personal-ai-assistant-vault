# Migration Mode

## Purpose

This document defines when and how the framework should enter migration mode for an existing vault.

## Migration Trigger

Migration mode becomes relevant when:
- the framework is installed
- `.ai/runtime/User-Profile.md` exists or is about to be created
- the user indicates that this is an existing vault, not a clean new one

Migration mode can also be considered active when a root-level `Migration/` folder exists.

## Standard Migration Workspace

The standard migration workspace is:

`Migration/`

It should stay visible in the vault root so the user can follow the process inside Obsidian.

## Migration Flow
1. confirm that this is an existing vault
2. confirm backup status
3. choose scan scope
4. create `Migration/` from the migration templates
5. analyze the selected area
6. document findings and proposals
7. let the user decide
8. migrate in controlled waves
9. review after each wave

## Migration Scope Options
- whole vault
- selected folders
- pilot area

## Related Documents
- [[Migration-Guide]]
- [[Safety-and-Backups]]
- [[Runtime-Model]]
