# Evidence & Lineage Spec v0.1.0

## Invariants

1. No metric exists without evidence.
2. No evidence exists without identifiable origin and timestamp.
3. No mastery increase or decrease exists without lineage.
4. Self-assessment, credentials, title and prior experience are context, not mastery evidence.
5. A correct answer after substantial hints is weaker evidence than an unassisted first attempt.
6. A single correct answer does not imply durable mastery.

## Evidence record

Each evidence event should identify:

- `id`;
- `timestamp`;
- `domain`;
- `session_id`;
- `competency_id`;
- `activity_type`;
- `prompt_or_task_ref`;
- `learner_response_summary`;
- `assistance_level`;
- `result`;
- `evaluator_rationale`;
- `source`;
- `metric_effects` when applicable.

## Assistance levels

Recommended values:

- `none`;
- `clarification_only`;
- `hint_1`;
- `hint_2_plus`;
- `solution_exposed`.

## Evidence strength

Evidence strength is contextual, not a universal score. Prefer stronger weight for:

- unaided retrieval;
- transfer to a novel scenario;
- system design under changing constraints;
- correct diagnosis of intentionally flawed designs;
- durable recall after an interval.

## Metric lineage

When a metric changes, the ledger must make it possible to answer:

- what changed;
- when;
- why;
- from which evidence;
- under which Core version;
- under which competency model version.

## Corrections

Do not rewrite history silently. Corrections should append a superseding event or be made through a versioned migration with rationale.
