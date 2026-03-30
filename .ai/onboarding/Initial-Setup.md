# Initial Setup

## Goal
Create a `User-Profile.md` that captures durable user preferences for the framework.

## Flow
1. Explain that the framework stores durable preferences in files instead of relying on session memory.
2. Ask the setup questions in a stable order.
3. Turn the answers into a filled `User-Profile.md`.
4. Confirm which settings are global defaults and which can still be overridden locally.

## Question Blocks

### 1. Language
- What is the preferred working language?
- Should templates be translated?
- Should governance files be translated or kept in English?

### 2. Usage Scope
- Which domains should the vault support?
- Which domains are sensitive by default?

### 3. Safety Settings
- Require confirmation before risky external actions?
- Require confirmation before file writes outside the main topic?
- Keep a draft-first workflow by default?

### 4. Privacy Settings
- Which domains must be treated as highly sensitive?
- Which actions should never be automated?

### 5. Structure Preferences
- Prefer flatter or more categorized structures?
- Require local `Index.md` files?
- Require local logs?

## Mapping To `User-Profile.md`
- Language answers fill `## Language`.
- Domain and usage answers fill `## Usage Scope`.
- Confirmation and approval answers fill `## Safety Settings`.
- Sensitive-data answers fill `## Privacy`.
- Structure answers fill `## Structure Preferences`.

## Output
- Fill a `User-Profile.md` instance from `.ai/templates/configuration/User-Profile.md`.
- Treat the result as durable defaults, not as a complete replacement for local context.
