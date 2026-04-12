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
Non-trivial conventions: see `docs/conventions/index.yaml`

Rules that always apply without lookup:
<!-- Max 5 lines. Only things that are non-obvious and always relevant. -->
- TODO

## Permanent Prohibitions
<!-- Things that must never happen under any circumstance. -->
- Never TODO
- Never TODO

---

## AI Navigation Protocol
> **AI agents only.** Human contributors: browse `README.md` files in each `docs/` subdirectory.

**Never read `README.md` files for navigation.** They are human-only documents and must not be used as AI navigation sources.

Navigate the knowledge base in three steps:
1. Read `docs/index.yaml` — identify the relevant category by matching task keywords against `triggers`
2. Read the category `index.yaml` listed under that category's `index` field — identify the specific document
3. Load only that document

### Trigger Table
| Situation                            | Category index                  | Priority if conflict       |
|--------------------------------------|---------------------------------|----------------------------|
| Writing or reviewing code            | `docs/conventions/index.yaml`   | ADR > Conventions          |
| Making architectural decisions       | `docs/adr/index.yaml`           | ADR is authoritative       |
| Applying a design principle          | `docs/architecture/index.yaml`  | Architecture > Conventions |
| Working on a feature or domain area  | `docs/domain/index.yaml`        | Domain > Conventions       |
| Implementing a specified feature     | `docs/specs/index.yaml`         | Spec defines the scope     |
| Touching build, CI/CD, or tooling    | `docs/toolchain/index.yaml`     | Toolchain is isolated      |

### Conflict Resolution Priority
**ADR > Domain > Architecture > Conventions > Toolchain**

Specs are not standing rules — they define intent for a specific feature and are consumed during implementation only.

---

## File Conventions in `/docs`
- `index.yaml` files are **AI navigation indexes** — the only files AI should read for navigation
- `README.md` files are **human-only navigation** — AI must never read these for navigation purposes
- `_` prefixed files (e.g. `_template.md`) are **authoring templates** — never load as knowledge, never reference as a source
- All other `.md` files are **loadable knowledge documents**