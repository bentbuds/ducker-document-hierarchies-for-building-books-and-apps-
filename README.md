# Ducker Agentic Docs Templates

Ducker-maintained fork of `Sukitly/agentic-docs-templates` for document-driven AI development across apps, tools, and long-form projects.

This repository keeps project memory in version-controlled documents so Codex, ChatGPT, Claude, Cursor, Gemini, and other agents can continue work without relying on chat history.

## Authority model

**Code / executable evidence → `docs/STATE.md` → `docs/DECISIONS.md` → product/architecture/testing docs → active plans/backlog → archive.**

Ducker is the final human approval authority for projects using this fork unless a project explicitly records a different owner in its own binding decisions.

## Quick start

1. Create a project from this repository or copy the documentation framework into an existing repo.
2. Read `AGENTS.md` before any development task.
3. Fill project facts into `ARCHITECTURE.md`, `docs/STATE.md`, `docs/TESTING.md`, and `docs/product-specs/`.
4. Run `python3 scripts/check-docs.py`.
5. Keep durable context in GitHub, not only in chat.

## Existing project bootstrap

Use this repository's bootstrap prompt:

```bash
claude "Read https://raw.githubusercontent.com/bentbuds/ducker-document-hierarchies-for-building-books-and-apps-/main/bootstrap.md and follow the instructions to set up agentic docs for this project."
```

Or download it first:

```bash
curl -sO https://raw.githubusercontent.com/bentbuds/ducker-document-hierarchies-for-building-books-and-apps-/main/bootstrap.md
claude "Read bootstrap.md and follow the instructions to set up agentic docs for this project."
```

## Repository structure

```text
├── AGENTS.md
├── ARCHITECTURE.md
├── bootstrap.md
├── docs/
│   ├── STATE.md
│   ├── DECISIONS.md
│   ├── DEPLOYMENT.md
│   ├── TESTING.md
│   ├── TECH_DEBT.md
│   ├── BACKLOG.md
│   ├── archive/
│   ├── product-specs/
│   ├── design-docs/
│   ├── exec-plans/
│   ├── templates/
│   └── references/
└── scripts/
    └── check-docs.py
```

## Core rules

- Read repository docs before changing code.
- `STATE.md` records current truth, not history.
- `DECISIONS.md` contains only still-binding decisions.
- Plan before execution and get required human approval.
- Use TDD for core business logic.
- Synchronize affected docs after implementation.
- Put historical material in `docs/archive/`; archived files are never current authority.
- Do not encode agent names or chain of command into filenames. Use attribution labels inside documents.

Recommended labels: **Implemented · Modified · Reviewed · Verified · Requested/Approved · Assigned · Last Updated**.

## Upstream

Original project: `Sukitly/agentic-docs-templates`.

This fork preserves upstream attribution and the MIT license while providing a Ducker-controlled source for future projects.
