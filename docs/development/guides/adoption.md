# Adoption, integration, and upgrades

The portable package can be read directly or copied into an existing repository. Automated adoption is optional. It does not create branches, commits, issues, network integrations, or runtime workers.

## Initial adoption

Run the scaffolder's preview from the framework checkout:

```sh
python tools/framework.py init --target /path/to/project --name "Project Name" --track existing --dry-run
python tools/framework.py init --target /path/to/project --name "Project Name" --track existing
```

From a self-contained exported skill instead, use `python /path/to/constitutional-dev/scripts/framework.py` with the same subcommands and flags. The exported package has no `tools` directory. Resolve the command from the package you actually have, not from the target application's working directory.

Use `greenfield`, `existing`, or `research`. The default destination is `docs/development`; `--framework-path` selects another relative directory. The tool refuses a destination outside the target or through a symlink, and preflights all file conflicts before writing. It never overwrites a differing file.

If the root has no `AGENTS.md`, the tool creates the [entrypoint template](../templates/AGENTS.template.md) with real relative paths. If root instructions already exist, it writes `AGENTS.constitutional-dev.md` and marks integration pending in `.constitutional-dev.json`. Review precedence and add a link from the existing entrypoint. Do not replace local instructions blindly. The checker requires an actual local link to the framework's index and constitution, not a filename mentioned in a code block.

The manifest's `entrypoint` and `integration_at_install` describe the installation event. They do not track current review status and need no update after routing is merged. The checker assesses current root links directly. Completing the draft profile is expected customization; changes to portable policy deserve a separate amendment review.

The [project profile](../project-profile.md) is the local adoption record. The install starts it as draft: fill authoritative homes, owners, commands, policies, and unresolved decisions, then record acceptance through the project's normal review. The scaffolder does not accept documents on the maintainer's behalf. A structural check passing does not accept the profile.

## Layer local policy

Keep the portable invariant set small. Local stack, branching, naming, test commands, accessibility targets, and approval conventions belong in the profile or linked owner docs. Requirements and design may remain at existing paths. Record amendments with scope and rationale using the [extension process](extending.md).

## Distribution-only repositories

When the checkout ships an archive, treat that archive as an artifact. Inspect source in a separate review location without executing it. Installing these docs does not update embedded code, regenerate a seed, train a model, or change runtime worker policy. Development in an unpacked source tree needs its own reviewed entrypoint and ownership map. Keep that adoption distinct from the public distribution.

## Upgrades

The manifest records source version and installed hashes. The checker reports local modifications for review; an amendment is not automatically an error. There is intentionally no destructive auto-upgrade.

Export a new version into a fresh staging directory, compare it with the adopted package, merge relevant changes on a branch, retain local decisions, update the profile and manifest hashes only after review, and run checks. Do not rerun init as an overwrite mechanism. Downstream changes may be proposed upstream, with product-specific material removed.

## Removal

Review the manifest and local changes before removing installed files. Remove or update entrypoint links as part of the same change; preserve accepted requirements and decisions that now depend on the framework. Removal never implies deleting application state.
