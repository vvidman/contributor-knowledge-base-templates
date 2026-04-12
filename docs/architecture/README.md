> **Human navigation.** AI agents: use `docs/architecture/index.yaml` — do not read this file for navigation.

# Architecture Principles

This category defines the design principles applied in this project and how they are interpreted here.
These documents explain the *why* behind structural decisions and the rules that follow from them.

When an architecture principle conflicts with a convention, the principle takes precedence.
When an ADR conflicts with an architecture principle, the ADR takes precedence.

## Documents

### `clean-architecture.md`
Layer structure, dependency direction, boundaries, and use cases.
Load when: reasoning about where code belongs or how layers should communicate.

### `solid.md`
How SOLID principles are applied in this project.
Load when: reviewing design decisions, evaluating class or interface design.

---

## Adding a New Architecture Document
Copy `_template.md` to a new file named after the principle or pattern.
Add the new file to the `documents` list in `index.yaml`.
