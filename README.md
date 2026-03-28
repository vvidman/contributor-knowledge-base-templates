# AI-Augmented Contributor Knowledge Base — Template Repository

A structured, tool-agnostic knowledge base template for software projects.
Designed for teams and solo developers who use AI coding assistants alongside human contributors.

---

## What is this?

This repository is a **template** for setting up a layered contributor knowledge base from day one of a project. It defines a consistent structure for project documentation that is useful for both:

- **Human contributors** — onboarding, architectural guidance, coding standards, domain understanding
- **AI coding assistants** — navigable, on-demand context loading to minimize unnecessary token usage

The core idea is simple: an AI assistant should know *what exists* without having to load *everything*. Knowledge is organized into categories, each with a manifest (`README.md`) that describes what is inside. The assistant loads only what is relevant to the current task.

---

## Design Principles

### 1. Minimal initial context
The root instruction file is intentionally lean. It contains only what is *always* relevant: project identity, tech stack, solution structure, permanent rules, and navigation instructions. Everything else lives in `docs/` and is loaded on demand.

### 2. Three-tier knowledge hierarchy
```
Tier 1 — Root instruction file     (always loaded by the AI tool)
Tier 2 — Category manifests        (loaded when a category is relevant)
Tier 3 — Specific knowledge files  (loaded only when directly needed)
```

This hierarchy keeps the working context small and precise.

### 3. Human and AI contributors are equal audiences
Nothing in this structure is AI-only. Every document should be readable and useful to a human developer as well. The navigation protocol applies to both.

### 4. Tool-agnostic content, tool-specific entry points
Each AI tool has its own instruction file name and location. The content across all of them is identical — only the filename differs. You keep the one you use and delete the rest.

### 5. Templates are not knowledge
Files prefixed with `_` (e.g. `_template.md`) are authoring scaffolds. They define the expected structure for new documents in their category. They must never be loaded as knowledge by an AI assistant, and they must never be committed as real content.

---

## Repository Structure

```
/
├── CLAUDE.md                          ← Claude Code (Anthropic)
├── AGENTS.md                          ← Codex CLI (OpenAI)
├── .cursorrules                       ← Cursor
├── .windsurfrules                     ← Windsurf
├── .github/
│   └── copilot-instructions.md        ← GitHub Copilot
│
└── docs/
    ├── README.md                      ← Master knowledge manifest
    │
    ├── conventions/
    │   ├── README.md                  ← Category manifest
    │   ├── _template.md               ← Authoring template
    │   └── [topic].md
    │
    ├── adr/
    │   ├── README.md
    │   ├── _template.md
    │   └── [NNN-title].md
    │
    ├── domain/
    │   ├── README.md
    │   ├── _template.md
    │   └── [area].md
    │
    ├── toolchain/
    │   ├── README.md
    │   ├── _template.md
    │   └── [tool].md
    │
    ├── architecture/
    │   ├── README.md
    │   ├── _template.md
    │   └── [principle].md
    │
    └── specs/
        ├── README.md
        ├── _template.md
        └── [feature-name].md
```

---

## How to Use This Template

### Step 1 — Create your repository from this template
Use the **"Use this template"** button on GitHub, or clone and reinitialize:
```bash
git clone https://github.com/your-org/this-template my-project
cd my-project
rm -rf .git && git init
```

### Step 2 — Keep only the instruction file for your AI tool
Each AI coding assistant reads from a specific file. Keep only the one that matches your tool and delete the others:

| AI Tool | File to keep |
|---|---|
| Claude Code | `CLAUDE.md` |
| Codex CLI | `AGENTS.md` |
| GitHub Copilot | `.github/copilot-instructions.md` |
| Cursor | `.cursorrules` |
| Windsurf | `.windsurfrules` |

### Step 3 — Fill in the root instruction file
Open your chosen instruction file and replace every `TODO` placeholder:
- Project name and description
- Tech stack
- Solution structure
- Coding style rules specific to your project
- Permanent prohibitions

### Step 4 — Build out `docs/` as the project grows
Start with what you know. You do not need to fill every category on day one.

A suggested starting order:
1. `docs/architecture/` — define your architectural principles before writing any code
2. `docs/conventions/` — establish coding standards early
3. `docs/domain/` — add domain knowledge as features are designed
4. `docs/adr/` — record decisions as they are made
5. `docs/toolchain/` — document infrastructure when it is set up
6. `docs/specs/` — write feature specs before each implementation

### Step 5 — Use templates when creating new documents
Every category has a `_template.md`. Always copy it (never edit it directly) when creating a new document:
```bash
cp docs/specs/_template.md docs/specs/user-authentication.md
```

### Step 6 — Keep manifests up to date
When you add a new document to a category, update the `README.md` frontmatter in that category to include the new file. This is how the AI assistant discovers that the document exists.

---

## Conflict Resolution Priority

When instructions from different categories appear to conflict, the following priority order applies:

**ADR > Domain > Architecture > Conventions > Toolchain**

Specs are not authoritative references — they describe intent for a specific feature and are consumed during implementation, not used as standing rules.

---

## Contributing to This Template

If you improve this structure in your own project and believe the change would benefit others, consider opening a PR against the original template repository. Changes to `_template.md` files and `README.md` manifests are especially welcome.
