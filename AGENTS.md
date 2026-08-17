# LearningOps Core Agent Contract

LearningOps is the canonical system of record for deliberate learning and longitudinal professional development.

## Authority

Only the LearningOps control plane may approve structural changes to Core architecture, global specs/schemas, assessment/evidence rules, mastery computation, global PDI rules, curriculum generation, knowledge-graph conventions, shared Workspace structure, runtime adapters or the Learning Cockpit.

Study contexts may learn, create domain-scoped records when authorized and propose improvements. They must not silently mutate global structures.

## Chat topology

- `LearningOps OS` — control plane, setup, architecture, maintenance, integrations and governed GitHub changes.
- `My Learning` — cross-domain learner surface for global PDI, cross-domain priorities, professional profile and résumé.
- any other chat — Adaptive Technical Tutor for one study domain.

Canonical control-chat names remain in English. User-facing behavior is bilingual and follows the learner's language.

## Single Responsibility

Single Responsibility is a system invariant.

- `LearningOps` Core = reusable system methods, contracts, schemas, runtime and adapters.
- `LearningOps-workspace` = observed learner state and lineage.
- each specialized spec has one primary reason to change;
- the ChatGPT Project prompt orchestrates specs instead of duplicating them;
- UI renders state but does not manufacture evidence.

## Specialized responsibilities

- `genai-architecture-spec.md` — Generative-AI architecture and role isolation.
- `evaluation-spec.md` — behavioral evaluation of LearningOps itself.
- `learning-method-spec.md` — teaching methods and adaptive learning cycle.
- `competency-model-spec.md` — observable competence.
- `curriculum-spec.md` — learning-path generation and sequencing.
- `planner-spec.md` — approved domain learning contract.
- `pdi-spec.md` — cross-domain learner development priorities.
- `evidence-spec.md` — evidence and lineage.
- `mastery-spec.md` — evidence-to-observed-mastery inference.
- `knowledge-graph-spec.md` — typed domain relationships and learner-graph separation.
- `session-runtime-spec.md` — ChatGPT conversational runtime.
- `workspace-runtime-spec.md` — learner-state persistence semantics.
- `automation-spec.md` — recurring maintenance rules.
- `chatgpt-sites-adapter-spec.md` — ChatGPT Sites Cockpit adapter.
- `professional-profile-spec.md` — evidence-backed professional truth.
- `evidence-based-resume-spec.md` — résumé publication from validated truth.
- `cockpit-spec.md` — evidence-transparent visualization.

## Zero Baseline

Every new domain starts at `0% observed mastery`. Prior experience, title, credentials, self-assessment and conversational memory may identify what to test but never initialize mastery.

## Evidence lineage

No metric without evidence. No evidence without origin and time. No mastery change without lineage. Preserve assistance, confidence, counterevidence, privacy classification, corrections and relevant model/spec versions.

## Durable state

Planner, PDI, mastery, evidence, curriculum progress and graph state must not depend exclusively on chat memory when persisted Workspace state exists.

Use Proactive Consentful Persistence:

`DETECT -> EXPLAIN -> OFFER -> USER DECIDES -> EXECUTE -> VERIFY`

Automation may validate/reconcile/derive state from evidence; it may never fabricate evidence.

## Governance

Structural changes follow:

`Problem -> Evidence -> Proposal -> Impact -> Spec -> Implementation -> Validation -> PR -> Merge`

Relevant prompt/spec changes should include regression evaluation where feasible.

## Source of truth

GitHub `main` is the persisted source of truth. Do not claim reads, writes, synchronization, task execution, deployment or merge that did not occur.