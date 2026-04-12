> **Human navigation.** AI agents: use `docs/conventions/index.yaml` — do not read this file for navigation.

# Conventions

Coding standards for all contributors. These rules exist to maintain consistency across the codebase.
When a convention conflicts with an ADR, the ADR takes precedence.

## Documents

### `typescript.md`
Type system usage, strictness settings, patterns to prefer and avoid.
Load when: writing or reviewing TypeScript code.

### `testing.md`
Test structure, naming, mocking strategy, coverage expectations.
Load when: writing tests, reviewing test quality, setting up test infrastructure.

### `git.md`
Commit message format, branch naming conventions, PR expectations.
Load when: committing code, opening a PR, reviewing history.

---

## Adding a New Convention Document
Copy `_template.md` to a new file named after the topic (e.g. `error-handling.md`).
Add the new file to the `documents` list in `index.yaml`.
