# Curriculum Spec v1.0

## Purpose

Generate and evolve a learning curriculum from goals, competencies, prerequisites and evidence instead of using a static content list.

## Method

LearningOps uses an evidence-aware form of backward design:

1. define desired capabilities;
2. define acceptable evidence for those capabilities;
3. map prerequisite concepts and mechanisms;
4. build a learning sequence;
5. adapt the sequence from observed evidence.

The curriculum is therefore a plan for producing capability evidence, not a table of contents.

## Inputs

- learner objective;
- domain scope and explicit out-of-scope items;
- competency model;
- knowledge-graph prerequisites;
- current evidence and mastery state;
- PDI priorities;
- constraints such as time, target role, certification or interview preparation.

Self-reported prior experience may guide diagnostics but must not skip competencies without evidence.

## Curriculum layers

Each domain may organize content into:

- Foundations;
- Core;
- Intermediate;
- Advanced;
- Specialist.

These are sequencing labels, not mastery scores.

## Pareto Two-Pass curriculum

### Pass 1 — Explanatory map

Select the smallest set of high-leverage concepts needed to form a coherent mental model of the domain.

### Pass 2 — Specialist depth

Return to important areas for mechanisms, internals, edge cases, performance, failure modes, alternatives, cost and architectural implications.

No topic is excluded merely because it is outside the first 20%.

## Sequencing rules

Prefer:

- prerequisite before dependent abstraction;
- mechanism before product;
- simple model before exceptions;
- isolated concept before interleaving;
- guided application before adversarial stress;
- transfer and retention before declaring robust mastery.

Allow diagnostic detours when evidence shows that a prerequisite is missing or already strong.

## Curriculum node

A curriculum node should identify:

- id and title;
- target competencies;
- prerequisites;
- rationale;
- target depth;
- recommended learning methods;
- acceptable evidence;
- completion status derived from evidence, not attendance;
- next candidate nodes.

## Adaptive progression

The next learning step is selected from the intersection of:

`goal relevance x prerequisite readiness x evidence gap x forgetting risk x leverage`

Do not advance solely because a topic was presented.

## Completion

A curriculum can be covered without being mastered. Report separately:

- curriculum coverage;
- observed mastery;
- breadth;
- specialist depth;
- review debt.

A curriculum remains revisable as the goal, domain or evidence changes.