# Governance Spec v0.2.0

## Control Plane

LearningOps has one control plane responsible for system architecture and governance.

In the ChatGPT adapter, the recommended UX is one Project named `LearningOps` with a dedicated maintenance chat named `Sistema LearningOps`.

That chat is the operational surface for:

- installation and access validation;
- architecture and system maintenance;
- spec and schema changes;
- migrations and compatibility;
- branches, commits, pull requests and merges;
- Cockpit changes;
- cross-domain governance.

The chat title is a process convention, not an access-control boundary. GitHub permissions and review history remain authoritative.

## Study Plane

A Study Plane is a logical learning context, not necessarily a separate ChatGPT Project.

In the ChatGPT adapter, every other learning chat inside the `LearningOps` Project may act as a Study Plane for its named field, for example:

- `Arquitetura Moderna de Dados`;
- `Engenharia de Prompt`;
- `Sistemas Distribuídos`.

The learner should not need to understand the term `Study Plane` to use the system.

Study chats may:

- study;
- read Core;
- read the relevant Workspace domain;
- create domain-scoped learning/session records when authorized;
- produce knowledge and evidence;
- identify gaps and misconceptions;
- propose structural improvements.

They must not autonomously approve or merge changes to global Core contracts, schemas, Cockpit structures or cross-domain governance.

## Single Responsibility

Single Responsibility is a governance invariant.

- Core stores reusable system intelligence.
- Workspace stores observed learner state.
- each spec has one primary reason to change;
- each schema validates one record family or bounded aggregate;
- the ChatGPT project instruction orchestrates rather than duplicating all specs;
- the Cockpit renders state but does not manufacture learning evidence.

See [genai-architecture-spec.md](genai-architecture-spec.md).

## Change flow

`Problem -> Evidence -> Proposal -> Impact -> Spec -> Implementation -> Validation -> PR -> Merge`

Relevant changes must not be made silently.

## Approval model

- Study contexts may propose.
- the LearningOps Control Plane evaluates and approves conceptually;
- GitHub records what was actually implemented and merged.

## Repository boundary

- `euvictorhfs/LearningOps` contains the public Core: methods, rules, specs, schemas, runtime adapters and Cockpit implementation.
- `euvictorhfs/LearningOps-workspace` contains private learner state: domains, sessions, evidence, metrics, PDI, gaps, history and learner graph references.

Crossing this boundary requires an explicit architectural decision.

## Source of truth

GitHub `main` is the persisted source of truth. Conversation memory supports runtime continuity but never replaces persisted state or evidence.