# Command: tailor cover

## Purpose

Draft a cover letter aligned to a JD and backed by resume evidence.

## Required Inputs

- Company name
- Role title
- Job description (or ingested role)
- Resume evidence (master resume or tailored resume)

## Workflow

1. Identify top 2-3 JD priorities.
2. Select evidence-backed proof points from resume.
3. Draft:
   - Opening alignment to role/company
   - Two to three proof points
   - Culture/mission fit
   - Strong close with intent
4. Verify every claim is supported by resume evidence.

## Output Blueprint

- Summary of Chosen Proof Points
- Cover Letter Draft
- Evidence Check (claims -> resume evidence)
- Missing Inputs (if blocked)

## State Updates

- Add a Tailored Versions entry referencing the cover letter variant.

## Evidence Checks

- Every claim must be traceable to resume evidence.

## Example Input

Company: ZenithPay
Role: Senior Product Manager, Payments
JD: (pasted text)
Resume: (pasted resume)

## Example Output

Summary of Chosen Proof Points:
- Payments API ownership at AtlasPay
- Fraud loss reduction via risk scoring feature
- Onboarding conversion improvements

Cover Letter Draft:
[3-4 paragraph draft]

Evidence Check:
- "Led payments API roadmap" -> AtlasPay bullet 1
- "Reduced fraud losses" -> AtlasPay bullet 3
- "Improved onboarding" -> AtlasPay bullet 2

## Missing Inputs

- "Which company and role is this for?"
- "Paste the job description if it's not ingested."
- "Paste the resume evidence you want me to use."
