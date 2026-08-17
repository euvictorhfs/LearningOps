# LearningOps

**English** | [Português](README.pt-BR.md)

**A Human–AI learning system for continuous, evidence-driven and versioned development.**

LearningOps turns a ChatGPT Project into a persistent learning environment.

Configure the system once. Then create a chat named after what you want to learn and start.

## Why LearningOps?

A generic chatbot works well for isolated questions. Studying for weeks, months or years requires continuity, method, planning, review, retention, observable competencies, a development plan, evidence, history, adaptation and lineage.

LearningOps adds that layer: ChatGPT runs the learning runtime while GitHub preserves the system and validated learner state.

## What LearningOps delivers

- **Learning Planner** — versioned contract for what was agreed for each study domain.
- **Adaptive curriculum** — organizes capabilities and sequence from goals, prerequisites and evidence.
- **Global evidence-driven PDI / Individual Development Plan** — prioritizes gaps across active fields.
- **Observed Mastery** — represents only capabilities actually demonstrated.
- **Competency Model** — separates breadth, depth, application, transfer, design, diagnosis, retention and communication.
- **Evidence Lineage** — meaningful progression can be traced to origin, time, assistance and system version.
- **Knowledge Graph** — connects concepts, mechanisms, prerequisites, alternatives, trade-offs and failure modes.
- **Knowledge Debt** — tracks important dependencies not yet demonstrated at the required depth.
- **Retention & Review** — revisits knowledge over time.
- **Learning Cockpit** — one view across domains, Planners, PDI, gaps, evidence and progression.
- **Professional Profile** — structured professional truth backed by evidence.
- **Evidence-Based Résumé** — produces job-ready résumés for humans, ATS and AI systems without inventing experience.

## LearningOps starts with a prompt, but it is not just a prompt

The official ChatGPT Project instruction acts as an **orchestrator**. It defines roles, invariants, routing, authoritative sources and which specialized specs to load.

Detailed intelligence remains versioned in GitHub specs and schemas.

This avoids a monolithic mega-prompt and keeps the system testable and portable.

## Single Responsibility Principle

Single Responsibility is a LearningOps pillar.

- **Generative AI Architecture** → architecture, context, prompts, tools and evals.
- **Learning Method** → how to teach.
- **Competency Model** → what observable competence means.
- **Curriculum** → what capabilities form a domain and how to sequence them.
- **Planner** → what formation was approved for one learner/domain.
- **PDI** → which development priorities have the highest value now.
- **Evidence** → what counts as evidence.
- **Mastery** → how evidence supports observed state.
- **Knowledge Graph** → how knowledge and relationships are modeled.
- **Session Runtime** → conversational behavior.
- **Workspace Runtime** → learner-state persistence.
- **Automation** → safe recurring maintenance.
- **Cockpit** → presentation of governed state.
- **Professional Profile** → structured professional truth.
- **Resume Generation** → publishing that truth for opportunities.

## The three chat types

### `LearningOps OS`

Responsibility: **maintain the system**.

Use it for setup, GitHub validation, Core, Workspace, architecture, specs, schemas, evals, migrations, versioning, Cockpit, automations, branches, commits, PRs and authorized merges.

The assistant acts as a **Generative AI Engineering Architect**.

**`LearningOps OS` is never a study session.**

After the user's first message, it should explain its role and surface examples such as:

- `Validate my installation.`
- `Check Core and Workspace.`
- `Review the architecture.`
- `Configure the Cockpit.`
- `Configure automations.`
- `Prepare a change for review.`

### `My Learning`

Responsibility: **cross-domain learner view**.

Use it for:

- global PDI;
- highest-priority gaps;
- progress comparison across domains;
- demonstrated competencies;
- retention and knowledge debt;
- professional profile;
- résumé generation;
- cross-domain Cockpit interpretation.

After the user's first message, it should explain its role and surface examples such as:

