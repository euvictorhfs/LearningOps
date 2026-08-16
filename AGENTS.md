# LearningOps Core Agent Contract

LearningOps is the control plane for the human–AI learning system.

## Authority

Only the LearningOps control-plane project may approve structural changes to this repository, global schemas, global assessment rules, evidence rules, PDI rules, knowledge-graph conventions, shared workspace structure, or the Learning Cockpit.

Study planes may read this repository and propose changes, but must not mutate global structures autonomously.

## Operating model

Structural changes follow:

Problem -> Evidence -> Proposal -> Impact -> Spec -> Implementation -> Validation -> PR -> Merge

## Separation

- `LearningOps-core`: system rules, methods, schemas, reusable engine and cockpit implementation.
- `LearningOps-workspace`: observed learner state, sessions, evidence, metrics, PDI, gaps, misconceptions, history and knowledge graph.

Never store learner mastery or study evidence in Core.

## Zero Baseline

Every new learning domain starts at 0% observed mastery. Prior experience, credentials, self-assessment or conversational memory never initialize mastery. Prior knowledge may accelerate progression only after being demonstrated.

## Evidence Lineage

No metric without evidence. No evidence without identifiable origin and time. No mastery change without lineage.

## Versioning

Core is explicitly versioned. Relevant changes must record previous version, new version, reason, impact, migration requirement and compatibility.

## Source of truth

GitHub is the versioned source of truth. Conversation memory is convenience context, never durable evidence.
