# ThoughtOps Work Evidence Contract v1.0

## Purpose

Accept provenance-rich candidates from real work without merging the responsibilities of ThoughtOps and LearningOps.

## Boundary

ThoughtOps reports an observable behavior in a work artifact. LearningOps decides whether it is relevant, sufficiently attributable and strong enough to store or test. LearningOps alone maps validated evidence to competencies, trends, PDI or résumé claims.

## Required intake

```yaml
contract_version: 1.0
candidate_id: string
created_at: ISO-8601
consent: explicit
source:
  system: ThoughtOps
  artifact_type: email | jira | sprint_document | retrospective | decision | other
  artifact_ref: redacted-or-approved-reference
  date: YYYY-MM-DD
context:
  objective: string
  audience: string-or-unknown
  constraints: [string]
observation:
  behavior: string
  outcome: string
  assistance_level: none | clarification_only | guided | substantially_generated
  counterevidence: [string]
assessment:
  confidence: low | medium | high
  limits: [string]
privacy:
  classification: private | confidential | shareable
  redactions: [string]
```

Reject intake when consent is not explicit, provenance is unusable, confidential content is excessive or the record is only an identity inference.

## Intake decision

```yaml
candidate_id: string
decision: accepted | rejected | needs_demonstration | superseded
decided_at: ISO-8601
mapped_domain: string-or-null
mapped_competencies: [string]
rationale: string
metric_effects: []
review_after: date-or-null
```

`accepted` means admissible evidence, not automatic mastery. `needs_demonstration` should generate a bounded study task. `rejected` preserves rationale without penalizing mastery unless independent negative evidence exists.

## Feedback to ThoughtOps

Return only approved, actionable priorities: a practice target, relevant gap, constraint, short experiment or review date. Do not export the full learner profile by default.

## Reconciliation

Duplicate candidates share lineage. Contradictions remain explicit. Corrections supersede rather than rewrite silently. The learner can appeal a decision and supply counterevidence.
