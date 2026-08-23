# ARCHITECTURE.md

## Purpose

This file maps the actual architecture of a derived project: module boundaries, dependency directions, entry points, data flow, cross-cutting concerns, and paths that matter to agents.

## Authority

- Executable code is the strongest evidence of what exists.
- `docs/STATE.md` summarizes current truth.
- This file records the current architectural shape and constraints.
- Significant proposed architecture changes belong in `docs/design-docs/` until adopted.

## Project structure

Replace this section with the derived project's real top-level structure and responsibilities. Every local path written here should exist.

## Layering and dependency rules

Document allowed dependency directions and forbidden coupling. Keep external integrations behind explicit boundaries where practical.

## Entry points

List runtime, worker, CLI, UI, API, build, and test entry points that actually exist.

## Data flow

Describe the shortest accurate path through the system from external input to durable state/output.

## Cross-cutting concerns

Document validation, authentication/authorization, error handling, logging, observability, configuration, secrets, background jobs, caching, and security boundaries as applicable.

## Conventions

Record architectural conventions that constrain future work. Do not use this file as a changelog.

## Decisions Made Without Asking

None in the template. Derived projects must disclose non-trivial unapproved choices here or in the carrying Design Doc / Exec Plan before implementation.
