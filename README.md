# Resume Tool Skill

A command-driven resume and cover letter tailoring skill with strict evidence rules, ATS-aware formatting, and persistent session state.

## Quick Start

Use this sequence for the fastest path from raw inputs to a tailored resume:

1. `begin`
2. `ingest jd`
3. `tailor resume`
4. `score`

## Who This Is For

- Job seekers who want ATS-friendly, evidence-backed resume and cover letter edits.
- Users who want a structured, repeatable workflow rather than free-form drafting.

## What It Does / Does Not Do

Does:

- Tailor resumes and cover letters to a specific job description.
- Enforce evidence-only claims and log ATS risks.
- Keep version history across sessions.

Does not:

- Invent metrics, skills, or outcomes you did not provide.
- Skip questions when required evidence is missing.

## How It Works

- Commands are explicit phrases (e.g., `tailor resume`).
- Each command loads `references/cross-cutting.md` and a command doc in `references/commands/`.
- Persistent state lives in `resume_state.md`.

## Commands

- `begin`: capture baseline profile and master resume.
- `ingest jd`: parse a job description into structured requirements.
- `tailor resume`: produce a JD-aligned resume variant with rationale and ATS pass.
- `tailor cover`: draft a JD-aligned cover letter backed by resume evidence.
- `score`: score a resume for ATS and recruiter fit with risk checks.
- `improve bullets`: rewrite bullets for impact and ATS alignment.
- `version log`: list tailored versions and change rationale.
- `help`: show this command list.

## Command Syntax Notes

- Commands must match the exact phrase (lowercase, space-separated).
- If evidence is missing, the tool will ask one question at a time.

## Example Inputs and Outputs

Example (resume tailoring):

```
tailor resume
```

You should expect:

- A resume variant aligned to the most important JD requirements.
- A short rationale explaining what changed and why.
- ATS risk notes if gaps are detected.

Example (scoring):

```
score
```

You should expect:

- ATS score and recruiter score.
- Strengths first, then gaps, with confidence labels.

## File Roles

- `SKILL.md`: behavior, rules, and command registry.
- `references/`: command workflows, schemas, and cross-cutting rules.
- `resume_state.md`: canonical session state and version tracking.
- `tests/fixtures/`: sample resumes and job descriptions.

## State Lifecycle

- `resume_state.md` is written on `begin`, `ingest jd`, `tailor resume`, `tailor cover`, `score`, and `improve bullets`.
- Mid-session saves happen automatically after major steps.
- State is confirmed saved when the session ends.

## Repo Layout

- `references/commands/`: per-command schemas and output formats.
- `references/cross-cutting.md`: shared rules (evidence, scoring, ATS checks).
- `tests/fixtures/`: sample inputs for development and testing.

## Troubleshooting

- Missing evidence: provide the metric, tool, or outcome requested.
- Stale targets: update your target roles when asked at session start.
- Unexpected output: confirm you ran the exact command phrase.
