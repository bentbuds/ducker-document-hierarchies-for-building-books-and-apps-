# Bootstrap: Set Up Ducker Agentic Docs for an Existing Project

> This file is an AI-agent prompt.

## Mission

Analyze the target project, install this repository's document-driven development framework, migrate existing project knowledge into the new authority hierarchy, and verify documentation integrity.

Ducker is the final human approval authority unless the target repository already contains a binding decision naming another final approver.

## Phase 1 — Analyze the project

Inspect project identity, tech stack, source structure, entry points, build/test commands, CI, deployment, architecture boundaries, existing agent instructions, documentation, and infrastructure.

Do not invent facts. Separate findings into:

- **Confirmed** — supported by repository evidence.
- **Needs input** — not discoverable from the repository.

## Phase 2 — Confirm with Ducker

Present the concise analysis and ask Ducker to correct errors, fill important unknowns, and approve the migration approach before changing project files.

## Phase 3 — Copy the framework

Use this repository as the source of truth:

`https://github.com/bentbuds/ducker-document-hierarchies-for-building-books-and-apps-`

Copy the framework at the same relative paths:

- `AGENTS.md`
- `ARCHITECTURE.md`
- `docs/STATE.md`
- `docs/DECISIONS.md`
- `docs/DEPLOYMENT.md`
- `docs/TESTING.md`
- `docs/TECH_DEBT.md`
- `docs/BACKLOG.md`
- `docs/archive/README.md`
- `docs/product-specs/knowledge-base.md`
- `docs/product-specs/glossary.md`
- `docs/design-docs/index.md`
- `docs/exec-plans/index.md`
- `docs/templates/design-doc.md`
- `docs/templates/exec-plan.md`
- `scripts/check-docs.py`

Create empty tracked directories with `.gitkeep` where needed:

- `docs/exec-plans/active/`
- `docs/exec-plans/completed/`
- `docs/references/`

## Phase 4 — Migrate, do not duplicate

Classify existing docs and move their current facts into the authoritative destination:

| Existing knowledge | Destination |
|---|---|
| Architecture/system design | `ARCHITECTURE.md` |
| Current state/runtime facts | `docs/STATE.md` |
| Binding technical decisions | `docs/DECISIONS.md` |
| Feature/product behavior | `docs/product-specs/knowledge-base.md` |
| Terminology | `docs/product-specs/glossary.md` |
| Testing | `docs/TESTING.md` |
| Deployment/ops | `docs/DEPLOYMENT.md` |
| Significant technical proposals | `docs/design-docs/` |
| Multi-session/migration plans | `docs/exec-plans/` |
| Active implementation deviations | `docs/TECH_DEBT.md` |
| Active product gaps/deferred work | `docs/BACKLOG.md` |
| Historical completed docs worth retaining | `docs/archive/` |

Delete superseded duplicate authority after migration. Archive only material with real historical value.

## Phase 5 — Customize with real facts

Replace template guidance with project-specific facts. Do not leave fake commands or placeholder architecture.

Keep the authority hierarchy:

**Code / executable evidence → `docs/STATE.md` → `docs/DECISIONS.md` → product/architecture/testing/deployment → active plans/backlog → archive.**

Keep filenames stable. Record authorship/approval using labels inside documents, not filenames.

Recommended labels:

**Implemented · Modified · Reviewed · Verified · Requested/Approved · Assigned · Last Updated**

## Phase 6 — Verify

Run:

```bash
python3 scripts/check-docs.py
```

Then inspect every reported failure and fix the documentation structure. Confirm that `docs/STATE.md` matches what actually exists in code/config.

## Phase 7 — Report

Report:

- files created/migrated/archived/deleted,
- remaining unknowns,
- documentation integrity result,
- decisions made without asking,
- exact next action.

Do not begin unrelated feature work during bootstrap without Ducker's explicit approval.
