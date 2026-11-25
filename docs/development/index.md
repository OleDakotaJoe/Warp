# Development framework

Start with the [constitution](constitution.md) and [project profile](project-profile.md). They identify authority and local choices. The framework governs development sessions; it is not instructions for workers inside the application unless explicitly integrated there.

## Pick a route

| Situation | Read | First useful result |
| --- | --- | --- |
| New project | [Greenfield](guides/greenfield.md) | Accepted small outcome and first verifiable slice |
| Existing application | [Existing system](guides/existing-system.md) | Evidence-backed map of intent, behavior, and discrepancies |
| Unproven algorithm or architecture | [Research](guides/research.md) | Bounded experiment with an independent reference |
| Install, merge instructions, or upgrade | [Adoption](guides/adoption.md) | Explicit ownership map and preserved local rules |
| Day-to-day delivery | [Lifecycle](guides/lifecycle.md) | Task-sized recon, execution, and verification |
| New rule or changed direction | [Extending](guides/extending.md) | Reviewed amendment with scope and enforcement |
| Agent session restarts or changes tools | [Handoff](guides/handoff.md) | Durable state and next action, with evidence |

## Authority and document homes

| Home | Responsibility | Authority |
| --- | --- | --- |
| [Constitution](constitution.md) | Cross-project development invariants | Accepted framework policy within user authorization |
| [Profile](project-profile.md) | Local adoption, owners, commands, source-of-truth routing | Local policy when explicitly accepted |
| [Philosophies](philosophies/index.md) | Engineering constraints and verification expectations | Applicable accepted policy |
| [Capabilities](capabilities/index.md) | Product intent, requirements, contracts, and design | Accepted capability documents |
| [Decisions](decisions/index.md) | Why a design or policy changed | Accepted decision in its stated scope |
| Execution plans and evidence | What a change will do and what was measured | Plans cannot silently amend a contract |
| [Proposals](proposals/index.md) | Unaccepted ideas and experiments | Evidence or proposals, not requirements |
| [Archive](archive/index.md) | Superseded decisions and completed execution history | Historical, not current policy |

These homes may be links to existing project directories. Adopt one owner per concept; do not build a second authoritative documentation tree.

## Working materials

- [Modes](modes/index.md): short instructions to use with any coding assistant.
- [Templates](templates/index.md): copy only what the work needs.
- [Verification philosophy](philosophies/verification.md): distinguish conformance from usefulness.

Document states are `draft`, `accepted`, `superseded`, and `archived`. Record implementation state separately; an accepted design may still be unimplemented. Metadata is a claim of status, not evidence of approval. See the constitution for conflict handling.
