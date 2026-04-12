> **Human navigation.** AI agents: use `docs/specs/index.yaml` — do not read this file for navigation.

# Feature Specifications

Feature specs define the scope, domain impact, and test expectations for a feature before implementation begins.
They are written by a reasoning partner (human or planning AI) and consumed by the implementation contributor.

Specs are **not standing rules**. They are point-in-time documents that describe intent for a specific feature.
Once a feature is fully implemented and merged, its spec is kept for historical reference but is no longer authoritative.

## Status Vocabulary
- `draft` — being written, not ready for implementation
- `ready` — approved, implementation can begin
- `in-progress` — actively being implemented
- `done` — implemented, merged, kept for reference only

## Documents

### `example-feature.md`
Example spec demonstrating structure and required fields.

---

## Adding a New Spec
Copy `_template.md` to a new file named after the feature (e.g. `user-login.md`).
Add the new file to the `documents` list in `index.yaml`.
