# Command: ingest jd

## Purpose

Parse a job description and store structured requirements in `resume_state.md`.

## Required Inputs

- Company name
- Role title
- Full job description text

## Workflow

1. Ask for any missing required inputs (one question at a time).
2. Extract:
   - Top competencies (3-7)
   - Toolstack and technologies
   - Priority ordering (ranked)
   - Noted gaps (if resume evidence exists)
3. Write a new entry under Target Roles Library.
4. Provide a concise summary and confirm the stored entry.

## Output Blueprint

- Summary
- Extracted Competencies
- Toolstack
- Priority Ordering
- Missing Inputs (if blocked)

## State Updates

- Add a new Target Roles Library entry with date and extracted fields.

## Evidence Checks

- Do not claim gaps unless resume evidence exists in `resume_state.md` or provided text.

## Example Input

Company: ZenithPay
Role: Senior Product Manager, Payments
JD: (pasted text)

## Example Output

Summary:
- Stored JD for ZenithPay — Senior Product Manager, Payments.

Extracted Competencies:
- Payments domain knowledge
- API platform experience
- Fraud/risk management
- Product analytics
- Cross-functional leadership

Toolstack:
- APIs, SQL, experimentation, fraud tooling

Priority Ordering:
1. Payments domain + API platform
2. Fraud/risk management
3. Analytics + experimentation
4. Cross-functional leadership

## Missing Inputs

- "What company is this for?"
- "What role title should I use?"
- "Paste the full job description text."