- `How is my PDI?`
- `What are my biggest gaps?`
- `What should I prioritize now?`
- `Compare my progress across domains.`
- `Update my professional profile.`
- `Generate my résumé for this job.`

### Study chats

Use only the natural field name:

`Modern Data Architecture`

`Prompt Engineering`

`Distributed Systems`

The study field name may use the learner's language.

The assistant acts as an **Adaptive Technical Tutor**.

After the user's first message — regardless of its wording — the chat should briefly explain its role and make useful actions discoverable. If the message already contains a clear topic or request, keep the introduction short and continue immediately.

Useful actions include:

- define/refine the Planner;
- learn a topic;
- practice problems and system design;
- review/retrieve knowledge;
- close the Planner;
- persist evidence when the system offers it.

## Bilingual runtime

Canonical chat names remain `LearningOps OS` and `My Learning`.

The runtime detects the user's language and responds in it. System messages should provide semantically equivalent PT-BR and EN behavior.

## Learning method

LearningOps combines complementary methods:

- Socratic Learning;
- Microlearning;
- Retrieval Practice;
- Spaced Revisit;
- Interleaving;
- Problem-Based Learning;
- Pareto Two-Pass;
- Analogy Bridging;
- Error Reverse Engineering;
- Deliberate Practice;
- System Design Practice;
- Adversarial Learning;
- Transfer Practice;
- Metacognitive Regulation.

Adaptive cycle:

`ORIENT → MAP → LEARN → RETRIEVE → APPLY → DESIGN → DEFEND → STRESS → DEBUG → DEEPEN → CONNECT → REFLECT → REVISIT`

This is not a checklist. The runtime selects the smallest useful subset.

## Zero Baseline

Every new learning field starts at:

`0% observed mastery`

Prior experience, title, certifications, confidence or chat memory do not initialize mastery. Prior knowledge may accelerate the path after it is demonstrated.

## Evidence before progress

Exposure is not mastery.

LearningOps looks for observable behaviors such as explaining, distinguishing, applying, diagnosing, comparing, defending, designing, transferring and retrieving knowledge after time has passed.

In assessment mode preserve:

`independent attempt → smallest useful hint → retry → full explanation when needed`

Assistance level is part of the evidence.

# Getting Started

## Step 1 — Create the Project

In ChatGPT, create a Project named:

`LearningOps`

Set memory to **project-only memory**.

## Step 2 — Connect GitHub

Authorize access to:

- Public Core: https://github.com/euvictorhfs/LearningOps
- Private Workspace: https://github.com/euvictorhfs/LearningOps-workspace

Core contains the system. Workspace contains observed learner state.

## Step 3 — Install the Project Instructions

Open:

https://github.com/euvictorhfs/LearningOps/blob/main/runtime/CHATGPT_PROJECT_INSTRUCTIONS.md

Copy the full contents into the ChatGPT **Project Instructions**.

## Step 4 — Create `LearningOps OS`

Create the first chat named:

`LearningOps OS`

Send:

> Initialize LearningOps and validate my installation. Confirm which canonical repositories and `main` branches you can actually access. Do not make changes.

The system must test real access and never assume a capability merely because it received a URL.

## Step 5 — Initialize the Workspace

Still in `LearningOps OS`, send:

> Validate and initialize my LearningOps Workspace using the current specs. Do not invent any data about me.

The system should verify structure, schemas, domains, history, lineage, compatibility and permissions.

## Workspace — durable learner memory

The private Workspace preserves, as applicable:

- Planners;
- domains;
- checkpoints;
- evidence;
- mastery;
- PDI;
- gaps and misconceptions;
- knowledge debt;
- retention;
- learner graph;
- professional profile;
- Cockpit config/snapshots;
- history and lineage.

### Fundamental guardrail

**Planner, PDI, mastery, evidence, curriculum state and knowledge graph must never depend exclusively on chat memory.**

`Chat → runtime`

`Workspace → persisted learner state`

`GitHub → source of truth`

## Step 6 — Create the Learning Cockpit with ChatGPT Sites

