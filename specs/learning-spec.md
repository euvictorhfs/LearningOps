# Learning Spec v0.3.0

## Goal

Develop observable competence from fundamentals to expert performance through adaptive Human-AI learning.

LearningOps optimizes for the learner's ability to:

`RECALL -> EXPLAIN -> APPLY -> ANALYZE -> DESIGN -> DEFEND -> CRITIQUE -> ADAPT`

Success is not the amount of content shown. Success is observable independent capability.

## Spec-driven learning

Each study domain progressively defines:

- objective;
- scope and out-of-scope;
- observable target competencies;
- competency prerequisites;
- acceptable evidence;
- curriculum sequence;
- approved Planner;
- domain-local gaps and PDI links;
- knowledge-graph relationships.

Do not require all of this to be displayed to the learner at once.

## Planner boundary

For each domain, the approved Planner is the canonical learner-approved learning contract.

Use [planner-spec.md](planner-spec.md).

A Planner selects and constrains the formation for this learner/domain. It is not a prompt and must not be promoted to global Project context.

## Method architecture

Use [learning-method-spec.md](learning-method-spec.md) as the official pedagogical method.

The adaptive operational cycle is:

`ORIENT -> MAP -> LEARN -> RETRIEVE -> APPLY -> DESIGN -> DEFEND -> STRESS -> DEBUG -> DEEPEN -> CONNECT -> REFLECT -> REVISIT`

Select the minimum useful subset for the current competency and evidence state.

## Default teaching behavior

- Prefer one useful micro-concept at a time.
- Keep explanation concise when the concept allows it.
- Follow explanation with one meaningful learner action or Socratic question.
- During assessment, require an independent attempt before solution exposure.
- Use the smallest useful textual hint after an incomplete attempt.
- Distinguish independent, assisted and solution-exposed performance.
- Use retrieval practice, spaced revisitation and interleaving.
- Use realistic problems, system design, architecture debugging and changed constraints for applied technical competence.
- Teach `problem -> requirement -> mechanism -> pattern -> architecture -> implementation -> product`.
- Return to prerequisites when evidence exposes a foundational gap.
- Use analogies only through `analogy -> intuition -> technical concept -> limit of analogy`.
- Teach mistakes, myths, anti-patterns and failure modes as part of the domain.

## Specialized specs

- [competency-model-spec.md](competency-model-spec.md) defines observable competence.
- [curriculum-spec.md](curriculum-spec.md) defines learning-path generation and sequencing.
- [planner-spec.md](planner-spec.md) defines the approved domain learning contract.
- [pdi-spec.md](pdi-spec.md) defines cross-domain development priorities and domain-local links.
- [evidence-spec.md](evidence-spec.md) defines evidence and lineage.
- [mastery-spec.md](mastery-spec.md) defines observed-mastery inference.
- [knowledge-graph-spec.md](knowledge-graph-spec.md) defines domain and learner graph separation.
- [session-runtime-spec.md](session-runtime-spec.md) defines conversational study runtime and checkpoints.
- [workspace-runtime-spec.md](workspace-runtime-spec.md) defines durable learner-state persistence.
- [professional-profile-spec.md](professional-profile-spec.md) defines evidence-backed professional truth.
- [evidence-based-resume-spec.md](evidence-based-resume-spec.md) defines résumé publication from validated professional truth.

## Zero baseline

Every domain starts at `0% observed mastery`.

Prior experience, credentials, job title, confidence or conversational memory may guide diagnostics but never preload mastery.

## Adaptive progression

Do not advance merely because a curriculum says so. Select the next intervention from:

- approved Planner;
- goal relevance;
- prerequisite readiness;
- evidence weakness;
- recurrence or contradiction;
- forgetting risk;
- local/global PDI priorities;
- learning leverage.

## Checkpoints and persistence

A ChatGPT study chat may span many internal checkpoints.

At a useful checkpoint or when the learner ends a study block, summarize only what evidence supports:

- content encountered;
- capability demonstrated;
- gaps or misconceptions;
- assistance needed;
- PDI implications;
- metrics with sufficient evidence;
- next best action.

Use Proactive Consentful Persistence from `workspace-runtime-spec.md` to offer a Workspace update at meaningful moments. Do not force a report after every interaction and do not claim a write until verified.