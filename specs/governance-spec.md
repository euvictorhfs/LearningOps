# Governance Spec v0.1.0

## Planes

### Control Plane: LearningOps

The `LearningOps` ChatGPT project is the only plane authorized to approve structural changes to the LearningOps system.

It governs:

- Core architecture;
- global specs and schemas;
- evidence model;
- KPIs and PDI rules;
- knowledge-graph conventions;
- shared workspace structure;
- Learning Cockpit;
- migrations and compatibility.

### Study Planes

Study projects such as `LearningOps | Modern Data Architecture` and `LearningOps | Human–AI Cognitive Engineering` may:

- study;
- read Core;
- read/write their domain learning evidence when authorized by the operating environment;
- produce knowledge and session artifacts;
- identify gaps and misconceptions;
- propose structural improvements.

They must not autonomously approve or merge changes to global Core contracts, shared schemas, shared Cockpit structures or cross-domain governance.

## Change flow

Problem -> Evidence -> Proposal -> Impact -> Spec -> Implementation -> Validation -> PR -> Merge

## Approval model

- Study planes propose.
- LearningOps evaluates and approves conceptually.
- GitHub records what was actually implemented and merged.

## Repository boundary

- `LearningOps-core` contains the system.
- `LearningOps-workspace` contains observed human state.

Crossing this boundary requires an explicit architectural decision.
