# Migration Guide

## Purpose

This guide explains how to introduce the framework into an existing vault without turning the process into a risky or opaque mass migration.

## Recommended Strategy

Use a guided migration with a visible `Migration/` folder in the vault root.

This means:
- install the framework first
- configure it second
- scan the existing vault or a selected area
- document the findings
- propose changes
- let the user decide
- migrate step by step

## Migration Stages

1. `Installed`
   The framework files are present in the vault.
2. `Configured`
   `User-Profile.md` and governance defaults are in place.
3. `Assessed`
   The selected vault area has been scanned and documented.
4. `Migration Planned`
   Proposals, mappings, and rollout steps are documented.
5. `Migrating`
   Approved changes are being applied in controlled waves.
6. `Operational`
   The selected areas are working with stable context, structure, and reusable workflows.

## Step-by-Step Process

### 1. Back up the vault
- Create a full backup first.
- Preferably test the process in a copy before touching the live vault.

### 2. Install the framework
- Copy the framework files into the vault root.
- Keep `.ai/` in the root.
- Do not start with a broad structural rewrite.

### 3. Configure the framework
- Create `User-Profile.md`.
- Set language, safety posture, and structure preferences.

### 4. Choose the scan scope
- whole vault
- selected folders
- one pilot area

### 5. Create `Migration/` in the vault root
- This folder stays visible in Obsidian.
- It is the central workspace for scan results, migration planning, decisions, and rollout tracking.

### 6. Analyze the selected scope
- Inventory the current structure.
- Identify local context that already exists.
- Identify missing structure, duplicate systems, and risky areas.

### 7. Document findings and proposals
- Record findings in `Migration/Findings.md`.
- Record proposed changes in `Migration/Proposals.md`.
- Record old-to-new relationships in `Migration/Mapping.md`.

### 8. Decide with the user
- Keep areas unchanged when they already work well.
- Add context or standard files when that is enough.
- Restructure only where the value is clear.

### 9. Roll out in waves
- Start with one pilot area.
- Review the result.
- Continue only after the user confirms the direction.

### 10. Review after each wave
- Check links.
- Check clarity.
- Check whether the framework actually improved continuity and usability.

## Scan Scope Options

### Whole Vault
- Best when the user wants a broad assessment first.
- Higher effort and higher complexity.

### Selected Folders
- Best when the vault has clear high-value areas to migrate first.
- Lower risk than a full-vault scan.

### Pilot Area
- Best default for cautious rollouts.
- Useful for validating the framework before expanding it.

## Migration Principles
- Never start without a backup.
- Analyze first, propose second, change third.
- Prefer augmentation over replacement.
- Preserve working structures unless the benefit of change is clear.
- Avoid mass changes without explicit approval.
- Treat sensitive areas conservatively.
- Document every important decision.

## Questions To Ask Before Scanning
1. Should the whole vault be scanned or only part of it?
2. Which areas are sensitive?
3. Which areas must never be changed automatically?
4. Should the process stop after analysis, or also prepare proposals?
5. Should the rollout start with one pilot area?
6. Should the existing structure be lightly augmented or more strongly aligned with the framework?

## Related Guides
- [[Getting-Started]]
- [[Safety-and-Backups]]
