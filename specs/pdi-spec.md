# PDI Spec v1.1

## Purpose

Define the LearningOps Individual Development Plan as a living, evidence-driven development loop tied to a learning goal.

PDI is not a static wish list and not a performance rating. It translates desired capability into prioritized development actions and is continuously revised from evidence.

## Method

LearningOps uses the loop:

`GOAL -> TARGET COMPETENCIES -> CURRENT EVIDENCE -> GAP -> PRIORITY -> INTERVENTION -> EVIDENCE -> REVIEW -> ADAPT`

This combines goal alignment, competency-based development and continuous feedback.

## Required fields

### Goal

The capability outcome the learner wants to reach, with scope and relevant constraints.

### Target competencies

Competencies required to achieve the goal, including target breadth/depth where applicable.

### Current observed state

Evidence-backed state only. Unknown remains unknown; it is not filled from title, credentials or self-confidence.

### Gap

Difference between target capability and observed evidence. Gaps may be:

- prerequisite;
- conceptual;
- retrieval;
- application;
- transfer;
- design;
- diagnostic;
- depth;
- retention;
- communication;
- knowledge debt.

### Knowledge debt

Knowledge debt is a known dependency the learner can currently work around but has not demonstrated at the depth required by the goal.

Examples:

- can use Spark conceptually but cannot explain shuffle behavior;
- can select a Lakehouse but lacks the metadata/table-format mechanisms needed to defend the choice;
- can complete a task with a framework but cannot diagnose failure below the abstraction.

Knowledge debt does not automatically block progression. Its priority depends on prerequisite leverage, recurrence, risk and the learner goal.

### Priority

Rank gaps using:

`goal impact x prerequisite leverage x evidence weakness x recurrence x risk`

Do not prioritize by novelty alone.

### Intervention

Choose the smallest useful action likely to generate learning and evidence, such as:

- microlearning;
- retrieval practice;
- deliberate-practice exercise;
- deep dive;
- problem case;
- system design;
- debugging;
- visual explanation;
- spaced review;
- transfer task.

### Success evidence

Define before the intervention what observable behavior would indicate progress.

### Review

After evidence, decide whether to:

- continue;
- deepen;
- revisit a prerequisite;
- schedule retention review;
- change priority;
- mark the gap sufficiently addressed for the current goal.

## PDI item

Each active PDI item should include:

- `id`;
- target competency ids;
- gap type and statement;
- evidence references;
- priority and rationale;
- next intervention;
- expected evidence;
- status;
- created/updated timestamps;
- review trigger or date.

## Guardrails

- A PDI does not create mastery.
- Completing an activity does not close a gap without evidence.
- PDI priorities can change when contradictory evidence appears.
- Keep the active PDI small; prefer a few high-leverage priorities over a long backlog.
- Separate development needs from judgments of identity, seniority or human worth.
- Do not turn every weakness into an active PDI item; only persist development work relevant to the current objective or systemic prerequisite risk.

## Relationship to curriculum

Curriculum answers `what capabilities and sequence form the domain?`.

PDI answers `given this learner's goal and evidence, what should we work on next?`.

The PDI may temporarily reorder curriculum nodes when a gap has higher leverage.