Use ChatGPT Sites when it is available for your account.

Open the ChatGPT Sites/Work experience or invoke `@Sites` in a compatible environment.

Example request:

> Create my Learning Cockpit using the current LearningOps specs and Workspace contract. The Cockpit must only present governed state and must never fabricate evidence or metrics.

Review the preview, review privacy/sharing settings, and publish when ready.

A deployment produces a production URL.

### Register the URL

Return to `LearningOps OS` and send:

> This is the official URL of my Learning Cockpit: `<URL>`. Register it in the Workspace as my active Cockpit.

The system must persist and verify that configuration in the Workspace.

**Do not add the Cockpit URL as a global Project source.** The URL is configuration; Workspace remains the source of truth.

### Does the Cockpit update automatically?

Do not assume it does.

The adapter must declare a mode:

- **live-data** — reads current governed state through a validated integration;
- **snapshot** — presents a snapshot that must be rebuilt/refreshed when Workspace changes.

A published URL does not prove automatic GitHub synchronization.

## Step 7 — Configure automations

LearningOps recommends two initial recurring jobs.

### `LearningOps Workspace Maintenance`

Default cadence: **daily**.

Use it to reconcile state derived from already-persisted evidence, review PDI, retention, knowledge debt, learner graph and Cockpit snapshot when applicable.

Suggested prompt:

> Read the current LearningOps Workspace. Reconcile only state derived from already-persisted evidence according to the current specs. Check PDI, mastery, retention, knowledge debt, learner graph and Cockpit snapshot when applicable. Never create evidence or mastery by inference. If you cannot actually write an allowed change, report it and do not claim the Workspace was updated.

### `LearningOps Health Review`

Default cadence: **weekly**.

Use it to validate schemas, lineage, Planner consistency, Core/Workspace compatibility, PDI, retention, broken references and Cockpit state.

Suggested prompt:

> Run a LearningOps Workspace health review. Check schema integrity, lineage, Planners, Core compatibility, PDI, retention, mastery and Cockpit. Do not fabricate evidence. Apply only changes permitted by the current specs and report anything requiring human decision.

### Automation rule

`READ → VALIDATE → DERIVE → RECONCILE → WRITE → VERIFY`

If write capability is unavailable:

`READ → VALIDATE → DERIVE → PROPOSE → REPORT`

**Automation may organize and derive state from evidence. Automation may never fabricate evidence.**

Task/app capabilities can change. Validate actual capabilities before relying on Project-file access or unattended GitHub writes.

## Step 8 — Create `My Learning`

Create a chat named:

`My Learning`

Use it as the cross-domain conversational surface.

Do not create separate chats for PDI, mastery, gaps, professional profile or résumé.

## Step 9 — Create your first study chat

Create a chat named after the field, for example:

`Modern Data Architecture`

Start naturally. No bootstrap command is required.

## Step 10 — Planner Discovery

LearningOps proposes an initial formation and you refine it in natural language:

- `Remove Kubernetes.`
- `Include Snowflake.`
- `Go deeper on Iceberg.`
- `I do not want Machine Learning now.`

Exploration does not need to be persisted.

## Step 11 — Close the Planner

When the plan is mature, the system should proactively offer:

> Your plan is consistent. Would you like to close your Planner and start studying?

You may also say:

> Close my Planner.

The system produces a candidate containing goals, scope, out of scope, competencies, prerequisites, curriculum, target depth, evidence expectations, checkpoints and relevant initial relationships.

## Step 12 — Approve and persist

After review:

> I approve the Planner.

The system should offer to persist it in the Workspace.

`Approved Planner → Workspace → GitHub`

Closing does not equal approval. Approval does not prove a write occurred. Persistence is complete only after verification.

### Planner is not a prompt

`Planner → source of truth`

`Prompt → runtime adapter`

Never add one domain Planner as a global Project source.

## During study

The learner should not need to remember when to update the Workspace.

LearningOps uses **Proactive Consentful Persistence**:

