---
category: architecture
last_updated: "YYYY-MM-DD"
documents:
  - file: clean-architecture.md
    covers: ["layers", "dependency rule", "use cases", "boundaries", "ports and adapters"]
  - file: solid.md
    covers: ["SRP", "OCP", "LSP", "ISP", "DIP", "single responsibility", "open closed"]
---

# Architecture Principles

This category defines the design principles applied in this project and how they are interpreted here.
These documents explain the *why* behind structural decisions and the rules that follow from them.

When an architecture principle conflicts with a convention, the principle takes precedence.
When an ADR conflicts with an architecture principle, the ADR takes precedence.

## Documents

### `clean-architecture.md`
Layer structure, dependency direction, and how domain, application, and infrastructure concerns are separated.
Load when: reasoning about where code belongs, reviewing layer boundaries, questioning dependency direction.

### `solid.md`
How the five SOLID principles are applied and enforced in this codebase.
Load when: designing new classes or interfaces, reviewing object-oriented design decisions.

---

## Adding a New Architecture Document
Copy `_template.md` to a new file named after the principle or pattern (e.g. `cqrs.md`, `event-driven.md`).
Add the new file to the `documents` list in this README's frontmatter.
