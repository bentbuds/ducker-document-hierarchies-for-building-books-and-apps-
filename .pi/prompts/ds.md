---
description: Check and sync all docs based on current branch changes
---

Perform a complete documentation sync check and update based on the current branch changes.

When an associated Exec Plan is complete and user verification is done, update its status, move it from `docs/exec-plans/active/` to `docs/exec-plans/completed/`, and update the index.

Check every relevant document before editing it. Apply the repository authority rules from `AGENTS.md`.

## Required checks

- `docs/STATE.md` reflects current truth only.
- `docs/DECISIONS.md` contains only still-binding decisions.
- `docs/product-specs/knowledge-base.md` reflects current product behavior.
- `ARCHITECTURE.md` reflects actual module/layer boundaries.
- `docs/DEPLOYMENT.md` reflects real deployment/runtime facts.
- `docs/TECH_DEBT.md` contains only active implementation deviations.
- `docs/BACKLOG.md` contains only active gaps/follow-ups.
- Design/Exec Plan indexes match their directories.
- Historical completed-purpose documents are archived and not treated as current authority.

## Evidence report

Report concrete evidence for each document checked, including whether it changed and why. Do not claim verification that was not actually performed.
