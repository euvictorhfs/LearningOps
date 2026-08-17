# Mastery Computation Spec v1.0

## Purpose

Define how LearningOps converts evidence into transparent estimates of observed capability without pretending to measure an underlying trait with scientific precision.

## Principle

Mastery is an evidence-backed inference over a defined competency model.

It is not:

- self-confidence;
- exposure;
- course completion;
- a credential;
- one correct answer;
- a hidden psychological score.

## Computation model

For each competency, maintain evidence across relevant dimensions rather than averaging every event equally.

Evidence is interpreted using:

- independence / assistance level;
- task difficulty and ambiguity;
- context novelty;
- transfer distance;
- design or diagnostic complexity;
- consistency across attempts;
- recency and retention interval;
- contradictory evidence;
- evaluator confidence and provenance.

## Evidence tiers

Approximate strength classes:

- **E0 — exposure only**: content presented; no capability evidence.
- **E1 — assisted demonstration**: partially correct or correct with meaningful hints/scaffolding.
- **E2 — independent demonstration**: correct relevant behavior without answer-shaped assistance.
- **E3 — transfer demonstration**: independent success in a materially different scenario.
- **E4 — robust/adversarial demonstration**: repeated transfer, design, diagnosis or adaptation under changed constraints, plus retention where relevant.

Tiers describe evidence strength, not universal numeric weights.

## Competency state inference

Use the competency states from `competency-model-spec.md`.

Typical interpretation:

- `unobserved`: no admissible evidence;
- `exposed`: E0 only;
- `developing`: meaningful E1 or mixed E1/E2;
- `applied`: credible E2 in relevant application;
- `robust`: repeated E2/E3 across contexts with no unresolved material contradiction;
- `specialist`: E3/E4 across depth, design/diagnosis and changed constraints where applicable;
- `review_due`: prior strong evidence has aged beyond its retention expectation or new contradictory evidence appeared.

No state transition is automatic solely from event count.

## Domain metrics

### Observed Mastery

Estimate the share of target competencies whose required capability has been demonstrated for the current curriculum/goal, weighted by competency importance only when the model explicitly defines importance.

### Generalist Breadth

Estimate coverage of the domain's important competency families at an adequate navigation/application level.

### Specialist Depth

Estimate the share of specialist-target competencies supported by mechanism, edge-case, design, diagnosis, performance and adaptation evidence.

### Retrieval / First-Try / Assisted / Transfer / Design / Diagnostic / Retention

Compute only from events explicitly eligible for that metric. Always expose numerator, denominator and evidence refs when practical.

## Percentage guardrail

A percentage is a summary of evidence over a declared model, not an objective measure of the person.

Do not display a percentage when:

- the denominator/model is undefined;
- evidence volume is too small for a useful estimate;
- evidence is materially contradictory and unresolved;
- the metric cannot be traced to source events.

Use `evidence insufficient to estimate` instead.

## Contradiction and decay

Do not silently erase old evidence. New failures can lower confidence or move a competency to `review_due` while preserving prior success.

Retention is modeled by re-testing after meaningful intervals, not by arbitrary automatic score decay.

## Aggregation rules

- Never let many low-strength events overwhelm a smaller number of stronger contradictory events without review.
- Repeated near-identical tasks provide less incremental evidence than diverse tasks.
- Assisted success must remain distinguishable from first-try independent success.
- Solution-exposed events are learning events, not mastery evidence for the exposed target.
- External accepted evidence can support capability, but metric effects remain an explicit LearningOps decision.

## Lineage

Every metric update must record:

- prior state/value;
- new state/value;
- competency/model version;
- evidence ids considered;
- contradictory evidence considered;
- inference rationale;
- Core version;
- timestamp.