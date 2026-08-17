# Professional Profile Spec v1.0

## Purpose

Maintain a canonical, structured and evidence-backed professional profile from which résumés, CVs, portfolio summaries, recruiter profiles and interview narratives can be generated.

The professional profile is not a résumé layout. It is the normalized source model for professional capability claims.

## Single Responsibility

- `professional-profile-spec.md` owns canonical professional facts and capability claims.
- `evidence-based-resume-spec.md` owns selection, tailoring and publication into résumé/CV outputs.
- `evidence-spec.md` owns underlying evidence and lineage.
- `mastery-spec.md` owns learning-state inference.

Changing document formatting must not change professional truth.

## Profile sections

The profile may contain:

- identity and contact fields approved for publication;
- professional headline candidates;
- summary claims;
- work history;
- education;
- certifications;
- projects;
- validated competencies;
- hard skills;
- tools and technologies;
- methods and architectural patterns;
- domain expertise;
- languages;
- publications or talks;
- portfolio/repository links;
- evidence-backed achievements;
- target-role preferences.

## Provenance

Every capability or achievement claim that goes beyond basic biographical fact should be traceable to one or more of:

- LearningOps evidence ids;
- accepted external/work evidence;
- versioned project/artifact references;
- user-verified employment/education/certification records.

Keep source provenance internal. Public outputs expose only the claim unless the user chooses otherwise.

## Skill normalization

Store a canonical skill label plus optional aliases/synonyms so different recruiters, ATS parsers and language models can recognize equivalent terminology.

Examples:

- canonical: `Apache Spark`; aliases: `Spark`, `PySpark` when technically applicable;
- canonical: `Data Modeling`; aliases may include `Dimensional Modeling` only when evidence supports that narrower capability.

Do not create aliases that inflate scope.

## Capability categories

Separate:

- demonstrated hard skills;
- tools/technologies;
- domain knowledge;
- methods/practices;
- architecture/design capability;
- diagnostic/troubleshooting capability;
- communication/leadership evidence when legitimately supported;
- learning-only foundational capability;
- authentic work/project impact.

Learning evidence may support a capability claim but must never be rewritten as employment experience or production impact.

## Claim maturity

Internally classify publication readiness, for example:

- `not_publishable` — insufficient evidence;
- `foundational` — bounded learning capability;
- `demonstrated` — independent relevant evidence;
- `strong` — repeated application/transfer evidence;
- `work_validated` — authentic external/work evidence with adequate attribution.

These labels are internal controls, not résumé wording.

## Target-role mapping

A profile may map competencies and skills to one or more target role families. The mapping is a retrieval aid for résumé generation, not proof that the learner qualifies for that role.

## Structured representation

Prefer a portable JSON representation compatible where practical with the open JSON Resume ecosystem while extending it with LearningOps provenance and capability metadata.

The public/exported JSON view must omit private evidence identifiers unless explicitly requested.

## Privacy

Professional publication is opt-in.

- Private/confidential evidence stays private.
- Client/company-sensitive details require redaction or generalized wording.
- The profile must support separate private canonical data and public-safe publication views.

## Update behavior

The profile evolves automatically from governed evidence and user-verified facts, but new or materially stronger external-facing claims require review rules from the résumé spec before publication.