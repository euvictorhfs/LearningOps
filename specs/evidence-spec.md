# Evidence & Lineage Spec v0.2.0

## Invariants

1. No metric exists without evidence.
2. No evidence exists without identifiable origin and timestamp.
3. No mastery change exists without lineage.
4. Self-assessment, credentials, title, prior experience and conversational memory are context, not mastery evidence.
5. A correct answer after substantial assistance is weaker than an unassisted attempt.
6. A single success does not imply durable mastery.
7. Observed workplace behavior is a candidate until LearningOps evaluates it.
8. Contradictory and negative evidence must remain visible.
9. The learner can contest, correct, withdraw consent or request deletion subject to applicable retention requirements.
10. Evidence supports capability claims, never judgments of human worth or hidden mental state.

## Evidence record

Each event should identify:

- `id`, `timestamp`, `domain`, `competency_id`;
- `session_id` or external source reference;
- `activity_type` and task reference;
- learner response or behavior summary;
- assistance level;
- result and evaluator rationale;
- provenance and Core version;
- confidence, limits and counterevidence;
- privacy classification and consent;
- metric effects when applicable;
- superseded record when correcting history.

## Assistance levels

- `none`;
- `clarification_only`;
- `hint_1`;
- `hint_2_plus`;
- `solution_exposed`;
- `substantially_generated`.

## Strength

Evidence strength is contextual. Prefer unaided retrieval, transfer to novel situations, design under changing constraints, diagnosis of flawed systems and durable recall. Workplace evidence may be strong for authentic application while still being confounded by collaboration, editing or unavailable context.

## External candidates

Use [thoughtops-evidence-contract.md](thoughtops-evidence-contract.md). Record the original candidate unchanged plus the LearningOps decision. Do not silently promote a candidate into a metric event.

## Metric lineage

Every change must answer what changed, when, why, from which evidence, under which Core and competency model versions, and what contradictory evidence was considered.

## Corrections

Append a superseding event or perform a versioned migration with rationale. Preserve auditability while honoring approved privacy and deletion obligations.
