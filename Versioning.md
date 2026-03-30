# Versioning

## Versioning Model

This project uses Semantic Versioning.

Format:

`MAJOR.MINOR.PATCH`

## Recommended Starting Line

The framework should begin public release versioning at:

`0.1.0`

This signals that the project is usable, but core structures may still evolve before `1.0.0`.

## What Counts As MAJOR
- breaking changes to core paths such as `.ai/`
- moving the official runtime location of `.ai/runtime/User-Profile.md`
- changing the role of `Migration/`
- changing key governance precedence rules
- renaming core template files in a way that affects users

## What Counts As MINOR
- new guides
- new generic skills
- new templates
- new optional capabilities
- non-breaking improvements to setup and migration support

## What Counts As PATCH
- documentation fixes
- wording clarifications
- link fixes
- small non-breaking template improvements

## Release Guidance
- keep `CHANGELOG.md` updated
- use GitHub releases and tags later
- document migration notes for every breaking change

## Stability Guidance
- `0.x`: faster iteration allowed, but document breaking changes clearly
- `1.x`: treat core structure and runtime conventions as stable by default

## Related Documents
- [[Runtime-Model]]
- [[Setup-Flow]]
- [[Migration-Mode]]
