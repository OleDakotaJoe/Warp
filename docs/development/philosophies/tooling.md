# Developer tooling

Applies to command wrappers, generators, scaffolding, validation, and local automation.

- Prefer an obvious documented command with focused options over many hidden variants. Keep help output synchronized with behavior.
- State writes, network use, environment assumptions, skips, and defaults. Offer preview or dry-run when meaningful for bulk changes.
- Preserve existing files and user work. Scaffolders should detect conflicts before writing and explain recovery. Never hide overwrite behind a convenience default.
- Use dependency-free or existing tooling where suitable. Installing a documentation workflow must not start the application or mutate external infrastructure.
- Validate the failure paths that protect user data, not just the successful scaffold.
- Generated artifacts must identify their source and version. Repeated generation must not silently overwrite accepted local amendments.
- Keep debug harnesses and evidence collection separate from normal product dependencies unless explicitly designed otherwise.

Verification: exercise commands, help, targeted operation, previews, conflict refusal, and generated output in isolated directories. Say which checks are structural and which exercise behavior.
