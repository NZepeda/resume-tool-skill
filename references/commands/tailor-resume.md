# Command: tailor resume

## Purpose

Generate a JD-aligned resume variant with rationale and ATS pass.

## Required Inputs

- Job description (or a previously ingested role)
- Master Resume (from `resume_state.md`)

## Workflow

1. Identify the target role entry in Target Roles Library.
2. Map JD requirements to resume evidence.
3. Identify gaps and propose edits.
4. Rewrite bullets using the Bullet Rewrite Formula.
5. Run ATS optimization pass.
6. Provide a recruiter lens pass (top-scan impact and role alignment).
7. Summarize the changes and scores.

## Output Blueprint

- Summary
- Mapping Table (JD requirement -> resume evidence / gap)
- Edited Resume (or edited sections only)
- Rationale (top 3-5 changes)
- ATS Pass Notes
- Recruiter Lens Notes
- Missing Inputs (if blocked)

## State Updates

- Add a Tailored Versions entry with date, company, role, variant, summary, scores.
- Update ATS Risk Log if risks are found.

## Evidence Checks

- Every change must map to a JD requirement or resume evidence.
- Flag missing metrics instead of inventing them.

## Example Input

Company: ZenithPay
Role: Senior Product Manager, Payments
JD: (pasted text)
Master Resume: (pasted resume)

## Example Output

Summary:
- Emphasized payments API ownership and fraud reduction impact.

Mapping Table:
| JD Requirement | Priority | Resume Evidence | Gap | Notes |
| -------------- | -------- | --------------- | --- | ----- |
| API platforms | High | Led payments API roadmap at AtlasPay | None | Highlighted in first role |
| Fraud reduction | High | Launched risk scoring feature (18% loss reduction) | None | Moved to top bullet |
| SQL/analytics | Medium | A/B testing program, analytics dashboards | Weak | Add explicit SQL usage |

Rationale:
- Reordered bullets to lead with payments + fraud wins.
- Added keywords: "API platform", "risk scoring".
- Flagged missing explicit SQL mention.

ATS Pass Notes:
- Standard headings used; keyword coverage improved.

Recruiter Lens Notes:
- Strong first-scan impact with domain alignment.

## Missing Inputs

- "Which company/role should I tailor for?"
- "Paste the full job description if not already ingested."
- "Paste your master resume if it's not in the state file."
