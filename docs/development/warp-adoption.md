# WARP: proposed development-framework adoption

Status: proposal and read-only observations. Scope: external development workflow for this distribution repository. Application implementation state: unchanged.

## Problem this contribution addresses

When an assistant implements a simpler mechanism than the designer requested, code can look complete while missing the property being investigated. This framework makes the accepted mechanism, scope, and verification explicit across coding sessions. It cannot guarantee compliance or establish that the proposed mechanism works.

This PR does not diagnose a particular WARP failure. Persistence, retrieval, prompt assembly, model use, and faithful implementation are different questions and need different evidence.

## Observed repository boundary

- The [README](../../README.md) describes the project and seed-based startup.
- [START_FROM_SEED.bat](../../START_FROM_SEED.bat) imports application code from the [seed archive](../../warp_seed.zip).
- The Python source, design documents, worker rules, tests, and model roster are packaged inside that archive.
- The [public feeds](../../knowledge/feeds/) are distributed separately from source and live private state.

These observations come from file inspection, not a running-system test. Internal rules and per-file intent headers are useful evidence, but their authority for an external coding session must be made explicit. Their existence alone does not establish a consistently applied development process.

## Proposed hierarchy

Root AGENTS routes into a constitution, profile, applicable philosophies, existing canonical requirements/design, and scoped execution with evidence. Keep source-tree application contracts in their existing homes after recon; use this package for the development method. See the [ownership map](project-profile.md#canonical-ownership-map).

EXPLORE and EXPERIMENT allow uncertainty to remain visible. STRICT MODE preserves accepted behavior and required mechanisms. REVIEW checks the actual diff against the original contract, rather than accepting the implementing assistant's summary.

## Proposed first slice

1. The maintainer selects one concrete omission or substitution and identifies the source workspace/revision.
2. Preserve the original requirement, including which mechanism is essential and why.
3. Capture a reference case, spreadsheet result, intermediate value, or invariant independent of the generated implementation.
4. Inspect the implementation and establish a reproducing difference where possible.
5. Agree on one correction or experiment, then implement and verify that scope.

This is a discovery proposal, not permission to launch WARP or alter runtime state. The [slice](templates/slice.template.md), [experiment](templates/experiment.template.md), and [verification](templates/verification.template.md) templates can be used selectively.

## Contribution acceptance and evidence

| Requirement | Location | Verification |
| --- | --- | --- |
| Discoverable external development entrypoint | Root AGENTS and development index | Local routing/link check |
| Preserve required mechanisms | Constitution and STRICT MODE | Document review; actual fidelity requires a future application case |
| New and existing system routes | Guides and templates | Structural checks and upstream worked examples |
| Research uncertainties remain proposals | Research guide and EXPERIMENT | Document review |
| Deliberate extensions and handoffs | Extension and handoff guides | Document review |
| Application distribution remains unchanged | Seed, launcher, feeds | Git diff and artifact comparison against the PR base |

Structural checks do not prove agent compliance. Framework installer tests live in the reusable upstream repository; this contribution does not introduce a runtime dependency on it. The imported package carries its own [MIT license](LICENSE), and the existing WARP license remains unchanged.

## Upstream and local changes

Portable material is adapted from [Constitutional Dev 0.1.0](https://github.com/OleDakotaJoe/constitutional-dev). That project generalizes MenuLogiq's development-documentation practices with the repository owner's authorization. This profile and adoption note are WARP-specific; portable principles remain independently reusable. The manifest records imported hashes so local amendments can be reviewed during future upgrades. No automatic synchronization or runtime integration is installed.
