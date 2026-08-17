# Learning Cockpit Spec v0.4.0

## Purpose

Provide one cross-domain visual interface over versioned LearningOps state. The Cockpit is not the source of truth; GitHub Workspace is.

## Architecture boundary

- Cockpit implementation belongs in `euvictorhfs/LearningOps/cockpit/` or a portable adapter implementation.
- Learner state, Cockpit configuration and generated snapshots belong in `euvictorhfs/LearningOps-workspace`.
- Core must never embed learner mastery/evidence as application source data.
- The Cockpit renders governed state; it does not compute or manufacture evidence/mastery rules owned by specialized specs.
- ChatGPT Sites may be used as the recommended ChatGPT-native adapter, but LearningOps Core must remain independent of it.

Use `chatgpt-sites-adapter-spec.md` for ChatGPT Sites behavior.

## Required experience

The Cockpit is mobile-first, clean and usable from phone, notebook or web. Design is subordinate to learning utility.

It must provide real navigation and interaction, not only a static preview.

## Required views

### Global / `My Learning` views

- learner overview across domains;
- global PDI priorities;
- cross-domain gaps and knowledge debt;
- retention/review state;
- demonstrated competencies across domains;
- Professional Profile;
- résumé / opportunity readiness entry point;
- global history and evidence-lineage governance.

### Domain views

- domain list and dashboard;
- active approved Planner and version/status;
- curriculum progress/context;
- domain-local PDI/gap context;
- competencies and observed mastery dimensions;
- study checkpoints;
- evidence;
- gaps/misconceptions;
- Knowledge Graph.

### Learning tools

- Learning Whiteboard usable on touch and desktop when implemented.

## Zero-state behavior

A newly initialized domain must visibly show `0% observed mastery` and must not fabricate KPIs.

Missing evidence-dependent metrics should display as unavailable / insufficient evidence.

A domain baseline does not imply an approved Planner or active study checkpoint.

## Whiteboard

The MVP whiteboard may persist draft nodes locally in the browser. Local whiteboard state is not learner evidence and must not affect mastery.

A governed capability may promote selected diagrams/notes to Workspace artifacts only through explicit evidence/knowledge rules.

## Knowledge graph

At zero baseline, render only registered domains and governed relationships. Concepts and edges must come from versioned domain knowledge, curriculum, Planner or validated artifacts; never fabricate a graph for visual completeness.

Use `knowledge-graph-spec.md`.

## Data modes

The active adapter must declare how data is refreshed:

### Live

The Cockpit reads current governed Workspace data through a validated integration.

### Snapshot

The Cockpit consumes a generated Workspace snapshot.

Snapshot mode must expose:

- generation timestamp;
- relevant Core/Workspace reference/version;
- data freshness/staleness;
- no fabricated fallback values.

Do not infer live synchronization from a published Site URL.

## Cockpit configuration

Workspace configuration should record, when approved:

- adapter type;
- active URL;
- status;
- visibility/access classification;
- data mode (`live`, `snapshot` or unverified);
- last verified time;
- last refresh time when known;
- Core/Cockpit spec version.

A Site URL is configuration metadata, not a Project source and not learner evidence.

## Minimum snapshot contract

At minimum, each domain may expose:

- domain id;
- title;
- status label;
- Planner status/version;
- observed mastery state/dimensions where evidence supports them;
- generalist breadth and specialist depth where evidence supports them;
- evidence count;
- validated competencies;
- current checkpoint when present;
- priority gaps/retention items when present.

Global snapshot data may expose:

- active global PDI items;
- cross-domain priorities;
- professional-profile summary;
- global retention/knowledge-debt counts or lists when evidence supports them;
- lineage/health indicators.

Future fields must be backward compatible or accompanied by an explicit migration.

## Privacy

The Cockpit may expose sensitive learner and professional-development state.

Before public or broader sharing, the learner must review visibility. Do not make private evidence, PDI, gaps or professional profile public merely because the adapter supports public publishing.

## Portability

Knowledge/state contracts remain portable through Markdown, YAML frontmatter and JSON/JSONL. Obsidian and ChatGPT Sites are optional interfaces, not runtime dependencies.

## Metric guardrail

Never display an evidence-derived mastery value without lineage in the persisted model. Use `mastery-spec.md` and `evidence-spec.md`. If evidence is insufficient, display that explicitly rather than inventing a score.

## Acceptance criteria

The Cockpit is acceptable when a user can:

1. navigate between global and domain views;
2. inspect Planner, competencies, evidence, gaps and checkpoints per domain;
3. inspect global PDI and cross-domain development state;
4. confirm Zero Baseline without fabricated knowledge;
5. inspect history and lineage driven by governed state;
6. identify whether the Cockpit is live, snapshot or unverified;
7. see stale snapshot state when applicable;
8. use optional learning tools without confusing drafts with evidence;
9. understand that Workspace/GitHub remains the source of truth.