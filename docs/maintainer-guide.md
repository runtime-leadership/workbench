# Workbench Maintainer Guide

Workbench is maintained by Runtime Leadership as a lightweight, practical starting point for people navigating engineering work, people, and decisions.

This guide captures product and repository conventions. It is not a required process for people using a private Workbench.

## Product Boundaries

Workbench supports work already worth doing. It is not:

- a new management process
- a checklist that proves work happened
- a requirement to document every conversation or decision
- a replacement for judgment, direct communication, or existing company systems
- a reason to create artifacts nobody will use

Add a resource only when it helps someone prepare better, see relevant context, make a clearer decision, or preserve a useful outcome in one sitting. If it creates more upkeep than value, it does not belong here.

## Upstream and Private Workbenches

Runtime Leadership maintains the canonical root structure and reusable resources. Users create independent private repositories from the GitHub template, add approved context, and adapt resources to local needs.

Future upstream changes are options, not mandatory migrations. Users should be able to review and adopt the resources they want without reorganizing their work around the repository.

## Functional Structure

Organize resources by what they do:

```text
templates/   Reusable working artifacts
resources/   Curated reference material
skills/      Repeatable instructions and workflows
agents/      Delegated roles with a defined job and boundaries
docs/        Explanations, setup guidance, and reference material
knowledge/   Durable context captured in a private Workbench
projects/    Active project context and working artifacts
```

Keep these areas distinct. A template may link to a resource or skill that helps complete it. A skill may invoke an agent for a bounded task. An agent may use templates, resources, documentation, knowledge, or project context. A counterpart is optional; do not create one merely to make every resource look complete.

## Ownership Boundaries

The canonical Workbench repository maintains `docs/` and the reusable tools distributed through `templates/`, `resources/`, `skills/`, and `agents/`. In a private Workbench, users should add new local files instead of modifying upstream files when practical. This makes future upstream changes easier to evaluate and adopt.

The private working areas are:

- `knowledge/` for durable personal, team, organizational, and technical context that may help across multiple situations
- `projects/` for active project context, analysis, plans, and working artifacts

Agents should read `docs/` for instructions but must not write there unless explicitly asked to maintain Workbench. They should write reusable context to `knowledge/` and project-specific output to `projects/`. Private workplace facts must not be added to an upstream contribution.

## Tool Compatibility

Canonical resources should remain readable as ordinary files so they work with OpenCode, Claude Code, Codex, Cursor, and other tools that can inspect a repository.

Some platforms require special directories or metadata for automatic discovery. Add platform-specific adapters only when they materially improve use. Adapters should point back to the canonical functional resource rather than becoming a separate source of truth. No AI platform should define the root structure.

## Context and Judgment

A private Workbench may contain employee, company, customer, project, or code context. Users should follow company policies, add only information and repositories they are authorized to use, and capture the minimum useful context rather than centralizing sensitive information by default.

Agents may retrieve, compare, challenge, and organize context. They must not invent missing facts or replace human judgment.

## Resource Relationships

The initial resources form a natural sequence without requiring one fixed workflow:

- The Career Ladder Library provides reference language and examples.
- The Growth Conversation Template applies expectations to evidence and focused development priorities.
- The 1:1 Template provides recurring space for support, feedback, progress, and changing context.

Each resource must remain useful on its own.

## Publishing Relationship

Runtime Leadership articles should reference other relevant articles when helping readers continue learning. A separate, compact call to action may offer Workbench as the place to use a related template or tool. Workbench complements the editorial path; it does not replace it or become required reading.

Each template should begin with a small callout:

> Part of [Workbench by Runtime Leadership](https://github.com/runtime-leadership/workbench), a lightweight workspace for navigating engineering work, people, and decisions. Use this template on its own or in a private Workbench created from the GitHub template.
