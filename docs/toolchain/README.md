> **Human navigation.** AI agents: use `docs/toolchain/index.yaml` — do not read this file for navigation.

# Toolchain

How-to guides for the build system, CI/CD pipelines, and development environment setup.
These documents are largely isolated — they do not conflict with conventions or ADRs.

## Documents

### `docker.md`
Container setup, local dev workflow, image build process.
Load when: setting up locally, modifying Docker config, debugging container issues.

### `ci-cd.md`
Pipeline configuration, deployment steps, environment variables.
Load when: modifying the build pipeline, setting up a new environment, debugging CI failures.

---

## Adding a New Toolchain Document
Copy `_template.md` to a new file named after the tool or process.
Add the new file to the `documents` list in `index.yaml`.
