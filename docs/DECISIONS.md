# DECISIONS.md

Only still-binding decisions belong here.

## D1 — Ducker is final human approval authority

**Decision:** Ducker has final approval for this template and derived projects unless a derived project's own binding decision explicitly names another final approver.

**Rationale:** Prevents agent/account identity confusion and preserves one clear human authority.

## D2 — Repository documents, not chat, are durable memory

**Decision:** Durable project context must live in version-controlled repository docs. Chat history is not authoritative project memory.

**Rationale:** Multiple agents must be able to continue from the repository alone.

## D3 — Authority hierarchy is fixed

**Decision:** Resolve conflicts in this order: code/executable evidence → `docs/STATE.md` → `docs/DECISIONS.md` → product/architecture/testing/deployment → active plans/backlog → archive.

**Rationale:** Separates current truth, binding choices, future work, and historical context.

## D4 — Stable filenames; attribution lives inside docs

**Decision:** Do not encode people or agents into filenames. Use stable names such as `STATE.md` and attribution labels inside entries.

**Rationale:** Avoids fragmented authority such as `STATE-ducker-codex-gpt.md`.

## D5 — This fork is self-contained

**Decision:** Bootstrap and usage instructions point to this Ducker-controlled repository. Upstream remains credited but is not required for normal use.

**Rationale:** Ducker can use and evolve the framework without depending on another maintainer's repository availability or future changes.
