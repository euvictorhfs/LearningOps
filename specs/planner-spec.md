# Learning Planner Spec v1.0

## Purpose

Define the canonical, learner-approved learning contract for one study domain.

A Planner answers:

`What exactly have we agreed to learn in this domain, at what depth, with which competencies, constraints and evidence expectations?`

The Planner is not chat memory, not a prompt, not the PDI and not the curriculum model itself.

## Core rule

Each study domain may have one active approved Planner and a versioned history of prior Planners.

The active Planner belongs in the private Workspace under that domain. It must never be added as a global Project source because domain-specific plans can contaminate unrelated study chats.

## Lifecycle

`DISCOVER -> PROPOSE -> REFINE -> CLOSE -> REVIEW -> APPROVE -> PERSIST -> USE -> REVISE`

### Discover

The learner states a broad learning intent. The runtime identifies goals, constraints, desired outcomes, prior prerequisites that need demonstration, and likely curriculum options.

### Propose

LearningOps proposes a coherent initial formation rather than asking the learner to construct a syllabus manually.

### Refine

The learner can naturally add, remove, reorder or deepen topics and competencies.

Examples:

- `Include Snowflake.`
- `Remove Kubernetes.`
- `Go deeper on Iceberg and Delta.`
- `I do not want Machine Learning in this Planner.`

### Close

When scope is sufficiently coherent, the runtime proactively offers:

`Would you like to close your Planner and start studying?`

The learner may also explicitly say `Close my Planner` / `Feche meu Planner`.

Closing produces a reviewable candidate. It does not persist or activate the Planner by itself.

### Approve

The learner explicitly approves the candidate.

Example: `I approve the Planner.` / `Aprovo o Planner.`

### Persist

After approval, the runtime offers to persist it to the Workspace. A durable write requires actual repository capability and user authorization. Never claim persistence unless the write is verified.

### Use

Study runtime loads the current active Planner from Workspace whenever persisted state is available. Chat memory is only a convenience cache.

### Revise

Material scope changes create a new Planner version. Preserve history and rationale; do not silently rewrite the prior approved contract.

## Required Planner content

An approved Planner should contain, as applicable:

- planner id and version;
- domain id and display name;
- learner goal;
- desired outcomes;
- scope;
- out of scope;
- target competencies;
- prerequisite relationships;
- target breadth and depth;
- curriculum nodes / sequence references;
- priority topics;
- relevant learning-method choices;
- acceptance/evidence expectations;
- checkpoints or review triggers;
- retention expectations where relevant;
- initial Knowledge Graph relationships;
- PDI linkage rules;
- creation and approval timestamps;
- Core version used;
- approval status and lineage.

## Relationship to other specs

- Competency Model defines observable competencies.
- Curriculum defines how a domain curriculum is generated and sequenced.
- Planner selects and constrains the formation agreed for this learner and domain.
- PDI prioritizes what should be worked on now across current goals and gaps.
- Learning Method governs how the next intervention is taught.
- Evidence and Mastery determine what was actually demonstrated.

## Planner is not a prompt

The Planner is a portable structured artifact.

A model-specific prompt can be rendered from the Planner when needed:

`Structured Planner -> Runtime Adapter`

The adapter is disposable. The Planner remains canonical.

## No chat-memory dependency

If persisted Planner state exists, the runtime must not reconstruct the canonical plan solely from remembered conversation.

If Workspace access is unavailable, say that persisted Planner state could not be verified. Continue only with clearly labeled conversational context and do not claim the canonical Planner was loaded.

## Guardrails

- No Planner is globally authoritative outside its domain.
- Closing does not equal approval.
- Approval does not equal successful persistence.
- A Planner does not create mastery.
- Prior experience may change sequencing only after evidence or as an explicit unverified assumption that still preserves Zero Baseline.
- Planner changes that materially alter scope must be versioned.
- Study chats may refine their own Planner but must not alter shared Core policy.