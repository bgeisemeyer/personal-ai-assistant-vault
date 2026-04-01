# Personal AI Assistant Vault

> 🧠 An open-source framework for building an AI-managed Obsidian vault that stays usable across different AI tools.

## ✨ What This Is

`Personal AI Assistant Vault` is a framework for turning an Obsidian vault into a durable, AI-assisted operating system for knowledge work.

Instead of storing critical context inside one chat session, this framework keeps rules, working context, progress, templates, and reusable workflows in files.

That makes it easier to continue work across different AI tools and future AI environments without losing the thread.

## 🎯 Vision

The goal is to combine:
- Obsidian as the human-friendly knowledge environment
- AI as assistant, operator, and collaborative partner
- file-based context as the continuity layer between tools

The result should be a reusable vault scaffold for private life, work, projects, hobbies, finance, research, and other personal or professional domains.

## 🔥 What This Is Really For

This framework is not only about keeping AI workflows portable.

It is meant to help build a real personal assistant inside Obsidian: one that can reduce mental load, save time, support difficult tasks, and automate multi-step workflows that would otherwise stay undone or consume too much energy.

The goal is not just better note-taking with AI.
The goal is practical assistance in real life.

That includes things like:
- helping with private topics that are hard to organize
- reducing repetitive admin work
- turning complex workflows into structured, reusable automations
- supporting research, writing, explanation, and decision-making
- making it easier to start or finish tasks that feel overwhelming

This should become a system that genuinely takes work off your shoulders.

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

## 🧩 What You Can Build With It

With the right skills, templates, and integrations, this framework can support workflows such as:

- reading and triaging emails for a specific topic
- extracting and explaining content from PDF attachments
- drafting and eventually sending suitable replies
- running structured research across trustworthy sources
- turning research into summaries, presentations, and decision-ready notes
- using OCR, PDF readers, speech-to-text, text-to-speech, Excalidraw, Signal, or custom MCP-connected tools
- automating repeated multi-step processes through reusable skills

The point is not to hard-code one assistant.
The point is to create a durable system for building many useful assistants and workflows on top of the same vault foundation.

## 🔁 Example Workflows

### Email + document understanding
Read emails related to a private topic, open PDF attachments, extract the relevant information, explain the contents in plain language, draft a suitable reply, and send it after approval.

### Research to presentation
Run research on a topic using at least 10 trustworthy sources, evaluate the results, turn them into a presentation draft, and add fitting Excalidraw sketches.

### Support for difficult life admin
Take emotionally difficult, cognitively heavy, or time-consuming topics and turn them into structured, reviewable workflows with clear context, next steps, and reusable logic.

### Tool-connected workflows
Combine MCP-connected tools, local files, structured templates, and reusable skills into end-to-end automations that would otherwise require manual coordination across many steps.

## 🗂️ Structure

```text
.ai/
  governance/
  skills/
  references/
  onboarding/
  runtime/
  templates/
```

### `.ai/governance/`
Core rules, safety posture, and the model for how the framework works.

### `.ai/skills/`
Reusable AI workflows such as research, vault maintenance, PDF processing, and diagram work.

### `.ai/references/`
Supporting conventions and reference material used by governance or skills.

### `.ai/onboarding/`
The initial setup flow that turns user answers into a durable `.ai/runtime/User-Profile.md`.

### `.ai/runtime/`
Runtime AI configuration such as the live user profile used during real vault operation.

### `.ai/docs/`
Public framework documentation that should stay available without cluttering the vault root.

### `.ai/templates/`
Reusable structures for topics, projects, assistants, and configuration files.

## ⚙️ How It Works

The framework uses layered context:

1. `Safety.md` defines hard safety boundaries.
2. Local `Index.md` files define topic-specific context.
3. `.ai/runtime/User-Profile.md` stores stable user defaults.
4. Skills define reusable workflows.
5. Templates provide repeatable structure.

This lets different AI tools continue work with less reliance on hidden session state.

## 🔌 Extensible By Design

The framework is designed to grow through:

- reusable skills for recurring workflows
- MCP-connected tools for external capabilities
- local context files for domain-specific boundaries
- templates for predictable structure
- user configuration for language, tone, and safety posture

That means you can start with a simple vault setup and gradually evolve it into a much more capable assistant system without rebuilding everything around one vendor or one session model.

## 🌍 Language Model

- Repository default: English
- User language: configured through `.ai/runtime/User-Profile.md`
- Local exceptions: allowed in the nearest `Index.md`

That means the framework can stay internationally readable while still adapting to each user.

## 🚧 Current V1 Scope

Included in V1:
- governance
- onboarding
- runtime model
- user-profile template
- research template set
- generic skills for research, vault maintenance, PDF processing, and Excalidraw

Current V1 stays intentionally focused on the core framework and does not include private runtime data or secret material.

## 🚀 Entry Points

- `AGENTS.md`
- `CLAUDE.md`
- `.ai/governance/Index.md`
- `.ai/docs/Getting-Started.md`
- `.ai/docs/Migration-Guide.md`
- `.ai/docs/Safety-and-Backups.md`
- `.ai/docs/Runtime-Model.md`
- `.ai/docs/Setup-Flow.md`
- `.ai/docs/Migration-Mode.md`
- `.ai/docs/Versioning.md`
- `.ai/docs/Architecture.md`

These entry files intentionally stay minimal and point to the central governance model.

## 🧭 Installation Paths

- New vault: start with `.ai/docs/Getting-Started.md`
- Existing vault: use `.ai/docs/Migration-Guide.md`
- Sensitive or high-risk content: read `.ai/docs/Safety-and-Backups.md` first

## 🛡️ Safety And Responsibility

This project aims for safer defaults, not guaranteed safety.

- Review `DISCLAIMER.md`
- Review `SECURITY.md`
- Treat sensitive domains conservatively
- Keep public framework files separate from private runtime data

You remain responsible for how you use the framework and any AI output produced with it.

## 🤝 A Real Assistant, Not Just A Chat

The long-term idea is to create an assistant that can genuinely help with life, work, and everything in between.

Obsidian provides the structure and interface.
AI provides assistance, reasoning, and automation.
This framework connects both into a durable system that can keep getting better over time.

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
