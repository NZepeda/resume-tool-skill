# Command: score

## Purpose

Provide ATS and recruiter scores with risk checks.

## Required Inputs

- Resume text (master or tailored)
- Job description (optional but recommended)

## Workflow

1. Evaluate ATS score components.
2. Evaluate recruiter score components.
3. Run risk checks:
   - Over-claiming
   - Date/title inconsistencies
   - Keyword stuffing
4. Report scores and top risks.

## Output Blueprint

- Score Summary
- ATS Score Breakdown
- Recruiter Score Breakdown
- Risk Checks
- Missing Inputs (if blocked)

## State Updates

- Update ATS Risk Log if risks are found.

## Evidence Checks

- If a JD is not provided, state that scores are estimated.

## Example Input

Resume: (pasted resume)
JD: (optional)

## Example Output

Score Summary:
- ATS: 84 (estimated)
- Recruiter: 79 (estimated)

ATS Score Breakdown:
- Parseability: 23/25
- Keyword coverage: 28/35
- Title alignment: 16/20
- Recency relevance: 17/20

Recruiter Score Breakdown:
- Impact clarity: 22/30
- Scope/ownership: 20/25
- Role alignment: 19/25
- Differentiation: 18/20

Risk Checks:
- Keyword stuffing: None
- Date/title inconsistencies: None

## Missing Inputs

- "Paste the resume you want scored."
- "Paste the job description for tighter scoring (optional)."
