```markdown
# SteelMind Nexus | Plant Decision Intelligence

> **Predictive Maintenance & OEE Command Center for Manufacturing**

SteelMind Nexus is an AI-native plant reliability and OEE decision-intelligence prototype that moves predictive maintenance from **"what might fail?"** to **"what should management do first, and why?"**

It combines equipment risk, production exposure, financial impact, maintenance requirements, spare-part availability, and scenario analysis into one executive decision workflow.

---

## 🎯 Problem

Traditional predictive-maintenance systems often stop at:

> **"This asset has a high probability of failure."**

But plant managers need to answer a more important question:

> **"Which failure should we act on first, what will it cost the business, and can we actually execute the intervention?"**

SteelMind Nexus addresses this gap by connecting:

**Asset Risk → Business Impact → Maintenance Decision → Spare Constraints → Scenario Analysis → Management Decision**

---

## 🚀 Core Differentiator

### Failure probability ≠ business priority

An asset with a slightly lower failure probability can still represent a much larger operational or financial risk.

SteelMind Nexus therefore prioritizes assets using:

- Failure risk
- Asset criticality
- Production exposure
- Financial exposure
- Downtime impact
- Spare availability
- Supplier lead time
- Intervention cost
- Maintenance urgency

---

## 🏭 Prototype Workflow

```text
Plant Telemetry
      │
      ▼
Asset Risk Intelligence
      │
      ▼
Business Impact Prioritization
      │
      ▼
Maintenance Decision
      │
      ├──────────────► Spare / Inventory Constraint
      │
      ▼
Scenario Analysis
      │
      ▼
Plant Decision Copilot
      │
      ▼
Human Management Decision
```

---

## 📊 Executive Command Center

The prototype provides a plant-level view of:

- Plant health
- OEE
- Production output
- Unplanned downtime
- Assets at risk
- Revenue exposure
- Potential protected value
- Maintenance value ratio
- OEE and production trends

Managers can drill from plant-level risk into the individual asset driving the exposure.

---

## 🔧 Example: PLTCM-02

The prototype identifies **PLTCM-02** as the highest-priority asset.

### Asset evidence

| Signal | Current | Baseline | Deviation |
|---|---:|---:|---:|
| Vibration | 8.4 mm/s | 6.3 mm/s | +33% |
| Bearing temperature | 87°C | 74°C | +17.6% |

### Business impact

- Failure risk: **91%**
- Business impact: **96/100**
- Production exposure: **620t**
- Financial exposure: **₹18.4L**
- Intervention cost: **₹0.8L**
- Maintenance Value Ratio: **23.0x**

### Recommended action

**Inspect / replace the drive-side bearing within 24 hours.**

---

## 📦 Execution Constraint

The system does not stop at recommending maintenance.

For the identified bearing:

- Required quantity: **2**
- Available stock: **0**
- Supplier lead time: **5 days**

This exposes an important operational blocker:

> A maintenance recommendation is only useful if the plant can execute it.

SteelMind Nexus therefore surfaces the spare constraint alongside the maintenance recommendation.

---

## 🔮 Scenario Simulator

The scenario engine allows management to compare maintenance timing.

### Act Now

- Failure risk: 91%
- Downtime: 4.1h
- Production exposure: 620t
- Financial exposure: ₹18.4L

### Delay 2 Days

- Failure risk: 97%
- Downtime: 7.2h
- Production exposure: 980t
- Financial exposure: ₹29.1L
- Additional modeled exposure: **₹10.7L**

The scenario values are **synthetic/model-based estimates for demonstration**, not guaranteed future outcomes.

---

## 🤖 Plant Decision Copilot

The prototype includes a deterministic, logic-backed decision copilot designed around common plant-management questions:

- Which asset should we prioritize?
- Why is PLTCM-02 high risk?
- Why is PLTCM-02 more important than PLTCM-04?
- What happens if maintenance is delayed by two days?
- Is a spare part blocking execution?
- Why did OEE decline?

The copilot connects the decision workflow rather than simply returning an isolated failure prediction.

---

## 🧩 Modular CoCo Skill Architecture

The repository contains four project-level Cortex Code skills:

### 1. Asset Risk Intelligence

Identifies elevated asset risk using telemetry, baselines, maintenance evidence, and degradation indicators.

### 2. Business Impact Prioritization

Ranks assets using failure risk together with production and financial exposure.

### 3. Maintenance Decision

Converts prioritized risk into an actionable maintenance recommendation while checking spare availability, lead time, and intervention cost.

### 4. Scenario Analysis

Compares maintenance timing scenarios and quantifies modeled changes in risk, downtime, production exposure, and financial exposure.

These skills are organized under:

```text
.cortex/
└── skills/
    ├── asset-risk-intelligence/
    │   └── SKILL.md
    ├── business-impact-prioritization/
    │   └── SKILL.md
    ├── maintenance-decision/
    │   └── SKILL.md
    └── scenario-analysis/
        └── SKILL.md
