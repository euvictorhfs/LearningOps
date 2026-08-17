# Knowledge Graph Spec v1.0

## Purpose

Define a portable, evidence-aware knowledge graph for concepts, dependencies and learner-relevant relationships without conflating domain knowledge with learner state.

## Two graph layers

LearningOps maintains a strict conceptual separation:

1. **Domain Knowledge Graph** — concepts and relationships that describe the subject.
2. **Learner Graph** — evidence-backed learner state attached to competencies/concepts.

Never encode learner mastery as if it were a property of the domain itself.

## Domain graph method

Use concept-mapping principles: concepts are nodes; labeled relationships form meaningful propositions.

Prefer explicit typed edges such as:

- `requires`;
- `part_of`;
- `implements`;
- `uses`;
- `contrasts_with`;
- `enables`;
- `constrains`;
- `fails_when`;
- `optimized_by`;
- `example_of`;
- `alternative_to`;
- `evolves_into`.

Avoid unlabeled edges that force the reader to guess the relationship.

## Node types

Typical domain nodes:

- area;
- domain;
- subdomain;
- concept;
- mechanism;
- pattern;
- architecture;
- technology/product;
- failure mode;
- trade-off;
- competency.

Nodes should have stable ids independent of display labels.

## Learner graph

Learner-specific state may reference domain nodes using:

- competency state;
- evidence ids;
- gap ids;
- misconception ids;
- PDI priorities;
- review-due status;
- confidence/contradiction metadata.

These records belong in the Workspace, not the Core domain model.

## Construction rules

Add a domain node or relationship when it is supported by:

- a governed curriculum/spec;
- versioned domain knowledge;
- a validated study artifact;
- an explicit migration or approved domain update.

Do not fabricate nodes or edges merely to populate the Cockpit.

## Learning use

Use the graph to:

- discover prerequisites;
- explain why a learning detour is needed;
- choose the next curriculum node;
- identify high-leverage concepts;
- connect isolated knowledge;
- generate interleaving sets;
- detect knowledge debt;
- visualize dependency risk.

## Concept mapping behavior

When teaching visually, prefer a focus question and a small subgraph over an unreadable global graph. Encourage the learner to explain or correct relationships; graph editing can itself generate evidence when the task is designed for assessment.

## Portability

Store canonical knowledge in portable text/structured formats such as Markdown + YAML and JSON/JSONL. Obsidian-compatible links are allowed but Obsidian is not required.

## Versioning

Graph changes that alter competency prerequisites, curriculum ordering or mastery denominators require explicit version lineage and impact review.