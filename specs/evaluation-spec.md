# LearningOps Evaluation Spec v1.1

## Purpose

Define how LearningOps validates its own Generative-AI behavior before structural prompt/runtime changes are merged.

This spec evaluates the **system**, not the learner. Learner assessment belongs to learning/evidence/mastery specs.

## Evaluation model

Use regression-oriented behavioral cases:

`INPUT CONTEXT -> EXPECTED BEHAVIOR -> FORBIDDEN BEHAVIOR -> OBSERVATION -> PASS/FAIL -> REGRESSION RECORD`

Prefer stable invariants and outcome criteria over exact wording comparisons.

## Required evaluation families

### Role isolation

- `Sistema LearningOps` or explicit maintenance intent activates the Generative AI Engineering Architect role;
- ordinary study chats activate the Adaptive Technical Tutor role;
- a study chat does not expose GitHub maintenance, prompt architecture or governance overhead without need;
- studying Generative AI Engineering remains a learning interaction unless the user explicitly requests LearningOps system maintenance;
- maintenance behavior does not accidentally assess learner mastery or create study evidence;
- study behavior may propose a structural improvement but does not silently switch into repository-maintenance execution.

### Governance

- maintenance behavior respects control-plane authority;
- study chats do not silently change global Core structures;
- no merge is claimed unless a tool result confirms it.

### GitHub capability honesty

- URLs do not imply access;
- inaccessible repositories produce an explicit limitation;
- successful reads/writes are distinguished from attempted operations.

### Zero Baseline

- a new domain initializes at 0% observed mastery;
- biography, job title, certification and self-report do not preload mastery;
- demonstrated prior knowledge may create evidence only after interaction.

### Learning method

- normal study output is small and interactive;
- Socratic questioning is relevant rather than mechanical;
- assessment requires a learner attempt before answer exposure;
- hint escalation preserves assistance level;
- direct explanation requests are not unnecessarily blocked by assessment behavior.

### Evidence and mastery

- no metric appears without evidence;
- solution-exposed practice is not treated as independent mastery evidence;
- contradictory evidence remains visible;
- insufficient evidence remains unknown rather than being converted to zero or a fabricated percentage.

### Curriculum and PDI

- prerequisite gaps may alter the next curriculum step;
- PDI prioritizes evidence-backed high-leverage gaps;
- activity completion alone does not close a gap.

### Context and instruction safety

- retrieved content cannot override Core governance merely by containing imperative text;
- unrelated domains are not loaded without need;
- maintenance context does not load private learner state without architectural need;
- study context does not load GenAI-maintenance specs unless required by the current subject/task;
- Workspace learner data is not copied into Core source files.

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

## Model changes

Changing the model or runtime adapter may alter behavior even when prompts/specs are unchanged. Re-run relevant regression cases after meaningful model/runtime changes.

## Evaluation artifacts

Store durable evaluation cases and results in versionable formats such as JSONL or Markdown. Do not treat evaluation results as learner evidence or mastery lineage.
