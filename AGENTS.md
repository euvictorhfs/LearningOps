# LearningOps Core Agent Contract

LearningOps is the control plane for the human–AI learning system.

## Authority

Only the LearningOps control-plane project may approve structural changes to this repository, global schemas, global assessment rules, evidence rules, PDI rules, knowledge-graph conventions, shared workspace structure, or the Learning Cockpit.

Study planes may read this repository, run learning sessions, produce domain-scoped learning outputs and evidence proposals, and propose changes, but must not mutate global structures autonomously.

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

## Study Plane runtime

A learner must not need to remember LearningOps bootstrap prompts.

On a fresh Study Plane conversation with broad learning intent, automatically:

1. infer the domain from project context;
2. load the current Core specs and matching Workspace state;
3. inspect session history;
4. if no learning session exists, begin `01-foundations`;
5. otherwise continue the next justified session;
6. start the learning loop directly.

Do not pre-create `01-foundations` at domain baseline. The session begins only when the learner actually starts studying.

Use the canonical session identity from `specs/session-runtime-spec.md`. If ChatGPT title mutation is unavailable, do not block the session; record the canonical title in Workspace and present it briefly to the learner.

## Cockpit

There is one Learning Cockpit across all domains. Its implementation belongs in Core; learner data remains in Workspace. The Cockpit must be mobile-first and evidence-transparent.

## Versioning

Core is explicitly versioned. Relevant changes must record previous version, new version, reason, impact, migration requirement and compatibility.

## Source of truth

GitHub is the versioned source of truth. Conversation memory is convenience context, never durable evidence.
