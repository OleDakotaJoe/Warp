# WARP development profile

Status: proposed local adoption, pending maintainer review of this PR. Framework source version: 0.1.0. Route: existing system with research components.

This profile and the root [agent entrypoint](../../AGENTS.md) organize external development sessions. They do not change WARP's runtime, internal workers, training, model roster, or distribution contents. Adoption is a proposed workflow, not a claim that a reported defect is fixed.

## Project and decision authority

The project maintainer owns WARP's product and architectural decisions. Contributors and coding assistants work within the current task and accepted contracts. Current explicit user instructions retain precedence. The initial contribution is documentation-only on a feature branch; it does not authorize a merge, deployment, seed rebuild, or publication of application state.

## Canonical ownership map

| Subject | Current home | Interpretation |
| --- | --- | --- |
| Public distribution and project description | [Repository README](../../README.md) | Maintainer's public description; capability claims still need evidence |
| Distribution payload | [Seed archive](../../warp_seed.zip) | Packaged code snapshot; not a directly editable source tree |
| Public knowledge distribution | [Feeds](../../knowledge/feeds/) | Published records; presence does not establish model capability |
| Development method | [Constitution](constitution.md), [philosophies](philosophies/index.md), [modes](modes/index.md) | Proposed external development workflow in this PR |
| Adoption evidence and first task | [WARP adoption note](warp-adoption.md) | Observations, limits, and proposed next slice |
| Application requirements, design, and decisions | Source headers and design/docs inside the seed | Inspect and reconcile with the maintainer before treating any as the current accepted contract |
| New accepted application contracts | Existing source-tree owner docs when identified | Link them here after recon; avoid a second application documentation tree |

The framework's [package requirements](capabilities/framework.requirements.md) and [package design](capabilities/framework.design.md) describe the reusable framework, not WARP's application requirements.

## Source, distribution, and live state

This checkout exposes a launcher, archive, and feeds. Source inspection may unpack the archive into a separate review directory without running it. Do not start batch files, application loops, restart watchers, model downloads, publication steps, or training simply to inspect documentation.

When development happens in the maintainer's full source tree, adopt or merge an entrypoint there explicitly and route to that tree's real owners. Adding files here does not inject instructions into the archive or running system. Seed regeneration and clean-machine validation are separate tasks with their own acceptance.

## Commands and verification

Documentation may be checked using a local checkout of the reusable [Constitutional Dev framework](https://github.com/OleDakotaJoe/constitutional-dev):

```sh
python /path/to/constitutional-dev/tools/framework.py check --target /path/to/Warp
```

The check is structural. It validates local links, package shape, manifest paths, and root agent routing; it does not verify WARP's behavior, mathematical claims, or semantic compliance. No application test suite is directly exposed in this distribution checkout. Inspect the seed's documented commands and dependencies before deciding which application checks are appropriate in a future source change.

## First useful development task

Choose one instance where generated code omitted or replaced a required mechanism. Record the original requirement, actual source location, independent reference example, and difference in behavior or intermediate transformation. Use [existing-system recon](guides/existing-system.md) and [research](guides/research.md) as appropriate. Do not label the issue retrieval failure, training regression, or design infeasibility without evidence distinguishing them.

After the maintainer accepts the relevant contract, use [STRICT MODE](modes/strict.md) for one focused implementation slice and require a [requirement/evidence table](templates/verification.template.md).

## Local amendments and open decisions

No application-specific philosophy or architecture has been replaced by this contribution. Maintainer review should establish the actual source workspace, accepted design owners, preferred application test environment, and whether this entrypoint is to be carried into future seeds. Record these decisions here or link their canonical owners using the [extension process](guides/extending.md).
