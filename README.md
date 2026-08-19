# Workbench

**By Runtime Leadership**

Workbench is a lightweight, opinionated monorepo for keeping your knowledge, projects, templates, resources, skills, and agents in one place.

The shared context makes every part more useful: agents can work from durable knowledge, skills can use templates and resources, and project outcomes can become context for future work. Workbench provides a practical starting structure and reusable tools without requiring you to adopt a new process.

## Create a Private Workbench

> **Use this repository as a template, not a public fork.** A public fork remains public, and a plain clone does not create an independent GitHub repository for your work.

1. Select **Use this template** on GitHub.
2. Create a new repository and set its visibility to **Private**.
3. Clone it and open it with OpenCode, Claude Code, Codex, Cursor, or another tool that can read a repository.
4. Add the approved context and tools that help with your work.

Do not use a public repository for private employee, company, customer, project, or code context.

## What Lives Here

| Path | Purpose | Write policy |
| --- | --- | --- |
| `docs/` | Documentation about Workbench itself | Upstream-managed; read-only unless maintaining Workbench |
| `templates/` | Reusable working artifacts | Use existing files or add local templates |
| `resources/` | Curated reference material | Use existing files or add local resources |
| `skills/` | Repeatable instructions and workflows | Use existing files or add local skills |
| `agents/` | Delegated roles with a defined job | Use existing files or add local agents |
| `knowledge/` | Your durable private knowledge base | Add and update reusable personal or organizational context |
| `projects/` | Active project context and artifacts | Add and update files while doing project work |

Treat `docs/` and existing files under `templates/`, `resources/`, `skills/`, and `agents/` as read-only by default. Put your durable context in `knowledge/` and project-specific work in `projects/`. Add new local tools instead of editing upstream files when practical.

## Compounding Context

Workbench becomes more useful as its parts connect:

- knowledge gives agents and skills durable context
- projects produce decisions and lessons worth retaining
- templates make recurring work easier to start
- resources provide trusted reference material
- skills encode repeatable ways of working
- agents apply focused capabilities across the repository

Keep only what earns its place. AI can organize and challenge context, but it should not invent missing facts or replace human judgment.

## Questions and Suggestions

Runtime Leadership maintains the canonical Workbench structure and does not currently accept external code contributions or pull requests.

[Open an issue](https://github.com/runtime-leadership/workbench/issues) if you have an idea, suggestion, or question. Issues are the preferred way to share feedback about the upstream template.

See the [maintainer guide](docs/maintainer-guide.md) for product boundaries, repository conventions, platform compatibility, and publishing guidance.
