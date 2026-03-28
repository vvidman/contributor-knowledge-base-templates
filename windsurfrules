# [Project Name]

## What is this project
<!-- 2-4 sentences: what does this project do, who uses it, what problem does it solve -->
TODO: Describe the project purpose here.

## Tech Stack
- **Backend**: TODO
- **Frontend**: TODO
- **Real-time**: TODO
- **ORM**: TODO
- **Database**: TODO
- **Architecture**: TODO
- **Testing**: TODO

## Solution Structure
```
src/[Project].Domain        - TODO
src/[Project].Application   - TODO
src/[Project].API           - TODO
src/[Project].UI            - TODO
docs/                       - Contributor knowledge base
```

## Coding Style
Non-trivial conventions: see `docs/conventions/README.md`

Rules that always apply without lookup:
<!-- Max 5 lines. Only things that are non-obvious and always relevant. -->
- TODO

## Permanent Prohibitions
<!-- Things that must never happen under any circumstance. -->
- Never TODO
- Never TODO

---

## Contributor Navigation Protocol
> This applies to both AI assistants and human contributors.

Before starting any task, read `docs/README.md` to discover relevant knowledge areas.
Then load only the category manifest and specific files relevant to the current task.

### Trigger Table
| Situation                            | Load first                       | Priority if conflict    |
|--------------------------------------|----------------------------------|-------------------------|
| Writing or reviewing code            | `docs/conventions/README.md`     | ADR > Conventions       |
| Making architectural decisions       | `docs/adr/README.md`             | ADR is authoritative    |
| Applying a design principle          | `docs/architecture/README.md`    | Architecture > Conventions |
| Working on a feature or domain area  | `docs/domain/README.md`          | Domain > Conventions    |
| Implementing a specified feature     | `docs/specs/README.md`           | Spec defines the scope  |
| Touching build, CI/CD, or tooling    | `docs/toolchain/README.md`       | Toolchain is isolated   |

### Conflict Resolution Priority
**ADR > Domain > Architecture > Conventions > Toolchain**

Specs are not standing rules — they define intent for a specific feature and are consumed during implementation only.

---

## File Conventions in `/docs`
- `README.md` files are **category manifests** — use them for navigation
- `_` prefixed files (e.g. `_template.md`) are **authoring templates** — never load as knowledge, never reference as a source
- All other `.md` files are **loadable knowledge documents**
