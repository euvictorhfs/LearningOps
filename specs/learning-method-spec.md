# Learning Method Spec v1.0

## Purpose

Define the official pedagogical methods used by LearningOps. The runtime adapts these methods to evidence; it does not execute every method on every concept.

## Pedagogical methods

- **Socratic Learning** — expose reasoning through one relevant question at a time; prefer why, constraints, assumptions and trade-offs over recall-only questioning.
- **Microlearning** — introduce the smallest useful concept, normally with a concise explanation, then require learner activity before continuing.
- **Retrieval Practice** — ask the learner to recover prior knowledge without exposing the answer first.
- **Spaced Revisit** — re-test important knowledge after time has passed; a single correct answer is not durable mastery.
- **Interleaving** — mix related concepts after initial learning so the learner must discriminate which principle applies.
- **Problem-Based Learning** — teach through realistic problems with context, requirements and constraints instead of theory-only exposition.
- **Pareto Two-Pass** — first build the small set of high-leverage concepts that explains most of the domain; then return for internals, edge cases, performance, failure modes and trade-offs. Pareto prioritizes order, not final depth.
- **Analogy Bridging** — use `analogy -> intuition -> technical concept -> limit of analogy`; never let an analogy replace the technical definition.
- **Error Reverse Engineering** — teach common mistakes, myths, anti-patterns and apparently reasonable decisions that fail under real constraints.
- **Deliberate Practice** — target a specific demonstrated gap with a task just beyond current independent performance and feedback proportional to the error.
- **System Design Practice** — require requirement discovery, decomposition, architecture, assumptions, trade-offs, failure analysis and adaptation under changed constraints.
- **Adversarial Learning** — challenge a proposed solution through devil's-advocate arguments, `break the system`, architecture debugging and counterexamples.
- **Transfer Practice** — require application of a principle in a materially different context from the teaching example.
- **Metacognitive Regulation** — explicitly support `plan -> monitor -> evaluate -> adapt`, and report learner-pattern observations only after recurring evidence.

## Operational learning cycle

LearningOps uses an adaptive cycle rather than a fixed lesson script:

`ORIENT -> MAP -> LEARN -> RETRIEVE -> APPLY -> DESIGN -> DEFEND -> STRESS -> DEBUG -> DEEPEN -> CONNECT -> REFLECT -> REVISIT`

### ORIENT

Establish the learning objective, constraints, current persisted state and relevant unknowns. Do not initialize mastery from self-report or experience.

### MAP

Build or update the competency and prerequisite map. Apply Pareto Two-Pass to choose the smallest high-leverage entry point without discarding long-term depth.

### LEARN

Teach one useful mechanism or concept at a time. Prefer mechanism before product and foundations before abstraction.

### RETRIEVE

Ask for unaided recall or reconstruction. Retrieval evidence is stronger when no answer-shaped cue is provided.

### APPLY

Use a realistic problem or comparison. The learner should choose the relevant concept rather than being told which pattern to use.

### DESIGN

When applicable, require the learner to build a solution, model, architecture, procedure or explanation from requirements.

### DEFEND

Require justification of decisions, assumptions, alternatives and trade-offs.

### STRESS

Change constraints, introduce counterarguments, scale, cost, failures or ambiguous requirements and ask whether the solution still holds.

### DEBUG

Present or inspect flawed reasoning and systems. Diagnose root causes rather than merely naming symptoms.

### DEEPEN

Descend abstraction layers into internals, mechanisms, performance, edge cases, failure modes and implementation implications.

### CONNECT

Link the concept to prerequisites, neighboring concepts, patterns and the domain knowledge graph.

### REFLECT

Update evidence-grounded metacognitive observations: what worked, what remained fragile, what assistance was needed and what should change next.

### REVISIT

Schedule future retrieval based on importance, fragility, contradictions and elapsed time. Revisit may happen in a later chat/session.

## Assessment guardrail

During an exercise or assessment:

1. learner attempts independently;
2. if incomplete or incorrect, provide the smallest useful textual hint;
3. learner attempts again;
4. only then provide the full explanation when needed;
5. distinguish first-try evidence from assisted evidence and solution-exposed practice.

Do not withhold a direct answer when the user explicitly asks for explanation rather than assessment.

## Technical depth

For technical domains, periodically descend multiple abstraction levels. Teach:

`problem -> requirement -> mechanism -> pattern -> architecture -> implementation -> product`

Avoid product-first teaching when the underlying mechanism is prerequisite knowledge.

## References

The design is informed by retrieval, spacing, interleaving and representation guidance from learning-science research; metacognitive planning-monitoring-evaluation; and evidence-centered learning design. LearningOps adapts these ideas into an evidence-transparent Human-AI runtime rather than claiming that one method is universally optimal.