# LearningOps

**English** | [Português](README.pt-BR.md)

**An AI learning system that turns isolated study conversations into continuous, observable and versioned development.**

## Why use LearningOps?

You can open ChatGPT and start asking questions about any topic. That works well for isolated answers, but studying for months requires something different: continuity, a learning method, criteria for deciding what was actually learned, gap review and a plan that evolves with you.

LearningOps adds that layer.

It turns ChatGPT from a generic chatbot into a **guided-learning runtime**: a ready-to-use Project prompt connects the model to versioned methods, specs and learner state in GitHub. You configure it once, then you can simply open a chat and study.

## What LearningOps delivers

- **Adaptive learning plan** — organizes the path from goals, prerequisites, competencies and evidence instead of following only a fixed content list.
- **Evidence-driven PDI / Individual Development Plan** — maintains a small set of high-leverage development priorities selected from the most relevant gaps.
- **Observed Mastery** — estimates only what you have demonstrated; exposure, title, certification and self-perception do not count as mastery.
- **Competency map** — separates generalist breadth, specialist depth, application, transfer, design, diagnosis, retention and other observable capabilities.
- **Evidence Lineage** — every meaningful progression can be traced to the activity, response, assistance level, timestamp and system version.
- **Knowledge Graph** — connects concepts, mechanisms, prerequisites, trade-offs, alternatives and failure modes without mixing domain knowledge with learner state.
- **Review and retention** — retrieves older knowledge, interleaves topics and revisits fragile concepts over time.
- **Learning Cockpit** — provides one view across domains, PDI, gaps, competencies, evidence and progression.
- **Evidence-based professional résumé** — can turn genuinely demonstrated capabilities into traceable professional claims without inventing seniority or experience.

## The learning method

LearningOps does not depend on one technique. It combines complementary methods and selects what is useful for the current learning state:

- **Socratic Learning** — uses one relevant question at a time to expose reasoning, assumptions and trade-offs before giving ready-made answers.
- **Microlearning** — introduces the smallest useful concept and asks the learner to act before moving on.
- **Retrieval Practice** — asks you to recover knowledge without exposing the answer first, strengthening independent recall.
- **Spaced Revisit** — returns to knowledge after time has passed; one correct answer is not treated as permanent mastery.
- **Interleaving** — mixes related concepts so you must identify which principle applies without being told what is being tested.
- **Problem-Based Learning** — teaches through realistic problems with context, requirements and constraints.
- **Pareto Two-Pass** — first builds a mental map from the concepts with the highest explanatory power, then returns for internals, edge cases, performance, failures and trade-offs.
- **Analogy Bridging** — uses `analogy → intuition → technical concept → limit of analogy` so simplification does not become misconception.
- **Error Reverse Engineering** — learns from common mistakes, myths, anti-patterns and decisions that look reasonable but fail under real constraints.
- **Deliberate Practice** — targets a specific gap with a task slightly above current independent performance and feedback proportional to the error.
- **System Design Practice** — requires requirement discovery, architecture, assumptions, trade-offs, failure analysis and adaptation.
- **Adversarial Learning** — challenges solutions through devil's-advocate arguments, changed constraints, flawed architectures and debugging.
- **Transfer Practice** — tests whether a principle can be applied in a materially different scenario from the teaching example.
- **Metacognitive Regulation** — uses `plan → monitor → evaluate → adapt` to improve the study strategy from recurring evidence.

### Operational cycle

The runtime selects only the useful stages:

`ORIENT → MAP → LEARN → RETRIEVE → APPLY → DESIGN → DEFEND → STRESS → DEBUG → DEEPEN → CONNECT → REFLECT → REVISIT`

This is not a mandatory checklist. It adapts to the target competency, current gap and available evidence.

## How the prompt works

LearningOps starts with a **ChatGPT Project prompt**.

That prompt does not contain the whole system. It acts as an orchestrator: it establishes critical rules, verifies GitHub access and loads only the specs required for the current task.

This follows the **Single Responsibility Principle**:

