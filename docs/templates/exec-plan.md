# E{N} — {Title}

**Status:** Active
**Requested/Approved:** Ducker
**Last Updated:** YYYY-MM-DD

## Goal

State the exact end condition.

## Scope

List packages/services/files included and excluded.

## Preconditions

List facts that must be true before execution starts.

## Sequence

Use ordered, independently verifiable steps with exact file paths, commands, and expected outcomes.

- [ ] Step 1
- [ ] Step 2

## Unsafe intermediate states

Document any state that must not be left partially applied and how the ordering prevents it.

## Verification

List targeted development checks and the final delivery-state CI/build/test command.

## Rollback

Describe how to restore the last known-good state.

## Resume state

Keep the exact next executable step here while the plan is active so a new agent/session can continue without chat history.

## Decisions Made Without Asking

List every non-trivial choice made without Ducker's explicit input and whether it was chosen because it is the right abstraction or merely convenient. Convenience-only choices require asking instead of silently proceeding.

## Completion

When complete:

1. run final verification;
2. perform the `AGENTS.md` self-review;
3. synchronize `docs/STATE.md` and affected docs;
4. move this file to `docs/exec-plans/completed/` without renaming;
5. update `docs/exec-plans/index.md`.
