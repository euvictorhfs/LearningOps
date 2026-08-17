# Workspace Runtime Spec v1.0

## Purpose

Define how LearningOps reads, proposes, persists, reconciles and verifies learner-state changes in the private `LearningOps-workspace` repository.

The Workspace is the durable record of observed learner state. Chat memory is not.

## Boundary

Core defines system behavior.

Workspace stores human state, including:

- domains;
- approved Planners;
- checkpoints;
- evidence;
- observed mastery state;
- PDI items;
- gaps and misconceptions;
- retention state;
- knowledge debt;
- learner graph state;
- professional profile;
- Cockpit configuration/snapshots;
- lineage and history.

Never copy system policy into learner-state records as if it were evidence.

## Runtime principle

For learner-state-dependent decisions, use:

`CURRENT CORE CONTRACTS + CURRENT PERSISTED WORKSPACE STATE`

when both are accessible.

Do not prefer remembered chat state over a newer persisted Workspace record.

## Proactive Consentful Persistence

The default interaction model is:

`DETECT -> EXPLAIN -> OFFER -> USER DECIDES -> EXECUTE -> VERIFY`

The learner should not need to remember internal persistence commands.

Examples of natural persistence triggers:

- Planner candidate becomes ready for approval;
- approved Planner is ready to persist;
- one or more meaningful evidence records are ready;
- a natural session checkpoint is reached;
- the learner is ending a study block;
- a correction/supersession should be recorded;
- professional-profile evidence is ready to aggregate.

## Consent granularity

Do not ask for a separate confirmation for every deterministic downstream state update.

If the learner approves `update my Workspace with the evidence from this session`, the same governed operation may:

- persist accepted evidence;
- persist the checkpoint;
- recompute allowed derived mastery state;
- update relevant PDI items;
- update knowledge debt;
- update learner-graph state;
- update a Cockpit snapshot;

provided every derived write follows its owning spec and is fully traceable to the approved evidence/update scope.

## Evidence batching

Avoid interrupting study for trivial micro-updates.

When several evidence candidates arise in a short block, aggregate them into a meaningful checkpoint and offer one understandable update.

Example:

`I have 3 evidence records from this study block ready to register. Would you like to update your Workspace?`

## Write capability honesty

Before a durable mutation, verify that the active tool/integration can actually write to the required repository/branch.

If write capability is unavailable:

- do not claim the Workspace was updated;
- describe the intended delta;
- keep it clearly pending/unpersisted;
- route implementation to `LearningOps OS` or another authorized write capability when appropriate.

Local computer storage is not a required intermediary. GitHub is the canonical durable store.

## Corrections

Prefer append/supersede semantics over silent historical rewrites.

A correction should preserve:

- prior record identity;
- replacement/superseding record;
- reason;
- actor/authorization;
- timestamp;
- Core version.

Respect deletion/consent requirements defined by Evidence and governance specs.

## Cross-domain state

Some learner state is domain-scoped; some is global.

Domain-scoped examples:

- domain Planner;
- domain curriculum progress;
- domain evidence;
- domain mastery dimensions;
- domain misconceptions;
- domain knowledge graph state.

Cross-domain examples:

- global PDI prioritization;
- professional profile;
- résumé publication inputs;
- global knowledge-debt prioritization;
- cross-domain competency summaries;
- global Cockpit overview.

The `My Learning` chat is the preferred conversational interface for cross-domain learner state.

## Suggested Workspace organization

The exact migration is versioned separately, but the logical layout should support:

```text
workspace/
  domains/<domain-id>/
    planner/
    state/
    sessions/
    evidence/
    knowledge/
  learner/
    pdi/
    professional-profile/
    cross-domain/
  cockpit/
    config/
    snapshots/
  evidence-inbox/
```

Existing compatible paths may be retained during migration. Structure must not be changed silently.

## Guardrails

- no metric without evidence;
- no evidence without origin/time;
- no mastery transition without lineage;
- no fabricated state to make the Cockpit look complete;
- no learner-state write merely because a chat remembered something;
- automation may reconcile/derive permitted state but cannot manufacture evidence;
- every durable mutation must be verifiable in GitHub history.