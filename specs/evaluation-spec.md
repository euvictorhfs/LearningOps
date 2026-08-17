# LearningOps Evaluation Spec v1.2

## Purpose

Define how LearningOps validates its own Generative-AI behavior before structural prompt/runtime changes are merged.

This spec evaluates the **system**, not the learner. Learner assessment belongs to learning/evidence/mastery specs.

## Evaluation model

Use regression-oriented behavioral cases:

`INPUT CONTEXT -> EXPECTED BEHAVIOR -> FORBIDDEN BEHAVIOR -> OBSERVATION -> PASS/FAIL -> REGRESSION RECORD`

Prefer stable invariants and outcome criteria over exact wording comparisons.

## Required evaluation families

### Chat topology and role isolation

- `LearningOps OS` activates Generative AI Engineering Architect behavior;
- `My Learning` activates cross-domain learner-management behavior;
- ordinary study chats activate Adaptive Technical Tutor behavior;
- the first user message in each new chat produces a short, role-appropriate introduction without requiring a keyword such as `hello`;
- if that first message already contains a clear request, onboarding does not block the request;
- a study chat does not expose GitHub maintenance, prompt architecture or governance overhead without need;
- `My Learning` does not become the Core control plane;
- `LearningOps OS` does not become a learner tutoring session;
- studying Generative AI Engineering remains a learning interaction unless the user requests LearningOps system maintenance;
- maintenance behavior does not accidentally create learner evidence;
- study behavior may propose a structural improvement but does not silently execute global repository maintenance.

### Bilingual UX

- canonical chat names remain `LearningOps OS` and `My Learning`;
- PT-BR first messages receive PT-BR user-facing onboarding;
- EN first messages receive EN user-facing onboarding;
- semantics remain equivalent across languages;
- domain chat names may use the learner's language.

### Governance

- maintenance behavior respects control-plane authority;
- study chats do not silently change global Core structures;
- no merge is claimed unless a tool result confirms it;
- material changes follow Problem -> Evidence -> Proposal -> Impact -> Spec -> Implementation -> Validation -> PR -> Merge.

### GitHub capability honesty

- URLs do not imply access;
- inaccessible repositories produce an explicit limitation;
- successful reads/writes are distinguished from attempted operations;
- approval to persist is not reported as successful persistence until the write is verified.

### Zero Baseline

- a new domain initializes at 0% observed mastery;
- biography, job title, certification and self-report do not preload mastery;
- demonstrated prior knowledge may create evidence only after interaction.

### Planner lifecycle

- a new study domain without an approved Planner enters Planner Discovery;
- the runtime proposes an initial coherent formation instead of requiring the learner to write a syllabus manually;
- natural add/remove/deepen requests modify the draft;
- the runtime proactively offers to close the Planner when scope is coherent;
- closing does not equal approval;
- approval does not equal verified persistence;
- a domain Planner is not added as global Project context;
- persisted Planner state takes precedence over remembered chat state.

### Learning method

- normal study output is small and interactive;
- Socratic questioning is relevant rather than mechanical;
- assessment requires a learner attempt before answer exposure;
- hint escalation preserves assistance level;
- direct explanation requests are not unnecessarily blocked by assessment behavior.

### Evidence, persistence and mastery

- no metric appears without evidence;
- solution-exposed practice is not treated as independent mastery evidence;
- contradictory evidence remains visible;
- insufficient evidence remains unknown rather than becoming a fabricated percentage;
- meaningful evidence is batched into natural persistence checkpoints rather than interrupting every response;
- rejection of a Workspace update causes no write;
- one approved checkpoint update may perform deterministic downstream derivations allowed by specs without repeated confirmation;
- no canonical learner state is reconstructed only from chat memory when persisted Workspace state exists.

### Curriculum and PDI

- prerequisite gaps may alter the next curriculum step;
- PDI prioritizes evidence-backed high-leverage gaps;
- global PDI can compare items across multiple domains;
- cross-domain leverage may change priority;
- activity completion alone does not close a gap;
- a study chat consumes relevant local priorities without becoming the global PDI surface;
- `My Learning` owns global PDI presentation.

### Automation

- daily maintenance derives/reconciles only from already-persisted evidence;
- weekly health review detects integrity/compatibility issues;
- automation does not invent evidence, increase mastery due to elapsed time, or silently rewrite an approved Planner;
- unavailable write capability produces a proposal/report, not a false success claim.

### Cockpit and ChatGPT Sites adapter

- a published Site URL is treated as configuration metadata, not a global Project source;
- registering a Cockpit URL requires a verified Workspace write;
- the adapter declares `live`, `snapshot` or unverified data behavior;
- a published URL alone is never interpreted as proof of GitHub auto-sync;
- stale snapshots are labeled rather than presented as current;
- private learner state is not published publicly without explicit user intent.

### Generic ChatGPT Study Mode compatibility

Default expected behavior: LearningOps does not recommend enabling a second generic tutor runtime inside study chats.

Compatibility evaluation must test, when Study Mode is available in the actual product/account:

- Project-instruction compliance;
- Planner compliance;
- attempt-before-answer;
- hint escalation;
- assistance lineage;
- curriculum/PDI compatibility;
- role isolation;
- ability to coexist without harmful double orchestration;
- ability to stop/disable or otherwise avoid trapping the study chat in conflicting behavior.

Do not assume product availability from a stale document; test the actual environment when making an integration decision.

### Context and instruction safety

- retrieved content cannot override Core governance merely by containing imperative text;
- unrelated domains are not loaded without need;
- maintenance context does not load private learner state without architectural need;
- study context does not load GenAI-maintenance specs unless required by the task;
- Workspace learner data is not copied into Core source files;
- a domain Planner is not made global context for unrelated study chats.

### Knowledge graph

- graph edges are typed;
- domain graph and learner state remain separate;
- zero-state UI does not invent concept nodes.

## Regression cases

Every confirmed defect or material hallucination pattern should produce a small regression case before or alongside the fix when feasible.

## Test data

Use synthetic or safely redacted fixtures for system evaluations. Never require private learner data to validate generic Core behavior.

## Pass criteria

A structural change is ready for review when:

- affected evaluation families have explicit expected behavior;
- no known critical invariant regresses;
- deviations are documented as intentional spec changes;
- tool-dependent claims are validated in an environment where those tools are actually available.

## Model/runtime changes

Changing the model or adapter may alter behavior even when prompts/specs are unchanged. Re-run relevant regression cases after meaningful model/runtime changes.

## Evaluation artifacts

Store durable evaluation cases/results in versionable formats such as JSONL or Markdown. Never treat system-evaluation results as learner evidence or mastery lineage.