`DETECT → EXPLAIN → OFFER → USER DECIDES → EXECUTE → VERIFY`

Examples:

> I have 3 meaningful evidence records from this study block ready to register. Would you like to update your Workspace?

> Would you like to close this checkpoint and persist the observed progress?

If the learner says no, do not write.

One understandable authorization may cover downstream updates permitted by the owning specs, such as evidence, checkpoint, mastery derivation, PDI, knowledge debt, learner graph and Cockpit snapshot. Do not ask separately for every internal consequence.

## Study chat versus internal session

A study chat is the continuous context for one field.

`session` / `checkpoint` are internal lineage units persisted in Workspace. The learner does not need separate chats such as `01-foundations`, `02-storage`, etc.

## Global PDI

PDI may contain domain-linked items, but canonical prioritization is cross-domain and is accessed through `My Learning`.

Method:

`GOAL → TARGET COMPETENCIES → CURRENT EVIDENCE → GAP → PRIORITY → INTERVENTION → EVIDENCE → REVIEW → ADAPT`

Curriculum answers: `what capabilities form this domain and in what sequence?`

Planner answers: `what was agreed for this learner in this domain?`

PDI answers: `across all current goals and evidence, what has the highest development value now?`

## Professional Profile and Résumé

`My Learning` aggregates evidence-backed professional truth across domains.

Pipeline:

`Learning Evidence → Professional Profile → Job Matching → Résumé Generation → Validation → PDF/DOCX`

Study capability must not be represented as production experience without attributable evidence.

## Do not use generic Study Mode by default

LearningOps already supplies its own pedagogical runtime.

Do not enable generic `@study`, `/study` or Study Mode inside a LearningOps study chat by default. Two tutor runtimes may compete over questions, hints, sequence, Planner, curriculum and assistance.

Actual availability may differ across documentation, accounts and rollouts. LearningOps should evaluate observed behavior rather than depend on an availability assumption.

### Future compatibility eval

Before allowing Study Mode as an optional adapter, test:

- Project Instructions compliance;
- Planner compliance;
- attempt-before-answer;
- hint escalation;
- assistance lineage;
- curriculum/PDI compatibility;
- role isolation;
- coexistence without harmful double orchestration.

## GitHub is durable memory

### Core

`euvictorhfs/LearningOps`

System, methods, specs, schemas, runtime, evals, governance and adapters.

### Workspace

`euvictorhfs/LearningOps-workspace`

Private observed learner state.

## Architecture

Main specs:

- [Generative AI Architecture](specs/genai-architecture-spec.md)
- [Evaluation](specs/evaluation-spec.md)
- [Learning Method](specs/learning-method-spec.md)
- [Learning](specs/learning-spec.md)
- [Competency Model](specs/competency-model-spec.md)
- [Curriculum](specs/curriculum-spec.md)
- [Learning Planner](specs/planner-spec.md)
- [PDI](specs/pdi-spec.md)
- [Evidence & Lineage](specs/evidence-spec.md)
- [Mastery](specs/mastery-spec.md)
- [Knowledge Graph](specs/knowledge-graph-spec.md)
- [Session Runtime](specs/session-runtime-spec.md)
- [Workspace Runtime](specs/workspace-runtime-spec.md)
- [Automation](specs/automation-spec.md)
- [ChatGPT Sites Adapter](specs/chatgpt-sites-adapter-spec.md)
- [Learning Cockpit](specs/cockpit-spec.md)
- [Professional Profile](specs/professional-profile-spec.md)
- [Evidence-Based Resume](specs/evidence-based-resume-spec.md)
- [Governance](specs/governance-spec.md)

## Simple rule

To maintain the system: `LearningOps OS`.

For your global learner view: `My Learning`.

To study: create a chat named after the field.

When the plan is ready: `Close my Planner.`

When something meaningful can be persisted: **LearningOps offers; you decide.**

## Core principle

**Do not measure how much content was presented. Measure what the learner can actually do with the knowledge — backed by evidence, context and lineage.**