- the prompt orchestrates;
- each spec owns one responsibility;
- schemas validate records;
- Core contains reusable system intelligence;
- Workspace contains observed learner state;
- Cockpit only renders governed state.

Official prompt:

https://github.com/euvictorhfs/LearningOps/blob/main/runtime/CHATGPT_PROJECT_INSTRUCTIONS.md

## Install in ChatGPT

### Step 1 — Create the Project

In ChatGPT, create a Project named:

`LearningOps`

Set memory to **project-only memory**.

### Step 2 — Connect GitHub

Give ChatGPT access to both repositories:

- Public Core: https://github.com/euvictorhfs/LearningOps
- Private Workspace: https://github.com/euvictorhfs/LearningOps-workspace

Core stores the system. Workspace stores your learning state.

### Step 3 — Add the Project instructions

Open:

https://github.com/euvictorhfs/LearningOps/blob/main/runtime/CHATGPT_PROJECT_INSTRUCTIONS.md

Copy the full contents into the ChatGPT **Project Instructions**.

You do this once.

### Step 4 — Create the first chat

Create a chat named:

`Sistema LearningOps`

Use this chat for:

- installation and repository-access validation;
- system maintenance;
- architecture;
- spec and schema updates;
- versioning;
- branches, commits, pull requests and merges when you authorize them.

Send:

> Initialize LearningOps and validate my installation. Confirm which canonical repositories and `main` branches you can actually access. Do not make changes.

ChatGPT must verify real access. It must not assume access simply because it received a URL.

### Step 5 — Start studying

Create another chat in the same Project and name it only after the field you want to study.

Examples:

`Modern Data Architecture`

`Prompt Engineering`

`Distributed Systems`

You do not need prefixes, session numbers or bootstrap commands.

Start naturally:

> I want to learn Modern Data Architecture.

LearningOps should load existing state, start at **0% observed mastery** for a new domain, generate the initial path and conduct the study using the official method.

## Simple chat rule

- **`Sistema LearningOps`** = installation, governance and maintenance.
- **Any other chat** = study of the field indicated by the chat name/context.

Internally the system may persist checkpoints and evidence, but you do not need to manage that complexity in ChatGPT.

## During study

The default interaction is small and active:

1. one micro-concept or problem;
2. one relevant question;
3. your attempt;
4. a small hint if needed;
5. another attempt;
6. full explanation when necessary;
7. evidence and next steps updated only when justified.

When you explicitly ask for direct explanation rather than assessment, the system may answer directly.

## Zero Baseline

Every new learning field starts at:

`0% observed mastery`

Prior experience, title, certifications, confidence or conversation memory do not initialize mastery.

Prior knowledge can accelerate progression only after it is demonstrated.

## GitHub is durable memory

ChatGPT runs the learning experience. GitHub preserves the system and validated history.

- `euvictorhfs/LearningOps` — public, versioned Core.
- `euvictorhfs/LearningOps-workspace` — private, versioned learner state.

Project memory supports continuity, but it does not replace persisted evidence.

## Architecture

Detailed rules live in [`specs/`](specs/).

Main specs:

- [Generative AI Architecture](specs/genai-architecture-spec.md)
- [Learning Method](specs/learning-method-spec.md)
- [Learning](specs/learning-spec.md)
- [Competency Model](specs/competency-model-spec.md)
- [Curriculum](specs/curriculum-spec.md)
- [PDI](specs/pdi-spec.md)
- [Evidence & Lineage](specs/evidence-spec.md)
- [Mastery Computation](specs/mastery-spec.md)
- [Knowledge Graph](specs/knowledge-graph-spec.md)
- [Session Runtime](specs/session-runtime-spec.md)
- [Learning Cockpit](specs/cockpit-spec.md)
- [Evidence-Based Resume](specs/evidence-based-resume-spec.md)
- [Governance](specs/governance-spec.md)

## Core principle

**Do not measure how much content was presented. Measure what the learner can actually do with the knowledge, backed by evidence and lineage.**
