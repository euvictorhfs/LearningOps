# Governance Spec v0.3.0

## Control Plane

LearningOps has one control plane responsible for system architecture and governance.

In the ChatGPT adapter, the canonical control-plane chat is:

`LearningOps OS`

It is the operational surface for:

- installation and access validation;
- architecture and system maintenance;
- spec/schema changes;
- migrations and compatibility;
- branches, commits, pull requests and merges;
- Cockpit/adapter changes;
- automation rules;
- cross-domain governance.

The chat title is a process convention, not an access-control boundary. GitHub permissions and review history remain authoritative.

## Learner Plane

Cross-domain learner management belongs to:

`My Learning`

This surface may:

- review global PDI;
- compare cross-domain gaps/priorities;
- review retention and knowledge debt;
- aggregate demonstrated competencies;
- maintain evidence-backed Professional Profile state;
- generate résumé outputs;
- interpret global Cockpit state.

It must not autonomously change global Core contracts or become the system control plane.

## Study Plane

A Study Plane is a logical learning context, not necessarily a separate ChatGPT Project.

In the ChatGPT adapter, a naturally named study chat acts as the Study Plane for one field, for example:

- `Modern Data Architecture`;
- `Prompt Engineering`;
- `Distributed Systems`;
- or an equivalent field name in the learner's language.

Study chats may:

- study;
- read relevant Core contracts;
- read the relevant Workspace domain;
- refine their domain Planner;
- create domain-scoped checkpoints/evidence when authorized;
- produce knowledge/evidence;
- identify gaps and misconceptions;
- propose structural improvements.

They must not autonomously approve or merge changes to global Core contracts, schemas, Cockpit structures or cross-domain governance.

## First-message UX

Every new chat should make its capabilities discoverable after the user's first message without requiring a trigger word.

- `LearningOps OS` introduces maintenance/control-plane actions.
- `My Learning` introduces cross-domain learner actions.
- study chats introduce Planner/study actions.

User-facing behavior follows the user's language; canonical control-chat names remain English.

## Single Responsibility

Single Responsibility is a governance invariant.

- Core stores reusable system intelligence.
- Workspace stores observed learner state.
- each spec has one primary reason to change;
- each schema validates one record family or bounded aggregate;
- the ChatGPT Project instruction orchestrates rather than duplicating all specs;
- the Cockpit renders state but does not manufacture learning evidence.

See [genai-architecture-spec.md](genai-architecture-spec.md).

## Durable learner-state boundary

Planner, PDI, mastery, evidence, curriculum progress, learner graph and professional-profile state must not depend exclusively on chat memory when persisted Workspace state exists.

Persistence follows Proactive Consentful Persistence:

`DETECT -> EXPLAIN -> OFFER -> USER DECIDES -> EXECUTE -> VERIFY`

Approval alone is not proof of a successful GitHub write.

## Automation governance

Automation may validate, organize, reconcile and derive state from already-persisted evidence.

Automation must not:

- fabricate evidence;
- convert elapsed time into mastery;
- convert self-report into demonstrated competence;
- silently rewrite an approved Planner;
- claim a failed/unavailable write succeeded.

## Change flow

`Problem -> Evidence -> Proposal -> Impact -> Spec -> Implementation -> Validation -> PR -> Merge`

Relevant changes must not be made silently.

## Approval model

- Study contexts may propose.
- `My Learning` may identify cross-domain needs or inconsistencies.
- `LearningOps OS` evaluates structural changes and governs implementation.
- GitHub records what was actually implemented and merged.

## Repository boundary

- `euvictorhfs/LearningOps` contains the public Core: methods, rules, specs, schemas, runtime adapters and Cockpit implementation.
- `euvictorhfs/LearningOps-workspace` contains private learner state: domains, Planners, checkpoints, evidence, mastery, PDI, gaps, history, learner graph, Cockpit config/snapshots and professional profile.

Crossing this boundary requires an explicit architectural decision.

## Source of truth

GitHub `main` is the persisted source of truth. Conversation/Project memory supports runtime continuity but never replaces persisted state or evidence.