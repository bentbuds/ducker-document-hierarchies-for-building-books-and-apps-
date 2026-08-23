# TESTING.md

## Purpose

Derived projects replace this file with their real testing strategy, commands, directories, test boundaries, mocks/fakes policy, and acceptance gates.

## Template integrity

For this framework repository, the primary verification command is:

```bash
python3 scripts/check-docs.py
```

It should verify required documentation structure, relative Markdown links, index coverage, and known path references.

## Derived-project requirements

- Core business logic uses TDD unless the project explicitly documents an exception.
- Tests should trace back to the approved spec/design/plan where practical.
- Do not claim verification unless the named command/test was actually run.
- Expensive full-project CI should be reserved for final delivery state; targeted tests may be used during development.
- Record the actual verification result in `docs/STATE.md`, not a process changelog.
