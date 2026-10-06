---
name: asset-risk-intelligence
description: Analyze industrial asset telemetry and maintenance evidence to identify equipment failure risk, likely failure mode, risk window, and supporting evidence.
---

# Asset Risk Intelligence

## Purpose

Identify which industrial assets show elevated failure risk and explain the evidence behind the risk assessment.

This skill is the first stage of the SteelMind Nexus reliability workflow.

## When to Use

Use this skill when the user asks:

- Which asset is most likely to fail?
- Which equipment is at highest risk?
- Why is an asset considered high risk?
- What evidence indicates degradation?
- What failure mode is emerging?
- Which assets require reliability attention?

## Inputs

Use available plant data such as:

- Asset ID
- Sensor telemetry
- Vibration
- Temperature
- Pressure
- Current
- Speed
- Historical baseline
- Maintenance history
- Previous failures
- Operating conditions
- Alarm history

## Workflow

1. Identify the relevant assets.
2. Compare current telemetry against historical or engineering baselines.
3. Detect abnormal trends or deviations.
4. Examine maintenance and failure history when available.
5. Identify the most plausible degradation or failure mode.
6. Estimate failure risk using the available evidence.
7. Assign a risk window where supported by the data.
8. Explain the evidence supporting the assessment.
9. Clearly distinguish observed evidence from inferred conclusions.

## Output

Return a structured assessment containing:

- Asset ID
- Failure risk
- Risk level
- Likely failure mode
- Risk window
- Key evidence
- Baseline comparison
- Evidence confidence
- Recommended next diagnostic action

## Evidence Rules

Do not claim that a sensor proves failure.

Use language such as:

- "indicates elevated risk"
- "consistent with degradation"
- "supports inspection"
- "suggests abnormal operating behavior"

Separate:

1. Observed telemetry
2. Historical comparison
3. Inference
4. Recommended action

## SteelMind Nexus Example

For PLTCM-02:

- Vibration: 8.4 mm/s
- Baseline: 6.3 mm/s
- Deviation: approximately +33%
- Bearing temperature: 87°C
- Baseline: 74°C
- Temperature deviation: approximately +17.6%
- Failure risk: 91%
- Likely issue: drive-side bearing degradation

The evidence should support further inspection rather than being presented as a guaranteed failure.

## Output Principle

Failure probability answers:

"What might fail?"

The next SteelMind Nexus skills determine:

"What matters most?"

and

"What should management do?"