# ChatGPT Sites Cockpit Adapter Spec v1.0

## Purpose

Define ChatGPT Sites as the recommended ChatGPT-native presentation adapter for the Learning Cockpit without making LearningOps dependent on ChatGPT Sites.

## Architectural boundary

`Workspace -> governed Cockpit data -> adapter -> UI`

GitHub Workspace remains the source of truth.

The Site URL is configuration metadata, not learner evidence and not a Project-wide knowledge source.

## Onboarding flow

1. Open ChatGPT Sites / Work in a supported ChatGPT environment.
2. Create a Learning Cockpit from the current Cockpit spec and Workspace data contract.
3. Provide only the data/links/constraints required for the Cockpit.
4. Review the private preview.
5. Review privacy/sharing settings.
6. Publish/deploy when ready.
7. Copy the production Site URL.
8. In `LearningOps OS`, provide the URL and explicitly request registration as the active Cockpit.
9. Persist and verify the URL in Workspace Cockpit configuration.

Example:

`This is the official URL of my Learning Cockpit: <URL>. Register it in the Workspace as my active Cockpit.`

## Do not add the Site URL as a global Project source

The URL identifies the UI endpoint. It is not the canonical source of learner state.

Adding a domain- or UI-specific artifact as global Project context can create unnecessary context pollution.

## Data refresh modes

A deployment URL does not imply automatic synchronization with GitHub.

An adapter implementation must declare one of these modes:

### Live-data mode

The Site reads current governed Workspace data through a validated integration at runtime.

Requirements:

- authentication/privacy reviewed;
- source and refresh behavior documented;
- errors visible;
- no fabricated fallback data.

### Snapshot mode

The Site renders a governed Workspace snapshot.

Requirements:

- snapshot contains generation timestamp and Core/Workspace references;
- Workspace maintenance may rebuild the snapshot;
- deployment/update behavior is explicit;
- stale state is labeled rather than presented as current.

## Registration record

Cockpit configuration should support:

- adapter type (`chatgpt-sites`);
- active URL;
- visibility/access classification;
- data mode (`live` or `snapshot`);
- last verified timestamp;
- last data refresh timestamp when known;
- Core/Cockpit spec version;
- status/notes.

## Privacy

The learner must review Site access before publishing.

Do not publish private learner evidence, PDI, professional profile or other sensitive state publicly unless the learner explicitly chooses that visibility with informed intent.

## Portability

ChatGPT Sites is an adapter, not a Core dependency.

The same Cockpit data contract may be rendered by another web app, local app or future platform adapter.