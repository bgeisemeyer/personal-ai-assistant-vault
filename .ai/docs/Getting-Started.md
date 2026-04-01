# Getting Started

## Choose Your Path

You can use this framework in two main ways:

1. Start with a new vault
2. Add it to an existing vault

## New Vault Setup

### 1. Create or open an Obsidian vault
- Use a new vault if you want a clean start.

### 2. Add the framework files
- Copy the framework into the vault.
- Keep the `.ai/` folder at the vault root.

### 3. Read the core entry points
- `AGENTS.md`
- `.ai/governance/Index.md`

### 4. Run the initial setup
- Create `.ai/runtime/User-Profile.md` from `.ai/templates/configuration/User-Profile.md`.
- Set language, structure preferences, and safety defaults.

### 5. Start with one topic
- Use a template from `.ai/templates/`.
- Add local context in the topic `Index.md`.
- Use the matching skill if needed.

## Existing Vault Setup

### 1. Make a backup first
- Recommended: create a full copy of the vault before adding the framework.
- If your vault already uses git, create a commit or snapshot first.

### 2. Add the framework files
- Copy the framework into the existing vault root.
- Do not restructure your whole vault immediately.

### 3. Run the initial setup
- Create `.ai/runtime/User-Profile.md`.
- Set language, structure preferences, and safety defaults.

### 4. Choose a migration scope
- Whole vault
- Selected folders
- One pilot area

### 5. Create a visible `Migration/` folder in the vault root
- Use the templates from `.ai/templates/migration/`.
- Keep scan results, proposals, and decisions there.

### 6. Migrate step by step
- Analyze first
- Propose second
- Change third

## Recommended First Operational State

You have reached a good first state when:
- the framework is installed
- `.ai/runtime/User-Profile.md` exists
- one pilot topic uses local context and templates
- the vault can be continued by an AI through files instead of chat memory

## Related Guides
- [[Migration-Guide]]
- [[Safety-and-Backups]]
