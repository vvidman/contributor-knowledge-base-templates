---
category: toolchain
last_updated: "YYYY-MM-DD"
documents:
  - file: docker.md
    covers: ["docker", "containers", "compose", "local dev environment"]
  - file: ci-cd.md
    covers: ["ci", "cd", "pipeline", "build", "deploy", "github actions"]
---

# Toolchain

How-to guides for the build system, CI/CD pipelines, and development environment setup.
These documents are largely isolated — they do not conflict with conventions or ADRs.

## Documents

### `docker.md`
Container setup, local dev workflow, image build process.
Load when: setting up locally, modifying Docker config, debugging container issues.

### `ci-cd.md`
Pipeline structure, deployment process, environment configs.
Load when: modifying CI config, setting up a new environment, debugging pipeline failures.

---

## Adding a New Toolchain Document
Copy `_template.md` to a new file named after the tool or concern (e.g. `vite.md`, `ef-migrations.md`).
Add the new file to the `documents` list in this README's frontmatter.
