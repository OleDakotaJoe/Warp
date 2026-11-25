# Starting a new project

Use [EXPLORE](../modes/explore.md) to identify the user, problem, outcome, constraints, and non-goals. Do not manufacture architecture before the first useful behavior is understood.

1. Set the [project profile](../project-profile.md): owners, intended environment, source-of-truth homes, available commands, and current authorization boundaries.
2. Draft the first capability using [product](../templates/product.template.md) and [requirements](../templates/requirements.template.md) sections. For a small project these can be one document. Distinguish outcomes from mechanisms the project specifically requires.
3. Resolve meaningful alternatives in [DESIGN](../modes/design.md). Use [EXPERIMENT](../modes/experiment.md) for uncertainties that need measurements. Accept decisions before relying on them as implementation constraints.
4. Choose a thin end-to-end slice with explicit inputs, outputs, failure behavior, and acceptance. Add design detail and a test plan only where they clarify a real boundary or risk.
5. Execute the accepted slice in [STRICT MODE](../modes/strict.md), verify against the original requirements, and leave a [handoff](handoff.md).

Do not create empty documents for future departments or subsystems. The first deliverable is a useful, checked behavior plus enough durable intent to extend it faithfully. Select a stack based on the project, not this framework's implementation language.
