# Evidence-Based Resume Spec v1.1

## Purpose

Generate professional résumé/CV outputs from the canonical Professional Profile and validated LearningOps evidence so the learner does not need to manually maintain résumé strategy, wording or formatting.

The goal is not to game recruiters, ATSs or language models. The goal is to produce documents that are truthful, machine-readable, recruiter-readable, role-relevant and evidence-grounded.

## Single Responsibility

- `professional-profile-spec.md` owns canonical professional facts and capability claims.
- this spec owns résumé selection, tailoring, publication strategy and render requirements.
- the Cockpit may expose/download generated outputs but does not own résumé truth or tailoring rules.

## Source model

Use `professional-profile-spec.md` as the canonical source.

A résumé claim may be supported by:

- validated study evidence;
- accepted external/work evidence governed by the evidence contract;
- versioned projects or artifacts with attributable contribution;
- repeated capability evidence across relevant competencies;
- user-verified biographical/employment/education/certification facts.

Do not use as proof by themselves:

- self-assessment;
- job title;
- certification possession;
- course completion;
- conversational memory;
- exposure-only study records.

## Publication pipeline

`TARGET ROLE/JOB -> PARSE REQUIREMENTS -> NORMALIZE SKILLS -> MATCH EVIDENCE -> SELECT CLAIMS -> DRAFT -> ATS/AI VALIDATE -> HUMAN READABILITY REVIEW -> RENDER -> USER APPROVAL`

### Target parsing

When a job description is supplied:

- extract responsibilities, required/preferred skills, technologies, domain terms and seniority expectations;
- distinguish hard requirements from generic employer language;
- identify recurring concepts rather than copying the job description verbatim;
- map requirements to canonical skills/competencies and aliases in the Professional Profile.

### Evidence matching

For each selected keyword or claim, require supporting profile data/evidence.

Never add a keyword merely because an ATS may search for it.

If a target requirement is valuable but unsupported, create a learning/PDI target instead of placing it in the résumé.

### Claim selection

Prioritize claims by:

`role relevance x evidence strength x attributable impact x recency x distinctiveness`

Avoid stuffing every known skill into every résumé.

## ATS and AI readability

Default résumé rendering should optimize for robust text extraction and semantic clarity across ATS parsers and language-model based recruiting tools.

Prefer:

- a single-column reading order;
- conventional section headings;
- standard fonts and bullets;
- explicit full skill/job terminology where ambiguity matters;
- contact information in normal document text;
- concise bullets with action + scope + evidence-backed outcome when outcome is known;
- normalized skill names plus natural aliases where genuinely supported;
- text-based documents rather than image-only résumés.

Avoid by default:

- multi-column layouts;
- tables used for core résumé content;
- charts or skill bars;
- icons carrying semantic meaning;
- text boxes;
- critical content in headers/footers;
- decorative graphics/photos unless the target market explicitly expects them;
- invisible keyword stuffing or repeated unnatural terms.

Current ATS documentation shows that complex formatting, tables, headers/footers, graphics and columns can still reduce parse reliability; formats accepted vary by system. Generate both PDF and DOCX when the runtime supports them, with the same canonical content.

## Machine-oriented semantics

Make the résumé easy for both parsers and LLMs to interpret by preserving explicit semantic structure:

- role/title;
- organization;
- dates;
- location when relevant;
- responsibility/achievement bullets;
- skills grouped by meaningful category;
- projects with contribution and technology context;
- education/certifications as separate sections.

Do not rely on visual proximity alone to communicate relationships.

## Structured canonical export

Maintain a structured résumé representation compatible where practical with the open JSON Resume schema. LearningOps-specific provenance fields should be stored as private extensions rather than forcing publication documents to expose evidence ids.

This structured representation enables multiple renderers without rewriting content from scratch.

## Base résumé and tailored views

Maintain:

- **Base résumé** — stable, high-quality representation for a target role family;
- **Tailored résumé** — a derived view for a specific job description using only supported claims;
- **Full CV/profile** — broader evidence-backed professional history when useful.

Tailoring changes selection, ordering and wording. It does not change underlying facts.

## Claim model

Each generated claim should identify internally:

- claim id;
- target role/context;
- capability statement;
- supporting competency ids;
- supporting evidence ids or verified-fact refs;
- strength/confidence;
- scope and limitations;
- keyword/requirement mappings;
- last reviewed date.

## Claim strength

Prefer claims demonstrated through independent application, transfer, design, diagnosis, durable retrieval or authentic validated work.

When evidence supports only learning capability, write a bounded skills/project claim instead of implying employment or production impact.

Never infer seniority directly from mastery percentages.

## Output formats

When supported, generate from the same structured source:

- ATS-safe PDF;
- ATS-safe DOCX;
- structured JSON;
- plain text/Markdown preview;
- optional HTML/web profile.

The PDF is the default human-shareable artifact. DOCX is an alternate submission format for systems where parsing reliability is preferable.

## Cockpit integration

The Learning Cockpit may expose a `Professional Profile / Resume` surface with:

- current base résumé status;
- target role family;
- evidence coverage for selected claims;
- unsupported target requirements;
- last generated date;
- PDF download;
- DOCX download when available;
- job-specific generation from a pasted job description;
- a privacy-safe preview before export.

Cockpit actions invoke the résumé pipeline; they do not mutate mastery.

## Automatic maintenance

The learner should not need to manually rewrite the résumé after each study session.

When new governed evidence materially changes a publishable capability, LearningOps may mark the Professional Profile and résumé as `refresh_recommended`.

Regeneration should update supported claims and skills while preserving user-verified employment facts and prior approved privacy choices.

Do not silently publish or submit a résumé to an employer.

## Validation

Before export, validate:

- every material claim has provenance;
- no confidential evidence leaks;
- job keywords are naturally supported by actual capabilities;
- no fabricated metrics, impact or seniority;
- section structure survives plain-text extraction;
- PDF/DOCX output has a logical reading order;
- wording is concise and human-readable;
- structured representation validates against its schema.

## User authority

The user approves external-facing versions before use. LearningOps can keep drafts current automatically, but external publication/application remains a user action.