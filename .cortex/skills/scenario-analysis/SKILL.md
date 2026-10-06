---
name: scenario-analysis
description: Compare maintenance timing scenarios and quantify modeled changes in failure risk, downtime, production exposure, and financial exposure.
---

# Scenario Analysis

## Purpose

Help plant managers understand the consequence of delaying or accelerating maintenance.

## When to Use

Use this skill when the user asks:

- What happens if we delay maintenance?
- What if we act today?
- What is the cost of waiting?
- Compare maintenance timing options.
- How much additional production is at risk?
- How does delay change financial exposure?

## Inputs

Use:

- Current failure risk
- Maintenance timing
- Expected downtime
- Production exposure
- Financial exposure
- Historical or modeled degradation assumptions

## Workflow

1. Establish the current intervention scenario.
2. Define alternative timing scenarios.
3. Estimate risk progression for each scenario.
4. Estimate downtime impact.
5. Estimate production exposure.
6. Estimate modeled financial exposure.
7. Compare each scenario with acting now.
8. Clearly identify modeled assumptions.

## SteelMind Nexus Example

Act Now:

- Risk: 91%
- Downtime: 4.1h
- Production exposure: 620t
- Financial exposure: ₹18.4L

Delay 2 Days:

- Risk: 97%
- Downtime: 7.2h
- Production exposure: 980t
- Financial exposure: ₹29.1L

Modeled additional exposure:

₹29.1L - ₹18.4L = ₹10.7L

## Output

Return a comparison table:

| Scenario | Risk | Downtime | Production Exposure | Financial Exposure |
|---|---:|---:|---:|---:|
| Act Now | ... | ... | ... | ... |
| Delay 1 Day | ... | ... | ... | ... |
| Delay 2 Days | ... | ... | ... | ... |
| Delay 3 Days | ... | ... | ... | ... |
| Delay 5 Days | ... | ... | ... | ... |

Then provide:

- Recommended scenario
- Main reason
- Incremental modeled exposure
- Key assumptions

## Important

Scenario results are modeled estimates in the prototype.

Do not present them as guaranteed future outcomes.