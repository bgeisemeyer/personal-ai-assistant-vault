# Personal AI Assistant Vault

> 🧠 An open-source framework for building an AI-managed Obsidian vault that stays usable across different AI tools.

## ✨ What This Is

`Personal AI Assistant Vault` is a framework for turning an Obsidian vault into a durable, AI-assisted operating system for knowledge work.

Instead of storing critical context inside one chat session, this framework keeps rules, working context, progress, templates, and reusable workflows in files.

That makes it easier to continue work across tools like OpenCode, Claude Code, and future AI environments without losing the thread.

## 🎯 Vision

The goal is to combine:
- Obsidian as the human-friendly knowledge environment
- AI as assistant, operator, and collaborative partner
- file-based context as the continuity layer between tools

The result should be a reusable vault scaffold for private life, work, projects, hobbies, finance, research, and other personal or professional domains.

## 💡 Core Principles

- **AI-agnostic:** no single assistant should own the context
- **Tool-agnostic:** the structure should survive tool changes
- **File-based continuity:** important context belongs in files, not hidden memory
- **Configurable language:** framework defaults to English, user preferences come from configuration
- **Safety-aware:** conservative defaults, explicit limits, no false promises
- **Open and adaptable:** intended as a public, reusable foundation

## 🤔 Why This Exists

Most AI workflows break when:
- you switch tools
- you lose session history
- context is scattered across prompts
- rules live in memory instead of in the repository

This framework addresses that by storing the operating model directly in the vault.

## 🗂️ Structure

```text
.ai/
  governance/
  skills/
  references/
  onboarding/
  templates/
```

### `.ai/governance/`
Core rules, safety posture, and the model for how the framework works.

### `.ai/skills/`
Reusable AI workflows such as research, vault maintenance, PDF processing, and diagram work.

### `.ai/references/`
Supporting conventions and reference material used by governance or skills.

### `.ai/onboarding/`
The initial setup flow that turns user answers into a durable `User-Profile.md`.

### `.ai/templates/`
Reusable structures for topics, projects, assistants, and configuration files.

## ⚙️ How It Works

The framework uses layered context:

1. `Safety.md` defines hard safety boundaries.
2. Local `Index.md` files define topic-specific context.
3. `User-Profile.md` stores stable user defaults.
4. Skills define reusable workflows.
5. Templates provide repeatable structure.

This lets different AI tools continue work with less reliance on hidden session state.

## 🌍 Language Model

- Repository default: English
- User language: configured through `User-Profile.md`
- Local exceptions: allowed in the nearest `Index.md`

That means the framework can stay internationally readable while still adapting to each user.

## 🚧 Current V1 Scope

Included in V1:
- governance
- onboarding
- user-profile template
- research template set
- generic skills for research, vault maintenance, PDF processing, and Excalidraw

Explicitly excluded from V1:
- OpenCode-specific runtime files
- email automation
- calendar automation
- example content
- personal data
- secrets and local integration setup

## 🚀 Entry Points

- `AGENTS.md`
- `CLAUDE.md`
- `.ai/governance/Index.md`

These entry files intentionally stay minimal and point to the central governance model.

## 🛡️ Safety And Responsibility

This project aims for safer defaults, not guaranteed safety.

- Review `DISCLAIMER.md`
- Review `SECURITY.md`
- Treat sensitive domains conservatively
- Keep public framework files separate from private runtime data

You remain responsible for how you use the framework and any AI output produced with it.

## 🛣️ Roadmap

Planned next steps include:
- refining governance rules further
- improving the onboarding experience
- expanding generic templates
- preparing extraction into a dedicated public GitHub repository
- adding optional integrations later without making the framework tool-dependent

## 🤝 Contributing

Contributions should improve clarity, portability, safety posture, and reuse.

Good contribution areas:
- governance improvements
- generic skills
- templates
- onboarding
- documentation

## 📄 License

Released under `Apache-2.0`.

See `LICENSE`, `DISCLAIMER.md`, and `SECURITY.md` for the legal and safety framing.
