# Learning Cockpit Spec v0.3.0

## Purpose

Provide one cross-domain visual interface over versioned LearningOps state. The Cockpit is not the source of truth; GitHub is.

## Architecture boundary

- Cockpit implementation belongs in `LearningOps-core/cockpit/`.
- Learner state and generated cockpit snapshots belong in `LearningOps-workspace`.
- Core must never embed learner mastery/evidence as application source data.
- A build or artifact-generation step may combine Core UI with a Workspace snapshot for rendering.

## MVP experience

The Cockpit is mobile-first, framework-light and usable from phone, notebook or web. Design is subordinate to learning utility.

The v0.3 MVP must provide real navigation and interaction, not only a static preview.

## Required MVP views

- Overall learner overview across domains.
- Domain list and per-domain dashboard.
- Per-domain tabs for PDI, competencies, sessions, evidence and gaps.
- Generalist breadth vs specialist depth.
- Observed mastery with zero-state behavior.
- Cross-domain PDI.
- Knowledge graph surface.
- Session/history timeline.
- Evidence-lineage governance view.
- Learning Whiteboard with draggable components usable on touch and desktop.

## Zero-state behavior

A newly initialized domain must visibly show 0% observed mastery and must not fabricate KPIs. Missing evidence-dependent metrics should display as unavailable or insufficient evidence.

A domain baseline does not imply an active learning session.

## Whiteboard

The MVP whiteboard may persist draft nodes locally in the browser. Local whiteboard state is not learner evidence and must not affect mastery.

A later governed capability may promote selected diagrams or notes to versioned Workspace artifacts.

## Knowledge graph

At zero baseline, render only registered domains and system relationships. Concepts and edges must be added from versioned knowledge or evidence; never fabricate a graph to make the interface appear populated.

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
- current session.

Future snapshot fields must be backward compatible or accompanied by an explicit migration.

## Portability

Knowledge content remains portable through Markdown, YAML frontmatter and JSON/JSONL. Obsidian may consume these files but is not a runtime dependency.

## Metric guardrail

Never display an evidence-derived mastery value without lineage in the persisted model. If evidence is insufficient, display that explicitly rather than inventing a score.

## MVP acceptance criteria

The v0.3 MVP is acceptable when a user can, on phone or desktop:

1. navigate between overview and system views;
2. open each domain and inspect its learning surfaces;
3. confirm zero baseline without fabricated knowledge;
4. inspect PDI, history and lineage placeholders driven by real state;
5. create and drag whiteboard components locally;
6. return to other views without page reload.
