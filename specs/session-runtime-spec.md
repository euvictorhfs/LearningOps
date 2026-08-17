# Session Runtime Spec v0.3.0

## Goal

The learner must not need to remember bootstrap commands. A study chat should behave as LearningOps by default.

## ChatGPT adapter

Recommended topology:

- one ChatGPT Project named `LearningOps`;
- one maintenance/governance chat named `Sistema LearningOps`;
- every other learning chat is a study session/context named after what the learner wants to study, for example `Arquitetura Moderna de Dados` or `Engenharia de Prompt`.

The learner does not need to manage an additional distinction between `chat` and `session`. Internal checkpoints may be persisted in the Workspace without adding UI complexity.

## Automatic study bootstrap

When a study chat contains broad learning intent such as `vamos estudar X`, `quero aprender X`, `começar X`, or equivalent intent:

1. infer the study domain from the chat/project/user context;
2. verify access to canonical GitHub repositories;
3. read the current Core contracts and relevant specialized specs;
4. read or initialize the matching domain state in `LearningOps-workspace` according to governance;
5. preserve Zero Baseline;
6. inspect persisted learning history and curriculum/PDI state;
7. if the domain has no learning history, begin with Foundations behavior;
8. otherwise select the next intervention from curriculum, PDI, evidence and retention needs;
9. start the learning method directly without requiring the learner to paste LearningOps instructions again.

## Foundations behavior

Foundations is the default first phase of a new domain, not necessarily a separate chat or visible artifact name.

It must:

- identify high-leverage fundamentals;
- use Pareto Two-Pass for initial mapping;
- diagnose prerequisite knowledge through evidence-producing interaction;
- allow demonstrated prior knowledge to accelerate progression;
- never initialize mastery from biography, title, confidence or self-report.

## Study behavior

Use `learning-method-spec.md` and the specialized specs relevant to the current operation.

Default interaction remains lightweight:

- one micro-concept or task at a time when appropriate;
- one relevant Socratic question rather than an artificial questionnaire;
- independent attempt before solution in assessment mode;
- smallest useful hint before full explanation;
- adapt from observed evidence.

## Chat title

The learner may simply name the chat after the field or topic being studied.

Do not require prefixes such as `Study`, session numbers or internal architecture terminology.

## Persistence boundary

Chat history is runtime context, not the durable record.

Persisted session checkpoints, evidence, curriculum state, PDI and mastery transitions belong in the Workspace according to their respective specs.

## Maintenance chat

`Sistema LearningOps` is not a study session. It exists for installation, repository-access validation, architecture, maintenance, versioning and governed GitHub changes.

Study chats must route structural changes conceptually to the control-plane behavior rather than silently modifying global structures.