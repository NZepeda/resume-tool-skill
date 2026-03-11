# Resume Tool Skill

A command-driven resume and cover letter tailoring skill. It uses `SKILL.md` for behavior, `references/` for workflows, and `resume_state.md` for persistent state.

## How It Works

- Commands are explicit phrases (e.g., `tailor resume`).
- Each command loads `references/cross-cutting.md` and a command doc in `references/commands/`.
- Persistent state lives in `resume_state.md`.

## Commands

- `kickoff`: capture baseline profile and master resume.
- `ingest jd`: parse a job description into structured requirements.
- `tailor resume`: produce a JD-aligned resume variant with rationale and ATS pass.
- `tailor cover`: draft a JD-aligned cover letter backed by resume evidence.
- `score`: score a resume for ATS and recruiter fit with risk checks.
- `improve bullets`: rewrite bullets for impact and ATS alignment.
- `version log`: list tailored versions and change rationale.
- `help`: show this command list.

## State File

`resume_state.md` is the canonical source of truth. The schema is defined in `references/cross-cutting.md`.

## Fixtures

Sample inputs live under `tests/fixtures/`.
