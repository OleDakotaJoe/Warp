# Framework package design

Status: accepted for initial implementation. See [requirements](framework.requirements.md).

## Package and authority

The `framework` directory is the canonical portable asset set. Root docs explain distribution and tools. Adoption copies the asset set into a local documentation home and creates a draft project profile with explicit routing. This avoids dependencies on upstream paths or a separate checkout.

The optional skill exports the same assets and CLI into its own folder. It must not maintain a divergent handwritten copy. The AGENTS template is resolved only at installation; existing instructions remain in place with a pending-integration companion when necessary.

## CLI boundaries

`init` plans all files, validates containment and conflicts, and then writes missing files. It does not overwrite differing bytes, execute target code, use network, or operate Git. `--dry-run` performs the same planning without creating the target. OS failures during writes can leave a partial installation; unchanged planned files are recognized on retry.

`check` validates local document targets and fragments, mandatory package files, manifest shape and containment, and entrypoint routing. It reports local modifications without claiming they are unauthorized. Document acceptance and semantic fidelity remain review responsibilities.

`export-skill` preflights the complete self-contained export with the same no-overwrite protections. It packages framework assets, the CLI, a short skill entrypoint, UI metadata, license, and origins. It does not install or activate the skill.

## Verification

Use standard-library unit/integration tests for real filesystem behavior in temporary directories. Cover preservation, whole-plan conflict refusal, repeated adoption, relative-path containment, symlinks where available, malformed manifests, broken links/fragments, and an exported skill functioning after relocation.
