# LearningOps Core Agent Contract

LearningOps is the canonical system of record for deliberate learning and longitudinal professional development.

## Authority

Only the LearningOps control plane may approve structural changes to Core architecture, global specs/schemas, assessment and evidence rules, mastery computation, PDI, curriculum generation, knowledge-graph conventions, shared Workspace structure, runtime adapters or the Learning Cockpit.

Study contexts may learn, create domain-scoped records when authorized and propose improvements. They must not silently mutate global structures.

## Single Responsibility

Single Responsibility is a system invariant.

- `LearningOps` Core = reusable system methods, contracts, schemas, runtime and Cockpit.
- `LearningOps-workspace` = observed learner state and lineage.
- each specialized spec has one primary reason to change;
- the ChatGPT Project prompt orchestrates specs instead of duplicating them;
- UI renders state but does not manufacture evidence.

Use `specs/genai-architecture-spec.md` for Generative-AI architecture principles.

## Specialized responsibilities

- `learning-method-spec.md` — teaching methods and adaptive learning cycle.
- `competency-model-spec.md` — observable competence.
- `curriculum-spec.md` — learning-path generation and sequencing.
- `pdi-spec.md` — learner-specific development priorities.
- `evidence-spec.md` — evidence and lineage.
- `mastery-spec.md` — evidence-to-observed-mastery inference.
- `knowledge-graph-spec.md` — typed domain relationships and learner-graph separation.
- `session-runtime-spec.md` — ChatGPT study runtime.
- `evidence-based-resume-spec.md` — professional claims backed by validated evidence.
- `cockpit-spec.md` — evidence-transparent visualization.

## Zero baseline

Every new domain starts at `0% observed mastery`. Prior experience, title, credentials, self-assessment and conversational memory may identify what to test but never initialize mastery.

## Evidence lineage

No metric without evidence. No evidence without origin and time. No mastery change without lineage. Preserve assistance, confidence, counterevidence, privacy classification, corrections and relevant model/spec versions.

## ChatGPT runtime

Recommended adapter:

- Project: `LearningOps`;
- maintenance/governance chat: `Sistema LearningOps`;
- every other learning chat: named naturally after the field being studied.

A learner should not need bootstrap prompts. Verify GitHub access, load only relevant authoritative context and start the adaptive learning method.

## Governance

Structural changes follow:

`Problem -> Evidence -> Proposal -> Impact -> Spec -> Implementation -> Validation -> PR -> Merge`

Relevant prompt/spec changes should include regression evaluation where feasible.

## Source of truth

GitHub `main` is the persisted source of truth. Do not claim reads, writes, synchronization or deployment that did not occur.