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

## Tool access

The `🛡️ Security and Exploit Reviewer` and `⚙️ Backend Expert` agents s intentionally omit the `tools` frontmatter property so they can use all tools available in the session.

## How to use

1. Open VS Code with GitHub Copilot Chat enabled.
2. Make sure this folder is available as a custom agent location.
3. Open chat and pick an agent from the agents dropdown.
4. Prompt the selected agent with a task that matches its specialty.

Typical examples:

- Use **🎨 Frontend Expert** for redesigns, component improvements, or layout debugging.
- Use **🛡️ Security and Exploit Reviewer** for audits, exploit analysis, and seccurity hardening.
- Use **⚙️ Backend Expert** for NestJS backend implementation, debuggging, and architecture work.

## Repository structure

- `frontend-expert.agent.md` — UI and UX-focused custom agent
- `security-exploit-reviewer.agent.md` — security audit and remediation custom agent
- `backend-expert.agent.md` — backend and NestJS-focused custom agent

## Notes

- These agents are written as Markdown `.agent.md` files with YAML frontmatter.
- They are designed for GitHub Copilot custom agent support in VS Code.
- Agent instructions are intentionally opinionated so each agent behaves consistently within its specialty.
