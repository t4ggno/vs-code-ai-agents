# VS Code AI Agents

This repository contains a curated set of custom GitHub Copilot agents for use in VS Code.

Each agent is packaged as a Markdown `.agent.md` file with YAML frontmatter and is designed to live in the user-level custom agent location so it can be reused across multiple workspaces and projects.

The collection is intentionally opinionated: each agent focuses on a narrow specialty, follows a concrete workflow, and is meant to produce high-signal, task-specific behavior instead of generic “do everything” answers.

## What is in this repository

The repo currently includes specialist agents for:

- frontend engineering and UI redesign
- backend and NestJS architecture
- security review and remediation
- Java development workflows
- Python development workflows
- Tauri desktop application development
- Hytale modding and creator workflows

In practice, this makes the repo useful as a reusable personal agent library for switching quickly between focused engineering modes inside VS Code.

## Included agents

| File                                 | Agent                            | Best used for                                                                                                     |
| ------------------------------------ | -------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `frontend-expert.agent.md`           | 🎨 Frontend Expert               | UI redesigns, component cleanup, responsive layout fixes, design-system alignment, React/TypeScript/Tailwind work |
| `backend-expert.agent.md`            | ⚙️ Backend Expert                | NestJS services, controllers, DTOs, guards, MikroORM flows, auth, API design, backend correctness                 |
| `security-exploit-reviewer.agent.md` | 🛡️ Security and Exploit Reviewer | security audits, exploit-path analysis, auth/authz review, secret exposure review, hardening and remediation      |
| `java-expert.agent.md`               | ☕ Java Expert                   | Java build tooling, packaging, debugging, testing, dependency management, Maven/Gradle workflows                  |
| `python-expert.agent.md`             | 🐍 Python Expert                 | Python environments, packaging, typing, pytest, tooling alignment, interpreter and dependency issues              |
| `tauri-expert.agent.md`              | 🦀 Tauri Expert                  | Tauri v2 architecture, Rust↔frontend IPC, capabilities, permissions, plugins, packaging, updater flows            |
| `hytale-mod-development.agent.md`    | 🎮 Hytale Mod Development        | Hytale plugins, data assets, art/content workflows, early-access modding guidance, creator tooling                |

## Agent highlights

### `frontend-expert.agent.md` — 🎨 Frontend Expert

Focused on modern UI engineering and UI/UX improvement with strong opinions about:

- redesigning weak layouts instead of polishing obviously flawed ones
- hierarchy, spacing, responsive behavior, accessibility, and dark-mode compatibility
- React, TypeScript, Vite, Tailwind CSS v4, and shadcn/ui-based workflows
- design research, design briefs, and implementation grounded in current UI patterns

### `backend-expert.agent.md` — ⚙️ Backend Expert

Focused on clean backend architecture and secure NestJS implementation, especially:

- modules, controllers, providers, guards, interceptors, and DTO design
- MikroORM entity manager usage, request context, serialization, locking, and write boundaries
- REST APIs, WebSockets, queues, and webhook flows
- authentication, authorization, and production-minded backend hardening

### `security-exploit-reviewer.agent.md` — 🛡️ Security and Exploit Reviewer

Focused on realistic application security review and remediation, including:

- full-repository sweeps instead of partial spot checks
- authentication, authorization, object-level access control, and session/token handling
- SQL/command/deserialization-style risks, secret leaks, and sensitive data exposure
- exploit-chain thinking, targeted remediation, and post-fix validation

### `java-expert.agent.md` — ☕ Java Expert

Focused on modern Java engineering workflows such as:

- Maven and Gradle project structure, wrappers, toolchains, and packaging
- Java debugging, testing, dependency graph issues, and VS Code Java workflows
- project-aware code organization and framework-sensitive implementation

### `python-expert.agent.md` — 🐍 Python Expert

Focused on modern Python development and environment discipline, including:

- interpreter and virtual-environment selection
- `pyproject.toml`, requirements files, packaging, and dependency hygiene
- pytest, linting, typing, and editor-aware debugging workflows

### `tauri-expert.agent.md` — 🦀 Tauri Expert

Focused on Tauri desktop and mobile app architecture with emphasis on:

- Rust core vs WebView responsibility boundaries
- commands, events, channels, capabilities, permissions, and plugins
- packaging, updater flows, sidecars, and security-aware desktop design

### `hytale-mod-development.agent.md` — 🎮 Hytale Mod Development

Focused on practical Hytale creator workflows, including:

- server plugins, data assets, art assets, prefabs, and creator tooling
- early-access-safe documentation-grounded guidance
- Java-based mod/plugin setup and version-aware modding advice

## Shared conventions across the repo

These agent files follow a fairly consistent structure:

- filename pattern: `<specialty>.agent.md`
- YAML frontmatter with fields such as `name`, `description`, `argument-hint`, and `target`
- `target: vscode` for VS Code-specific usage
- long-form agent body describing expertise, workflow, rules, validation expectations, and output format

The agents are intentionally written with a strong voice and concrete working style. They are not minimalist prompts; they are specialized operating modes.

## Tool access

The current agents intentionally omit `tools` and `model` frontmatter so they can inherit the session defaults and use the available toolset provided by GitHub Copilot in VS Code.

## Repository structure

```text
.
├── backend-expert.agent.md
├── frontend-expert.agent.md
├── hytale-mod-development.agent.md
├── java-expert.agent.md
├── python-expert.agent.md
├── security-exploit-reviewer.agent.md
├── tauri-expert.agent.md
└── README.md
```

### File-by-file overview

- `frontend-expert.agent.md` — opinionated frontend and UI/UX redesign agent
- `backend-expert.agent.md` — NestJS and backend architecture agent
- `security-exploit-reviewer.agent.md` — security audit and remediation agent
- `java-expert.agent.md` — Java build/debug/package workflow agent
- `python-expert.agent.md` — Python environment, packaging, and tooling agent
- `tauri-expert.agent.md` — Tauri/Rust desktop application specialist agent
- `hytale-mod-development.agent.md` — Hytale modding and creator-workflow specialist agent
- `README.md` — repository overview and usage guide

## How to use

1. Open VS Code with GitHub Copilot Chat enabled.
2. Make sure this folder is available as a custom agent location.
3. Open chat and select one of the custom agents from the agent picker.
4. Prompt the selected agent with a task that matches its specialty.

### Example use cases

- Use **🎨 Frontend Expert** for redesigns, component cleanup, layout debugging, and responsive UI upgrades.
- Use **⚙️ Backend Expert** for NestJS implementation, API architecture, DTO and guard design, or MikroORM-backed backend work.
- Use **🛡️ Security and Exploit Reviewer** for audits, exploit analysis, and security hardening.
- Use **☕ Java Expert** for Java build failures, Gradle/Maven setup, test workflows, or debugger issues.
- Use **🐍 Python Expert** for environment confusion, packaging cleanup, test/tooling issues, or modern Python refactors.
- Use **🦀 Tauri Expert** for Rust/frontend boundary issues, command design, capabilities, updater flows, or desktop packaging.
- Use **🎮 Hytale Mod Development** for Hytale plugin work, asset workflows, modding guidance, or creator-pipeline questions.

## Why this repo exists

This repo is useful when you want:

- reusable agents that are available across projects
- specialty prompts with stronger guidance than a generic assistant mode
- consistent task framing for frontend, backend, security, Java, Python, Tauri, and Hytale work
- a maintainable library of custom agent definitions that can evolve over time

## Notes

- These agents are designed for GitHub Copilot custom agent support in VS Code.
- The prompts favor explicit workflows, practical validation, and specialty-specific judgment.
- Because the agents are stored as plain Markdown files, they are easy to version, review, and refine over time.
