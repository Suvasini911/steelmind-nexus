---
name: maintenance-decision
description: Convert prioritized equipment risk into an actionable maintenance recommendation using evidence, spare availability, lead time, intervention cost, and business exposure.
---

# Maintenance Decision

## Purpose

Translate prioritized equipment risk into an executable maintenance recommendation.

This skill answers:

"What should the plant do next?"

## When to Use

Use this skill when the user asks:

- What maintenance action should we take?
- Should we inspect or replace the component?
- Which spare part is required?
- Is maintenance execution blocked?
- What should be done within the next 24 hours?
- What is the value of intervention?

## Inputs

Use available:

- Asset risk
- Failure mode
- Evidence
- Business impact
- Recommended component
- Spare inventory
- Required quantity
- Supplier lead time
- Intervention cost
- Maintenance resources
- Production constraints

## Workflow

1. Review asset failure risk and supporting evidence.
2. Review business impact.
3. Identify the likely component or failure mode.
4. Check spare availability.
5. Compare available stock with required quantity.
6. Check supplier lead time if stock is insufficient.
7. Estimate intervention cost.
8. Compare intervention cost with modeled exposure.
9. Recommend the lowest-risk practical intervention.
10. Identify execution blockers.
11. Require human approval before irreversible operational action.

## SteelMind Nexus Example

Asset:

PLTCM-02

Issue:

Drive-side bearing degradation

Recommendation:

Inspect/replace drive-side bearing within 24 hours.

Spare:

XYZ-6208

Stock:

0

Required:

2

Lead time:

5 days

Intervention cost:

₹0.8L

Modeled financial exposure:

₹18.4L

Modeled exposure-to-intervention-cost ratio:

23.0x

## Value Ratio

Calculate:

Financial exposure / intervention cost

For the example:

₹18.4L / ₹0.8L = 23.0x

Call this a:

"Maintenance Value Ratio"

Do not label this conventional ROI.

## Output

Return:

- Recommended action
- Asset
- Failure mode
- Required component
- Spare status
- Lead time
- Intervention cost
- Modeled financial exposure
- Maintenance value ratio
- Execution blocker
- Required approval

## Governance

The skill must not autonomously:

- issue a purchase order
- release a work order
- shut down equipment
- modify production schedules
- approve spending

Such actions require human authorization.