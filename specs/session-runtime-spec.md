# Session Runtime Spec v0.2.0

## Goal

A learner must not need to remember bootstrap commands. A Study Plane should behave as LearningOps by default.

## Automatic session bootstrap

When a new conversation in a Study Plane contains broad learning intent such as `vamos estudar X`, `quero aprender X`, `começar X`, or an equivalent request:

1. infer the Study Plane domain from project context;
2. read the current Core contract and relevant specs;
3. read the matching domain state in `LearningOps-workspace`;
4. preserve Zero Baseline;
5. inspect session history before choosing the next session;
6. if no learning session has started, initialize `01-foundations`;
7. otherwise continue or create the next justified learning session from evidence and curriculum state;
8. begin the learning loop without asking the learner to repeat LearningOps instructions.

## Foundations

`01-foundations` is the default first learning session for a broad new domain. It is not pre-created at domain initialization. It becomes real only when the first learning conversation begins, preserving temporal lineage.

Foundations must diagnose and teach prerequisite concepts from first principles while allowing prior knowledge to accelerate only after demonstration.

## Canonical session identity

Every session has a canonical identifier and display title.

Default first session:

- id: `01-foundations`
- display title: `01 — Foundations`

For later sessions, use concise domain-appropriate names such as `02 — Storage & File Formats`.

The runtime should use the canonical title in session records and may suggest it as the ChatGPT conversation title. If the product surface does not expose a title-write action, title renaming remains a UI concern and must not block the learning session.

## Conversation behavior

On a fresh study conversation, do not respond with setup instructions. Initialize silently, state the session name briefly, and start the first useful learning cycle.

## Persistence boundary

Chat history is runtime context, not the durable record. Session checkpoints, evidence and state transitions must be represented in the Workspace according to governance and evidence specs.

## Governance

Study Planes may create domain-scoped learning outputs and evidence proposals, but structural changes to Core, global schemas, shared Workspace structure or Cockpit require the LearningOps control plane.
