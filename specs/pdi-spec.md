# PDI Spec v1.2

## Purpose

Define the LearningOps Individual Development Plan as a living, evidence-driven, cross-domain prioritization loop.

PDI is not a static wish list, not a performance rating and not one isolated plan per study chat. Domain-local development items may exist, but the canonical learner prioritization is global across active goals and domains.

The preferred conversational interface for global PDI is `My Learning`.

## Method

LearningOps uses:

`GOAL -> TARGET COMPETENCIES -> CURRENT EVIDENCE -> GAP -> PRIORITY -> INTERVENTION -> EVIDENCE -> REVIEW -> ADAPT`

## Scope model

### Domain-local PDI context

A study domain may maintain gaps and candidate interventions tied to its Planner and evidence.

### Global PDI

Global PDI ranks active development needs across domains and professional goals.

It answers:

`Given all current goals, Planners, evidence and dependencies, what should this learner work on next?`

Do not assume every domain receives equal priority.

## Required fields

### Goal

Capability outcome, scope and constraints. A global PDI may reference multiple goals.

### Target competencies

Competencies required for the goals, including breadth/depth where applicable.

### Current observed state

Evidence-backed state only. Unknown remains unknown; never fill from title, credentials, self-confidence or chat memory.

### Gap

Difference between target capability and observed evidence. Gap types include:

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

A known dependency the learner can currently work around but has not demonstrated at the depth required by current goals.

Knowledge debt does not automatically block progression. Priority depends on leverage, recurrence, risk and goals.

### Priority

Rank using:

`goal impact x prerequisite leverage x evidence weakness x recurrence x risk`

For global prioritization, also consider cross-domain leverage: a prerequisite that unlocks several active domains may outrank a narrow local weakness.

Do not prioritize by novelty alone.

### Intervention

Choose the smallest useful action likely to produce learning and evidence, such as:

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

Define observable success before the intervention where practical.

### Review

After evidence, decide whether to:

- continue;
- deepen;
- revisit a prerequisite;
- schedule retention review;
- change global/domain priority;
- mark the gap sufficiently addressed for the current goal.

## PDI item

Each item should include:

- `id`;
- domain id(s) when applicable;
- goal references;
- target competency ids;
- gap type and statement;
- evidence references;
- priority and rationale;
- cross-domain leverage where relevant;
- next intervention;
- expected evidence;
- status;
- created/updated timestamps;
- review trigger/date.

## Guardrails

- PDI does not create mastery.
- Completing an activity does not close a gap without evidence.
- Contradictory evidence may change priority.
- Keep the active global PDI small; prefer a few high-leverage priorities over a long backlog.
- Separate development needs from identity, seniority or human-worth judgments.
- Do not turn every weakness into an active item.
- Do not require a dedicated PDI chat: `My Learning` is the cross-domain surface; study chats consume relevant domain priorities.

## Relationships

Curriculum: `what capabilities and sequence form the domain?`

Planner: `what has this learner agreed to study in this domain?`

PDI: `across goals and evidence, what should the learner work on now?`

The PDI may temporarily reorder curriculum activity when a higher-leverage gap exists, but it must not silently rewrite an approved Planner.