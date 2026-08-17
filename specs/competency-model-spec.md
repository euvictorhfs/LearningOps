# Competency Model Spec v1.0

## Purpose

Define observable technical competence so LearningOps can design curricula, elicit evidence and estimate mastery without confusing exposure with capability.

## Design basis

LearningOps uses an Evidence-Centered Design-inspired separation:

- **competency model** — what capability is being claimed;
- **evidence model** — what observable behavior would support or weaken that claim;
- **task model** — what task can elicit that behavior.

Competencies must be observable and testable, not personality labels.

## Hierarchy

`Area -> Domain -> Subdomain -> Concept -> Mechanism -> Application -> Trade-off -> Observable competency`

A domain may omit layers that add no value, but every scored competency must have a stable id and evidence expectations.

## Competency statement

Prefer verbs that expose performance. Examples:

- explain a mechanism in own words;
- distinguish two easily confused concepts;
- select an approach under constraints;
- apply a mechanism without being told which pattern to use;
- diagnose a flawed system;
- design a solution;
- defend trade-offs;
- adapt a solution after requirements change;
- retrieve the principle after time has passed.

Avoid competencies such as `understands X` without an observable criterion.

## Capability dimensions

Track dimensions separately when relevant:

- **breadth** — navigation across the domain and recognition of relationships;
- **conceptual understanding** — mechanisms, causes and constraints;
- **application** — correct use in realistic tasks;
- **transfer** — use in a novel situation;
- **design** — construction of coherent solutions;
- **trade-off reasoning** — consequences and alternatives;
- **diagnosis** — identification of root causes and failure modes;
- **depth** — internals, edge cases, performance and implementation implications;
- **retrieval** — independent recovery without answer-shaped cues;
- **retention** — retrieval after meaningful elapsed time;
- **technical communication** — precise explanation and defense.

Generalist breadth and specialist depth must never be collapsed into one number.

## Development state

Use qualitative state as the primary interpretation:

- `unobserved` — no evidence;
- `exposed` — encountered, not demonstrated;
- `developing` — partial or assisted evidence;
- `applied` — independent application evidence exists;
- `robust` — repeated independent evidence across contexts;
- `specialist` — deep mechanism, diagnosis, design and adaptation evidence where the competency warrants it;
- `review_due` — prior evidence exists but retention or contradiction requires revalidation.

A state change requires lineage.

## Evidence expectations

Each competency should declare, when applicable:

- prerequisites;
- evidence types that support it;
- stronger evidence patterns;
- disconfirming evidence patterns;
- minimum context diversity;
- retention expectation;
- target depth for the learner goal.

## Task model

Tasks should vary enough to prevent memorizing the assessment shape. Use combinations of:

- explanation;
- comparison;
- counterexample;
- retrieval;
- practical case;
- requirement discovery;
- system design;
- architecture debugging;
- changed-constraint adaptation;
- deep-dive mechanism question.

## External frameworks

Domain authors may map competencies to external frameworks such as SFIA, certification objectives or role frameworks, but external mappings do not initialize mastery and do not override LearningOps evidence.