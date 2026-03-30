# Safety and Backups

## Before You Start

Before installing or migrating this framework into an existing vault:

- make a full backup of the vault
- ideally test the setup in a copy first
- create a git commit or snapshot if your vault already uses version control

## Why This Matters

This framework is designed to help, not to guarantee safe outcomes.

Introducing it into an existing vault may still create problems if changes are applied too broadly, too quickly, or without enough review.

## What Could Go Wrong
- Broken internal links
- Confusing parallel structures
- Duplicate context files
- Migration plans with too much scope
- Changes applied where none were needed
- Processing of sensitive content without enough caution
- Reduced clarity instead of improved continuity

## Safe Default Approach

Use this order:

1. back up
2. install
3. configure
4. analyze
5. propose
6. decide
7. change
8. review

## Sensitive Areas

These should be treated conservatively by default:
- health
- finance
- work materials
- private communication
- identity data

## Rollback Strategy

If a migration wave goes wrong:

1. stop further changes
2. review the latest migration log entries
3. restore from backup if needed
4. revert the latest approved wave if you use version control
5. narrow the scope and reassess

## Recommended Practice
- Start with one pilot area.
- Keep `Migration/` visible in the vault root.
- Do not let the framework silently replace your existing structure.
- Make sure every larger change has a documented reason.

## Related Guides
- [[Getting-Started]]
- [[Migration-Guide]]
