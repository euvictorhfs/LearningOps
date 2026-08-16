# LearningOps Cockpit

The Cockpit is a framework-light, mobile-first single-page application for navigating LearningOps state.

## Run

Serve this directory with any static HTTP server. The application attempts to load `snapshot.json` from the same directory and falls back to a zero-baseline demo state when no snapshot is present.

For governed usage, generate or copy a snapshot from `LearningOps-workspace/cockpit/snapshot.json` at build/deploy time. Do not move learner state into Core.

## MVP v0.3

- overview across domains
- domain drill-down
- PDI
- competency/session/evidence/gap surfaces
- knowledge graph surface
- history
- evidence-lineage view
- touch/desktop draggable whiteboard with browser-local draft persistence

Whiteboard local state is a draft surface and is not evidence until explicitly promoted through a governed Workspace workflow.
