# Setup Flow

## Purpose

This document defines how the framework should start in a real vault.

## Setup Trigger

The framework should enter setup mode when:
- the framework files are present
- but `.ai/runtime/User-Profile.md` does not exist yet

## Setup Mode

In setup mode, the AI should:
1. read `AGENTS.md`
2. read `.ai/governance/Index.md`
3. detect that `.ai/runtime/User-Profile.md` is missing
4. offer the initial setup flow
5. use `.ai/onboarding/Initial-Setup.md`
6. create `.ai/runtime/User-Profile.md` from `.ai/templates/configuration/User-Profile.md`

## Output Of Setup

The minimum successful setup output is:
- a completed `.ai/runtime/User-Profile.md`

After that, the framework can continue in one of two directions:
- normal operational use for a new vault
- migration mode for an existing vault

## What Setup Should Establish
- preferred working language
- translation preference for templates and governance
- usage scope
- safety defaults
- privacy posture
- structure preferences

## Related Documents
- [[Getting-Started]]
- [[Migration-Guide]]
- [[Runtime-Model]]
