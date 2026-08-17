# LearningOps Core Agent Contract

LearningOps is the canonical system of record for deliberate learning and longitudinal professional development.

## Authority

Only the LearningOps control-plane project may approve structural changes to this repository, global schemas, assessment rules, evidence rules, PDI rules, knowledge-graph conventions, shared Workspace structure or the Learning Cockpit.

Study planes may read the Core, run sessions and propose domain-scoped records. ThoughtOps may submit work-evidence candidates. Neither may mutate global structures autonomously.

## Separation

- `LearningOps`: reusable learning rules, schemas, engine and cockpit.
- `LearningOps-workspace`: learner state, sessions, evidence, metrics, PDI, gaps, history and knowledge graph.
- `ThoughtOps`: daily professional artifacts and situational feedback.
- `ThoughtOps-workspace`: work context, preferences and approved operational records.

LearningOps exclusively owns study, curriculum, observed mastery, validated repertoire, longitudinal technical positioning and evidence-based résumé generation. It must not become an email, Jira or sprint-document production system.

## External work evidence

ThoughtOps candidates enter through `specs/thoughtops-evidence-contract.md`. A candidate is never proof by declaration. LearningOps records an intake decision: accepted, rejected, needs demonstration or superseded. Acceptance may contribute evidence without necessarily changing a metric.

## Zero baseline

Every new domain starts at 0% observed mastery. Prior experience, title, credentials, self-assessment, conversational memory and ThoughtOps observations do not initialize mastery. They may identify what to test.

## Evidence lineage

No metric without evidence. No evidence without origin and time. No mastery change without lineage. Preserve assistance level, counterevidence, confidence, privacy classification and correction history.

## Runtime

On a fresh Study Plane with broad learning intent, infer the domain, load current Core and Workspace state, inspect history, start foundations when no session exists, or continue the next justified session. The learner need not remember bootstrap prompts.

## Cockpit

There is one mobile-first, evidence-transparent Learning Cockpit across domains. Implementation belongs in Core; learner data remains in Workspace.

## Governance

Structural changes follow:

Problem -> Evidence -> Proposal -> Impact -> Spec -> Implementation -> Validation -> PR -> Merge
