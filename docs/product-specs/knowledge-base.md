# Product Knowledge Base

Keep this file as a concise current snapshot of user-visible behavior and product entry points. Rewrite entries in place when behavior changes; do not append process history.

## Agentic documentation framework

The framework stores durable project context in version-controlled Markdown with a strict authority hierarchy, stable filenames, bounded current-state documents, binding decisions, active queues, and a read-only archive. Primary entry points: `AGENTS.md`, `docs/STATE.md`, `docs/DECISIONS.md`, `ARCHITECTURE.md`, `docs/TESTING.md`, and `bootstrap.md`.

## Ducker approval model

Ducker is the default final human approval authority for this template and derived projects unless the derived project explicitly records a different final approver in its own binding decisions. Attribution is written inside documents rather than encoded in filenames.

## Bootstrap behavior

`bootstrap.md` instructs an AI agent to analyze an existing project, confirm findings with Ducker, copy this framework, migrate rather than duplicate existing authority, customize with real facts, and run `scripts/check-docs.py`.
