# Automation Spec v1.0

## Purpose

Define safe recurring maintenance for LearningOps learner state without fabricating learning evidence.

Automation complements event-driven, consented persistence. It does not replace it.

## Two update paths

### Transactional study updates

Triggered by meaningful study events with user consent:

- approved Planner persistence;
- evidence checkpoint;
- session close;
- correction/supersession;
- professional-profile aggregation.

### Periodic maintenance

Recommended initial routines:

1. `LearningOps Workspace Maintenance` — daily.
2. `LearningOps Health Review` — weekly.

These are defaults, not immutable schedules. The learner may change cadence.

## Daily Workspace Maintenance

Purpose: reconcile already-persisted learner state.

May:

- find persisted checkpoints/evidence not yet reconciled;
- recompute permitted derived mastery state;
- refresh global/domain PDI priorities;
- identify overdue retention reviews;
- update knowledge-debt status;
- reconcile learner-graph derived state;
- rebuild Cockpit snapshots when the active adapter supports it;
- report inconsistencies or required human decisions.

Must not:

- create evidence from absence or inference;
- increase mastery because time passed;
- convert self-report into demonstrated competence;
- silently change an approved Planner;
- claim a write that cannot be verified.

## Weekly Health Review

Purpose: validate integrity and compatibility.

Check:

- schema validity;
- missing lineage;
- Planner/state inconsistencies;
- Core/Workspace compatibility or version drift;
- stale PDI items;
- retention backlog;
- broken/superseded references;
- Cockpit snapshot/config drift;
- records requiring human review.

## Execution model

`READ -> VALIDATE -> DERIVE -> RECONCILE -> WRITE -> VERIFY -> REPORT`

If write permission is unavailable:

`READ -> VALIDATE -> DERIVE -> PROPOSE -> REPORT`

Never substitute a claim of success for verification.

## ChatGPT Tasks adapter

When ChatGPT Tasks are used, onboarding should create the routines explicitly and explain their cadence and scope.

Tasks may evolve as the ChatGPT product changes. The runtime must verify current capabilities before relying on:

- Project-file access;
- connected-app access;
- GitHub read/write capability;
- unattended writes.

Do not treat uploaded Project files as the durable source for automation. GitHub Workspace is canonical.

## Suggested daily task prompt

`Read the current LearningOps Workspace. Reconcile only state derived from already-persisted evidence according to the current LearningOps specs. Check PDI, mastery, retention, knowledge debt, learner-graph state and Cockpit snapshot when applicable. Never create evidence or mastery by inference. If you cannot actually write an allowed change, report it and do not claim the Workspace was updated.`

## Suggested weekly task prompt

`Run a LearningOps Workspace health review. Check schema integrity, lineage, Planners, Core compatibility, PDI, retention, mastery references and Cockpit configuration/snapshots. Do not create or modify evidence except through an explicitly governed correction. Apply only changes permitted by current specs and report anything requiring human decision.`

## Notification policy

Do not notify on routine no-op runs unless the platform requires it.

Surface:

- failed writes;
- structural incompatibility;
- overdue high-priority retention;
- contradictory or broken evidence lineage;
- Planner incompatibility;
- human decisions required.

## Guardrail

**Automation may organize, validate and derive state from evidence. Automation may never fabricate evidence.**