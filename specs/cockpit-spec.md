# Learning Cockpit Spec v0.2.0

## Purpose

Provide one cross-domain visual interface over versioned LearningOps state. The Cockpit is not the source of truth; GitHub is.

## Architecture boundary

- Cockpit implementation belongs in `LearningOps-core/cockpit/`.
- Learner state and generated cockpit snapshots belong in `LearningOps-workspace`.
- Core must never embed learner mastery/evidence as application source data.
- A build or artifact-generation step may combine Core UI with a Workspace snapshot for rendering.

## Experience

The Cockpit is mobile-first, framework-light and usable from phone, notebook or web. Design is subordinate to learning utility.

## Required views

- Overall learner view across domains.
- Domain dashboard.
- Generalist breadth vs specialist depth.
- Observed mastery with evidence drill-down.
- First-try vs assisted accuracy when evidence exists.
- Retention and transfer indicators when evidence exists.
- PDI and priority gaps.
- Knowledge graph and competency dependencies.
- Session history and evidence lineage.
- Knowledge debt and misconceptions.

The v0.2 implementation may expose a smaller baseline surface while preserving the data contracts required to grow into these views.

## Zero-state behavior

A newly initialized domain must visibly show 0% observed mastery and must not fabricate KPIs. Missing evidence-dependent metrics should display as unavailable or insufficient evidence.

A domain baseline does not imply an active learning session.

## Visual learning

The Cockpit should support architecture diagrams and collaborative visual reasoning without requiring a design tool. Preferred representations are lightweight web-native diagrams, editable nodes/edges, SVG or Mermaid where appropriate.

## Portability

Knowledge content should remain portable through Markdown, YAML frontmatter and JSON/JSONL. Obsidian may consume these files but must not be a runtime dependency.

## Metric guardrail

Never display a mastery percentage without a route to its evidence and lineage. If evidence is insufficient, display that explicitly rather than inventing a score.