```

---

## 🏗️ Repository Structure

```text
steelmind-nexus/
│
├── .cortex/
│   └── skills/
│       ├── asset-risk-intelligence/
│       ├── business-impact-prioritization/
│       ├── maintenance-decision/
│       └── scenario-analysis/
│
├── app/
│   └── steelmind_nexus.tsx
│
├── data/
│   └── synthetic
│
├── docs/
│
└── README.md
```

---

## 🛡️ Governance & Prototype Scope

This prototype intentionally distinguishes between demonstration logic and production deployment.

### Current prototype

- Synthetic demonstration data
- Deterministic decision logic
- Modeled financial and production exposure
- Logic-backed decision copilot
- Modular CoCo skill definitions
- Human approval required for operational actions

### Not claimed as part of the current prototype

- Live plant IoT/SCADA connectivity
- Live ERP/CMMS integration
- Autonomous equipment shutdown
- Autonomous purchase-order creation
- Production-system control
- Guaranteed financial savings
- Production Snowflake deployment

The architecture is designed to be extended toward these capabilities in a production implementation.

---

## 🔭 Future Production Extension

SteelMind Nexus can be extended to connect:

```text
IoT / SCADA
     │
     ├── Sensor telemetry
     ├── Machine alarms
     └── Operating conditions
             │
             ▼
        Snowflake Data Layer
             │
     ┌───────┼────────┐
     ▼       ▼        ▼
   CMMS     ERP    Inventory
     │       │        │
     └───────┼────────┘
             ▼
      Decision Intelligence
             │
     ┌───────┼────────────┐
     ▼       ▼            ▼
   Risk   Business      Scenario
          Impact         Analysis
             │
             ▼
       Plant Decision
          Copilot
```

Potential future capabilities include:

- Multi-plant benchmarking
- Advanced predictive models
- Automated condition monitoring
- Work-order prioritization
- Spare-part demand forecasting
- Supplier lead-time risk
- Maintenance workforce optimization
- OEE root-cause analysis
- Closed-loop outcome tracking

---

## 💡 Key Insight

> **Failure probability tells us what might fail.  
> Business impact tells us what matters.  
> Execution constraints tell us what can actually be done.**

SteelMind Nexus combines all three to turn predictive maintenance into a **business decision system**.

---

## 🔗 Prototype

**Live Prototype:**  
https://share.gemini.google/YBxZXM8dRfw0

**GitHub Repository:**  
https://github.com/Suvasini911/steelmind-nexus

---

## ⚠️ Demo Disclaimer

SteelMind Nexus is a hackathon prototype using synthetic/model-based industrial data.

Financial exposure, production exposure, failure progression, and scenario outcomes are illustrative estimates intended to demonstrate the decision-intelligence workflow.
```

### Now save it

In VS Code:

1. Open `README.md`
2. `Ctrl + A`
3. Paste the README above
4. `Ctrl + S`

Then in the terminal run:

```powershell
git add README.md
git commit -m "Improve project documentation"
git push
```
