# Engineering philosophies

Read only the applicable subjects. Each policy states the behavior it protects and how to evaluate it. Product-specific rules belong in the project profile or owning capability, not in this portable core.

| Subject | Applicability |
| --- | --- |
| [AI collaboration](ai-collaboration.md) | Coding sessions, prompts, model handoffs |
| [Product intent](product-intent.md) | Scope, outcomes, non-goals, priorities |
| [Architecture](architecture.md) | Boundaries, domain logic, adapters, APIs |
| [Code quality](code-quality.md) | Naming, types, dependencies, maintainability |
| [Data and persistence](data-and-persistence.md) | Schemas, state, history, caches, migrations |
| [Verification](verification.md) | Acceptance, regression, research claims |
| [Interfaces and accessibility](interfaces-and-accessibility.md) | UI, CLI, SDK, errors, human interaction |
| [Security and privacy](security-and-privacy.md) | Trust, identity, external boundaries, publication |
| [Observability](observability.md) | Diagnostics, progress, costs, measurements |
| [Delivery and infrastructure](delivery-and-infrastructure.md) | Builds, configuration, deployment, recovery |
| [Tooling](tooling.md) | Developer commands, help, reproducibility |
| [Documentation](documentation.md) | Canonical ownership, lifecycle, audience, links |

Use the [philosophy template](../templates/philosophy.template.md) and [extension guide](../guides/extending.md) for additions. Requirements inside a policy apply when that policy's subject is in scope; adoption does not require every application to grow every subsystem.
