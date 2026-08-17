# Learning Cockpit Spec v0.3.1

## Purpose

Provide one cross-domain visual interface over versioned LearningOps state. The Cockpit is not the source of truth; GitHub is.

## Architecture boundary

- Cockpit implementation belongs in `euvictorhfs/LearningOps/cockpit/`.
- Learner state and generated cockpit snapshots belong in `euvictorhfs/LearningOps-workspace`.
- Core must never embed learner mastery/evidence as application source data.
- A build or artifact-generation step may combine Core UI with a Workspace snapshot for rendering.
- The Cockpit renders governed state; it does not compute or manufacture evidence/mastery rules that belong to their specialized specs.

## MVP experience

The Cockpit is mobile-first, framework-light and usable from phone, notebook or web. Design is subordinate to learning utility.

The MVP must provide real navigation and interaction, not only a static preview.

## Required views

- Overall learner overview across domains.
- Domain list and per-domain dashboard.
- Per-domain surfaces for PDI, competencies, study chats/checkpoints, evidence and gaps.
- Generalist breadth vs specialist depth.
- Observed mastery with zero-state behavior.
- Cross-domain PDI.
- Knowledge graph surface.
- History timeline.
- Evidence-lineage governance view.
- Learning Whiteboard usable on touch and desktop.

## Zero-state behavior

A newly initialized domain must visibly show 0% observed mastery and must not fabricate KPIs. Missing evidence-dependent metrics should display as unavailable or insufficient evidence.

A domain baseline does not imply an active study chat.

## Whiteboard

The MVP whiteboard may persist draft nodes locally in the browser. Local whiteboard state is not learner evidence and must not affect mastery.

A governed capability may promote selected diagrams or notes to versioned Workspace artifacts only through explicit evidence/knowledge rules.

## Knowledge graph

At zero baseline, render only registered domains and governed system relationships. Concepts and edges must come from versioned domain knowledge, curriculum or validated artifacts; never fabricate a graph to make the interface appear populated.

Use `knowledge-graph-spec.md` for graph semantics.

## Data contract

The UI consumes a Workspace snapshot. At minimum each domain exposes:

- domain id;
- title;
- status label;
- observed mastery;
- generalist breadth;
- specialist depth;
- evidence count;
- validated competencies;
- current study context/checkpoint when present.

Future snapshot fields must be backward compatible or accompanied by an explicit migration.

## Portability

Knowledge content remains portable through Markdown, YAML frontmatter and JSON/JSONL. Obsidian may consume these files but is not a runtime dependency.

## Metric guardrail

Never display an evidence-derived mastery value without lineage in the persisted model. Use `mastery-spec.md` for computation and `evidence-spec.md` for lineage. If evidence is insufficient, display that explicitly rather than inventing a score.

## Acceptance criteria

The Cockpit is acceptable when a user can, on phone or desktop:

1. navigate between overview and system views;
2. open each domain and inspect its learning surfaces;
3. confirm zero baseline without fabricated knowledge;
4. inspect PDI, history and lineage driven by governed state;
5. use the whiteboard without confusing local drafts with evidence;
6. return to other views without losing navigation state.