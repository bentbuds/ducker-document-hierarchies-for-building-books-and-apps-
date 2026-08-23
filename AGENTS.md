# AGENTS.md

## Human authority

Ducker is the final human approval authority for this template and for derived projects unless a derived project's own binding decision explicitly names a different final approver.

Do not attribute final approval to Shawn or another person unless Ducker explicitly delegates that authority in the project repository.

Use stable filenames. Do not encode people, agents, or chain of command into filenames.

When attribution matters, use labels such as:

- **Implemented:** who wrote the change
- **Modified:** who changed existing work
- **Reviewed:** who reviewed it
- **Verified:** who actually ran or checked verification
- **Requested/Approved:** who requested or approved the direction
- **Assigned:** who owns the next work item
- **Last Updated:** date of latest meaningful update

## Communication rules

1. Lead with the conclusion or action.
2. Do not repeat the same point in multiple forms.
3. Use concrete file/module names instead of vague references.
4. Use tables when a structured comparison is genuinely useful.
5. Report only findings that actually exist; do not invent filler categories.
6. Do not narrate obvious internal process.

## Hard rules

1. **Read docs before code.** For development tasks, read the relevant repository knowledge documents before editing.
2. **Plan before execution.** State the intended file changes and behavior before implementing non-trivial work. Obtain required human approval.
3. **Docs before code when criteria are met.** Create a Design Doc or Exec Plan only when the admission criteria below require one.
4. **Tests first for core logic.** Use Red → Green → Refactor for behavior that matters.
5. **No placeholder feature delivery.** Do not ship fake backends, empty implementations, or temporary branches as final product behavior unless Ducker explicitly asks for a prototype/spike.
6. **No minimum-diff shortcuts.** Prefer the right abstraction over the smallest patch.
7. **No silent decisions.** Non-trivial proposals must include `## Decisions Made Without Asking` and list choices made without Ducker's input.
8. **No unrequested scope expansion.** Report adjacent issues without changing them unless requested.
9. **Self-review and doc sync are part of completion.** A task is not done until verification and documentation synchronization are complete.
10. **Archived material is never current authority.** Do not use `docs/archive/` as current requirements.

## Repository knowledge map

### Current truth and binding choices

- `docs/STATE.md` — concise current-state snapshot; must match executable evidence
- `docs/DECISIONS.md` — still-binding decisions and trade-offs
- `ARCHITECTURE.md` — architecture map and dependency boundaries
- `docs/TESTING.md` — testing strategy and acceptance requirements
- `docs/DEPLOYMENT.md` — deployment/runtime procedures

### Product knowledge

- `docs/product-specs/knowledge-base.md` — current product behavior and key entry points
- `docs/product-specs/glossary.md` — canonical terminology

### Proposals and plans

- `docs/design-docs/index.md` — significant design proposals
- `docs/exec-plans/index.md` — multi-session / migration execution plans
- `docs/BACKLOG.md` — active product gaps and deferred work
- `docs/TECH_DEBT.md` — active implementation deviations with repayment paths

### History and references

- `docs/archive/README.md` — archive rules/catalog
- `docs/references/` — external guides and source material
- `docs/templates/` — Design Doc and Exec Plan templates

## Authority hierarchy

When sources conflict, resolve them in this order:

1. **Code and executable verification** — strongest evidence for what actually exists.
2. **`docs/STATE.md`** — current truth summary.
3. **`docs/DECISIONS.md`** — still-binding choices.
4. **Product / architecture / testing / deployment docs** — intended behavior and constraints.
5. **Active plans and backlog** — future work.
6. **`docs/archive/`** — historical context only.

Chat history is not project memory.

## Document budgets

### `docs/STATE.md` and `docs/product-specs/knowledge-base.md`

- Current conclusions only.
- Rewrite affected entries in place when facts change.
- Keep each domain/feature entry to roughly five lines or less.
- Link to the authoritative design, plan, or source entry point for details.
- Do not turn these files into changelogs.

### `docs/DECISIONS.md`

- Keep only still-binding decisions.
- Each decision should be concise: choice, rationale, trade-off, link.
- Remove decisions that no longer constrain future work.

### `docs/TECH_DEBT.md` and `docs/BACKLOG.md`

- Active queues only.
- Delete entries when repaid, started, abandoned, invalidated, or superseded.
- Do not keep completed-history tables here.

## Design Doc admission criteria

Default: **do not create one**.

Create a Design Doc only when both are true:

- the change materially alters architecture, module boundaries, data model, external contracts, major dependencies, or user interaction model; and
- at least two real approaches have different structural consequences, with meaningful rework if the wrong one is chosen.

Use `docs/templates/design-doc.md` and index it in `docs/design-docs/index.md`.

## Exec Plan admission criteria

Default: **do not create one**.

Create an Exec Plan when the work involves one of:

- cross-package/service cutover with ordering dependencies;
- irreversible migration or schema change;
- multi-PR or multi-session work requiring durable resume state.

Use `docs/templates/exec-plan.md`, store active plans in `docs/exec-plans/active/`, and move completed plans to `docs/exec-plans/completed/` without renaming.

## Naming conventions

- Design Doc: `D{number}-{kebab-case-description}.md`
- Exec Plan: `E{number}-{kebab-case-description}.md`

Numbers increment from the corresponding `index.md`.

## TDD discipline

For core business logic:

1. Write tests from the approved behavior/spec.
2. Run them and confirm they fail for the intended reason.
3. Implement the final behavior.
4. Refactor after the tests pass.
5. Run the project's final verification once at delivery state.

## Doc sync matrix

| Trigger | Check/update |
|---|---|
| Feature added/changed | `docs/product-specs/knowledge-base.md`, `docs/STATE.md` |
| Architecture changed | `ARCHITECTURE.md`, possibly `docs/DECISIONS.md` |
| Design Doc adopted | `docs/design-docs/index.md`, relevant architecture/product docs |
| Exec Plan completed | `docs/STATE.md`, `docs/exec-plans/index.md`, move plan to `completed/` |
| New deployment/runtime dependency | `docs/STATE.md`, `docs/DEPLOYMENT.md`, `ARCHITECTURE.md` |
| New technical debt | `docs/TECH_DEBT.md` |
| New product gap/deferred work | `docs/BACKLOG.md` |
| Historical doc no longer authoritative | move to `docs/archive/` and update archive catalog |

## Pre-delivery self-review

Before claiming completion:

- [ ] Behavior matches the approved request/spec.
- [ ] Relevant tests exist and pass.
- [ ] No placeholder code was introduced as final behavior.
- [ ] No unresolved `TODO` / `FIXME` / `HACK` remains unless tracked as active debt.
- [ ] Error paths and external-state assumptions are explicit.
- [ ] Security-sensitive inputs are validated at boundaries.
- [ ] `docs/STATE.md` matches what actually exists.
- [ ] Related docs were synchronized.
- [ ] Any decisions made without asking are disclosed.
- [ ] Ducker's required approval has been obtained where the workflow requires it.

## Project customization

Derived projects should add their real commands, tech stack, coding rules, and testing conventions below rather than keeping placeholders.

### Common commands

Project-specific.

### Tech stack

Project-specific.

### Coding rules

Project-specific.

### Testing

Project-specific; see `docs/TESTING.md`.
