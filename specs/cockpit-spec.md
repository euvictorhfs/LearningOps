# Learning Cockpit Spec v0.1.0

## Purpose

Provide one cross-domain visual interface over versioned LearningOps state. The Cockpit is not the source of truth; GitHub is.

## Required views

- Overall learner view across domains.
- Domain dashboard.
- Generalist breadth vs specialist depth.
- Observed mastery with evidence drill-down.
- First-try vs assisted accuracy.
- Retention and transfer indicators when evidence exists.
- PDI and priority gaps.
- Knowledge graph and competency dependencies.
- Session history and evidence lineage.
- Knowledge debt and misconceptions.

## Visual learning

The Cockpit should support architecture diagrams and collaborative visual reasoning without requiring a design tool. Preferred representations are lightweight web-native diagrams, editable nodes/edges, SVG or Mermaid where appropriate.

## Portability

Knowledge content should remain portable through Markdown, YAML frontmatter and JSON/JSONL. Obsidian may consume these files but must not be a runtime dependency.

## Metric guardrail

Never display a mastery percentage without a route to its evidence and lineage. If evidence is insufficient, display that explicitly rather than inventing a score.
