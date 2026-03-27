# VS Code AI Agents

This repository contains a small collection of custom GitHub Copilot agents for use in VS Code.

The agents in this folder are designed to be discovered from the user-level custom agent location and reused across workspaces.

## Included agents

### `frontend-expert.agent.md` — 🎨 Frontend Expert

An opinionated UI engineering and UI/UX agent focused on:

- redesigning and modernizing interfaces
- improving layout, hierarchy, responsiveness, and accessibility
- working with React, TypeScript, Vite, Tailwind CSS v4, and shadcn/ui patterns
- making bold but scoped UI improvements instead of cosmetic-only tweaks

### `security-exploit-reviewer.agent.md` — 🛡️ Security and Exploit Reviewer

A security review and remediation agent focused on:

- full-repository security sweeps
- authentication and authorization review
- exploit-path analysis instead of checklist-only review
- API, WebSocket, ORM, secret-handling, and data-exposure issues
- applying high-confidence security fixes when remediation is requested

### `backend-expert.agent.md` — ⚙️ Backend Expert

A backend architecture and implementation agent focused on:

- NestJS modules, controllers, providers, decorators, guards, and interceptors
- DTO validation, exception handling, and API contract design
- MikroORM repositories, serialization, transactions, request context, and locking
- REST APIs, WebSockets, queues, and secure authentication/authorization flows

### `tauri-expert.agent.md` — 🦀 Tauri Expert

A Tauri-specific agent focused on:

- Tauri v2 architecture and frontend↔core IPC boundaries
- commands, events, plugins, sidecars, capabilities, and permissions
- packaging, updater flows, native integrations, and platform-specific behavior
- secure desktop and mobile app development with Rust + web frontends

### `java-expert.agent.md` — ☕ Java Expert

A general Java development agent focused on:

- Java application and library development
- Maven and Gradle build/package management
- JDK and toolchain-aware debugging, testing, and packaging
- VS Code Java workflows, dependency management, and architecture hygiene

### `hytale-mod-development.agent.md` — 🎮 Hytale Mod Development

A Hytale-specific modding agent focused on:

- Java server plugins, data assets, art assets, and prefab/world workflows
- Hytale documentation usage and version-aware modding guidance
- early-access-safe creator workflows, packaging, and publishing
- modding best practices grounded in official Hytale direction and community docs

## Tool access

These agents currently omit the `tools` frontmatter property so they can use all tools available in the session unless a future agent intentionally scopes them.

## How to use

1. Open VS Code with GitHub Copilot Chat enabled.
2. Make sure this folder is available as a custom agent location.
3. Open chat and pick an agent from the agents dropdown.
4. Prompt the selected agent with a task that matches its specialty.

Typical examples:

- Use **🎨 Frontend Expert** for redesigns, component improvements, or layout debugging.
- Use **🛡️ Security and Exploit Reviewer** for audits, exploit analysis, and security hardening.
- Use **⚙️ Backend Expert** for NestJS backend implementation, debugging, and architecture work.
- Use **🦀 Tauri Expert** for Tauri IPC, permissions, packaging, and native/runtime debugging.
- Use **☕ Java Expert** for Java application work, package management, build issues, and debugger/test workflows.
- Use **🎮 Hytale Mod Development** for Hytale plugins, assets, modding docs, creator workflows, and publishing guidance.

## Repository structure

- `frontend-expert.agent.md` — UI and UX-focused custom agent
- `security-exploit-reviewer.agent.md` — security audit and remediation custom agent
- `backend-expert.agent.md` — backend and NestJS-focused custom agent
- `tauri-expert.agent.md` — Tauri architecture and native app custom agent
- `java-expert.agent.md` — general Java development custom agent
- `hytale-mod-development.agent.md` — Hytale creator and modding custom agent

## Notes

- These agents are written as Markdown `.agent.md` files with YAML frontmatter.
- They are designed for GitHub Copilot custom agent support in VS Code.
- Agent instructions are intentionally opinionated so each agent behaves consistently within its specialty.
