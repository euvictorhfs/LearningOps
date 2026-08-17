# PDI Spec v1.0

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
- communication.

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
- gap statement;
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

## Relationship to curriculum

Curriculum answers `what capabilities and sequence form the domain?`.

PDI answers `given this learner's goal and evidence, what should we work on next?`.

The PDI may temporarily reorder curriculum nodes when a gap has higher leverage.