# Command: version log

## Purpose

List tailored versions and their rationale.

## Required Inputs

- None (reads from `resume_state.md`)

## Workflow

1. Load `resume_state.md`.
2. Display Tailored Versions table.
3. Summarize the most recent 3-5 variants.

## Output Blueprint

- Tailored Versions Table
- Recent Summary
- Missing Inputs (if blocked)

## State Updates

- None.

## Evidence Checks

- Only report versions present in the state file.

## Example Output

Tailored Versions Table:
| Date | Company | Role | Variant | Summary | ATS Score | Recruiter Score | Notes |
| ---- | ------- | ---- | ------- | ------- | --------- | --------------- | ----- |
| 2026-03-10 | ZenithPay | Sr PM, Payments | ats | Added payments API focus | 86 | 79 | Added fraud keywords |

Recent Summary:
- 2026-03-10: ZenithPay — Emphasized payments API and fraud reduction.

## Missing Inputs

- "I can't find `resume_state.md`. Run `begin` first or provide the file."
