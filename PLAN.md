# Resume Tool Implementation Plan

This document captures the implementation plan for a resume and cover letter tailoring tool, using this repository’s skill architecture as the basis.

## Goals

1. Tailor resumes and cover letters to specific job descriptions.
2. Maximize ATS compatibility and recruiter appeal.
3. Maintain persistent user state and version history.
4. Provide repeatable, command-driven workflows.

## Project Architecture Takeaways

1. Single skill entrypoint that defines behavior, routing, and priorities.
2. Command-specific workflows stored as reference docs and loaded on demand.
3. Cross-cutting modules used by multiple commands.
4. Scoring rubric with root-cause diagnosis to drive decision paths.
5. Persistent session state stored in a single markdown file.

## Command Interface

Proposed commands for the tool:

1. `kickoff` for onboarding and baseline profile capture.
2. `ingest jd` for job description parsing and competency extraction.
3. `tailor resume` for JD-aligned resume output with rationale and diff.
4. `tailor cover` for a cover letter aligned to JD and resume evidence.
5. `score` for ATS score, recruiter score, and risk checks.
6. `improve bullets` for targeted bullet rewrites and impact strengthening.
7. `version log` for tracking tailored variants per job.
8. `help` for command list and guidance.

## Persistent State File

Create a single state file, `resume_state.md`, with these sections:

1. Profile with target roles, seniority band, industry, and preferred tone.
2. Master resume as the canonical baseline text.
3. Achievements bank with raw STAR or CAR facts and metrics.
4. Skills and tech inventory with normalized terms and synonyms.
5. Target roles library containing each JD and extracted competencies.
6. Tailored versions with timestamps and job identifiers.
7. Recruiter notes with recurring feedback patterns.
8. ATS risk log with formatting and keyword gaps.

## Resume Tailoring Pipeline

Core workflow behind `tailor resume`:

1. Parse JD for competencies, toolstack, and priority ordering.
2. Map existing resume signals to JD requirements.
3. Identify gaps and suggest additions or rewrites.
4. Rewrite bullets using action, result, scope, and metric.
5. Run ATS optimization pass for headings, formatting, and keywords.
6. Run recruiter lens pass for top-scan impact and role alignment.

## Cover Letter Pipeline

Core workflow behind `tailor cover`:

1. Opening alignment to role and company.
2. Two or three proof points mapped to JD priorities.
3. Culture or mission fit statement.
4. Strong close with clear intent.
5. Ensure every claim is backed by resume evidence.

## Scoring and Quality Rubrics

ATS score components:

1. Parseability, headings, and structure.
2. Keyword coverage and relevance.
3. Title alignment to the target role.
4. Recency relevance for the last two to three roles.

Recruiter score components:

1. Impact clarity with metrics and outcomes.
2. Scope and ownership of work.
3. Role alignment and seniority fit.
4. Differentiation through unique projects or insights.

Risk and integrity checks:

1. Over-claiming detection.
2. Date and title consistency checks.
3. Keyword stuffing detection.

## Reference Docs Layout

Mirror the existing repo pattern with command docs:

1. `references/commands/kickoff.md`
2. `references/commands/ingest-jd.md`
3. `references/commands/tailor-resume.md`
4. `references/commands/tailor-cover.md`
5. `references/commands/score.md`
6. `references/commands/improve-bullets.md`
7. `references/commands/version-log.md`
8. `references/commands/help.md`
9. `references/cross-cutting.md`

## Feedback Loop and Versioning

Each run should update `resume_state.md` with:

1. Tailored version metadata.
2. Summary of changes and rationale.
3. ATS and recruiter score snapshots.

## Testing and Calibration

Calibrate with a test set:

1. Sample resumes across seniority levels.
2. Real job descriptions across company types.
3. Recruiter feedback if available.

Measure alignment between tool scores and real outcomes, then tune scoring weights.

## Expected Deliverables

1. Command-driven resume and cover letter tailoring tool.
2. Persistent user state and version history.
3. Dual-lens scoring system for ATS and recruiter views.
