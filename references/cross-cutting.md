# Cross-Cutting Guidance

This document defines shared rules and modules used by all commands.

## Evidence Rules

- Do not fabricate resume content, metrics, tools, or company details.
- Only claim alignment when there is a direct mapping to resume evidence.
- When data is missing, ask for it and stop. One question at a time.

## State Schema (resume_state.md)

```markdown
# Resume State — [Name]

Last updated: [date]

## Profile

- Target role(s):
- Seniority band:
- Industry focus:
- Preferred tone:

## Master Resume

[Canonical baseline resume text]

## Achievements Bank

| ID | Title | Situation | Action | Result | Metrics | Notes |
| -- | ----- | --------- | ------ | ------ | ------- | ----- |

## Skills Inventory

| Skill | Variants / Synonyms | Evidence |
| ----- | ------------------- | -------- |

## Target Roles Library

### [Company] — [Role]

- Date ingested:
- Job description:
- Top competencies:
- Toolstack:
- Priority ordering:
- Noted gaps:

## Tailored Versions

| Date | Company | Role | Variant | Summary | ATS Score | Recruiter Score | Notes |
| ---- | ------- | ---- | ------- | ------- | --------- | --------------- | ----- |

## Recruiter Notes

- [date]: [pattern or feedback]

## ATS Risk Log

- [date]: [risk] — [fix]
```

## ATS Optimization Rules

- Use standard headings: Summary, Experience, Skills, Education.
- Avoid columns, tables, and graphics in the final output.
- Prefer simple bullet points, 1-2 lines each.
- Keywords should be natural, not repeated.
- Use consistent tense and verb forms.

## ATS Risk Checks (Concrete)

- **Hidden text or graphics**: Flag any non-textual content or layout tricks.
- **Non-standard headings**: Require standard section labels.
- **Excessive formatting**: Tables, columns, or heavy styling.
- **Keyword stuffing**: Repeating the same keyword 5+ times in a short section.
- **Inconsistent dates**: Overlapping roles or missing months/years.
- **Title misalignment**: Resume title differs from target role without explanation.

If any risk is present, add an entry to ATS Risk Log with a suggested fix.

## Bullet Rewrite Formula

Target pattern:

- Action verb + scope + method + result + metric

If metric is missing, flag it and request it.

## Mapping Rules

- Map each JD requirement to resume evidence or mark it as a gap.
- A gap is either missing evidence or weakly evidenced.
- Keep a compact mapping table in the response when possible.

## Mapping Table Format

Use this table format when producing mappings:

| JD Requirement | Priority | Resume Evidence | Gap | Notes |
| -------------- | -------- | --------------- | --- | ----- |

Priority values: High / Medium / Low. Gap values: None / Weak / Missing.

## Gap Handling

- **Missing**: No resume evidence exists. Ask for missing projects or accomplishments.
- **Weak**: Evidence exists but lacks scope or metrics. Ask for scale, outcomes, or tooling details.
- **Metric missing**: Do not estimate. Flag it and request the metric explicitly.

## Scoring Rubric (Lightweight)

ATS Score (0-100):
- Parseability (25)
- Keyword coverage (35)
- Title alignment (20)
- Recency relevance (20)

Recruiter Score (0-100):
- Impact clarity (30)
- Scope/ownership (25)
- Role alignment (25)
- Differentiation (20)

If scores are estimated, say so explicitly.

## Recruiter Lens Heuristics (Concrete)

- First 6 seconds: top 2 bullets should show role-relevant impact with metrics.
- Role alignment: recent role title and first role bullets should match the target role.
- Scope: call out team size, budget, scale, or system footprint when present.
- Differentiation: at least one bullet should include a unique project, domain insight, or hard-won result.
- Recency: the last 2-3 roles should map to the JD’s core requirements.

## Tailored Version Conventions

- Variant naming: `base`, `ats`, `recruiter`, or a short descriptor (e.g., `fintech-focus`).
- Summary: 1-2 lines describing the most important changes.
- Scores: If either score is omitted, state why.

## Response Templates (Global)

- Use the templates inside each command doc.
- Include `Missing Inputs` when the workflow cannot proceed.
