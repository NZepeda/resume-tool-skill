# Command: begin

## Purpose

Initialize `resume_state.md` with baseline profile and master resume.

## Required Inputs

- Target role(s)
- Seniority band
- Industry focus
- Preferred tone
- Master resume text (or a resume file pasted in full)

## Workflow

1. Ask for any missing required inputs (one question at a time).
2. Create `resume_state.md` using the schema in `references/cross-cutting.md`.
3. Populate Profile and Master Resume sections.
4. Initialize empty tables/sections for the remaining schema.
5. Confirm a brief summary of what was captured.

## Output Blueprint

- Summary
- Captured Inputs
- Next Step Suggestion
- Missing Inputs (if blocked)

## State Updates

- Write full `resume_state.md` if missing.
- If it exists, update Profile and Master Resume only (do not overwrite other sections).

## Evidence Checks

- Do not infer roles, metrics, or achievements that are not explicitly provided.

## Example Input

- Target roles: Senior Product Manager, Growth PM
- Seniority band: Senior
- Industry focus: Fintech
- Tone: Direct and metrics-focused
- Master resume: (pasted resume text)

## Example Output

Summary:
- Created `resume_state.md` with baseline profile and master resume.

Captured Inputs:
- Roles: Senior Product Manager, Growth PM
- Seniority: Senior
- Industry: Fintech
- Tone: Direct and metrics-focused

Next Step Suggestion:
- Run `ingest jd` with a target job description.

## Missing Inputs

Ask for the single most blocking input first:
- "What target role(s) are you aiming for?"
- "What seniority band should I use?"
- "What industry focus should I assume?"
- "What tone do you want in the materials (e.g., direct, formal, warm, concise)?"
- "Paste your current resume text so I can build the master resume section."
