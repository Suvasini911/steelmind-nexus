---
name: business-impact-prioritization
description: Prioritize industrial asset risks using production exposure, financial exposure, criticality, downtime impact, and operational constraints.
---

# Business Impact Prioritization

## Purpose

Convert equipment failure risk into business priority.

The highest failure probability is not automatically the highest management priority.

## When to Use

Use this skill when the user asks:

- Which asset should management prioritize?
- Which failure matters most to production?
- What is the business impact of an asset failure?
- Which asset creates the greatest financial exposure?
- Why is one asset more important than another?
- What should be addressed first?

## Inputs

Use available:

- Failure risk
- Asset criticality
- Production exposure
- Downtime exposure
- Financial exposure
- Revenue at risk
- OEE impact
- Inventory constraints
- Operational urgency

## Workflow

1. Identify assets with meaningful failure risk.
2. Quantify production exposure.
3. Quantify financial exposure where data supports it.
4. Consider asset criticality and operational role.
5. Consider downtime consequences.
6. Consider execution constraints.
7. Rank assets by overall business priority.
8. Explain why the top-ranked asset outranks alternatives.

## Priority Logic

Business priority should consider:

- Failure likelihood
- Business criticality
- Production impact
- Financial exposure
- Urgency
- Execution constraints

Do not rank assets using failure probability alone.

## SteelMind Nexus Example

PLTCM-02:

- Failure risk: 91%
- Business impact: 96/100
- Production exposure: 620t
- Financial exposure: ₹18.4L

PLTCM-04:

- Failure risk: 84%
- Business impact: 82/100
- Production exposure: 310t
- Financial exposure: ₹7.2L

Therefore PLTCM-02 receives higher business priority despite the difference in failure probability being relatively modest.

## Output

Return:

- Priority ranking
- Asset
- Failure risk
- Business impact
- Production exposure
- Financial exposure
- Criticality
- Main reason for ranking
- Management implication

## Important

Financial values in the SteelMind Nexus prototype are modeled/synthetic estimates unless connected to validated enterprise data.

Never describe modeled exposure as guaranteed financial loss or guaranteed savings.