# Evidence-Based Resume Spec v1.0

## Purpose

Generate professional résumé/CV claims from validated LearningOps evidence without turning study attendance, self-description or inferred seniority into unsupported claims.

## Principle

A résumé claim is a publication view over validated evidence, not a new source of truth.

The Workspace remains authoritative for the underlying evidence and lineage.

## Eligible sources

A claim may be supported by:

- validated study evidence;
- accepted external/work evidence governed by the evidence contract;
- versioned projects or artifacts with attributable contribution;
- repeated capability evidence across relevant competencies.

Do not use as proof by themselves:

- self-assessment;
- job title;
- certification possession;
- course completion;
- conversational memory;
- exposure-only study records.

## Claim model

Each generated claim should identify internally:

- claim id;
- target role/context when supplied;
- capability statement;
- supporting competency ids;
- supporting evidence ids;
- strength/confidence;
- scope and limitations;
- last reviewed date.

## Claim strength

Prefer claims demonstrated through independent application, transfer, design, diagnosis, durable retrieval or authentic validated work.

When evidence only supports foundational knowledge, write a bounded foundational claim instead of inflating it into expertise.

## Generation workflow

`TARGET -> SELECT RELEVANT COMPETENCIES -> RETRIEVE VALIDATED EVIDENCE -> DRAFT CLAIM -> CHECK ATTRIBUTION -> CHECK SCOPE -> USER REVIEW`

The user approves the final wording before external use.

## Output styles

The same evidence may generate different views:

- concise résumé bullet;
- detailed CV capability;
- portfolio evidence note;
- interview story;
- technical profile summary.

Wording can change by audience; evidence lineage cannot.

## Guardrails

- Never infer seniority from mastery percentages.
- Never claim production impact without attributable evidence.
- Never expose private/confidential evidence in a public résumé.
- Preserve uncertainty where evidence is incomplete.
- If a desired claim is stronger than current evidence, create a PDI/assessment target instead of fabricating the claim.