# Day 30 — Build an AI Business Continuity Simulator

## Project Overview

For Day 30, I built an interactive **AI Business Continuity Simulator** that teaches how companies respond when unexpected disruptions affect their operations.

Instead of simply reading about risk management, the user experiences a realistic business disruption, evaluates the situation, chooses a response strategy, and sees how each decision affects the company.

## What the Simulator Does

The simulation starts by generating a random business scenario with:

- Company type
- Industry
- Critical operations
- Customer dependency
- Disruption severity
- Available resources
- Recovery pressure

The player then works through a series of crisis-management decisions.

## Crisis Scenarios

The simulator can introduce disruptions such as:

- Supplier shutdown
- Logistics disruption
- Technology outage
- Sudden demand spike
- Facility disruption
- Workforce shortage
- Cyber-related operational interruption
- Critical inventory shortage

## Decision Areas

The player must decide how to respond across several areas:

### 1. Immediate Response

Identify what should be protected first.

Possible priorities include:

- Customers
- Revenue-generating operations
- Critical inventory
- Employees
- Technology systems

### 2. Resource Allocation

Decide where limited resources should go during the disruption.

The player learns that allocating everything to one area can create secondary problems elsewhere.

### 3. Supplier & Partner Response

Evaluate whether to:

- Continue with the existing supplier
- Activate backup suppliers
- Split orders
- Search for alternative sources

### 4. Customer Communication

Choose how the company communicates with customers during the crisis.

The simulation demonstrates the relationship between transparency, trust, service expectations, and reputation.

### 5. Recovery Strategy

Create a recovery plan that balances:

- Speed
- Cost
- Risk
- Customer impact
- Long-term resilience

## Live Business Metrics

The dashboard updates after every decision.

| Metric | Meaning |
|---|---|
| Business Continuity | Ability to keep critical operations running |
| Financial Impact | Cost and revenue pressure caused by the crisis |
| Customer Trust | Likelihood that customers remain confident in the company |
| Operational Risk | Exposure to additional disruptions |
| Recovery Speed | How quickly normal operations can return |
| Resilience | Ability to withstand future disruptions |

## Optimization Dashboard

The final dashboard provides a complete assessment of the crisis response.

It includes:

- Overall Continuity Score
- Strongest Decision
- Weakest Decision
- Biggest Operational Risk
- Financial Impact
- Customer Impact
- Recovery Readiness
- Recommended Next Actions

## Final Score

The simulator generates a score from **0–100**.

### 90–100 — Crisis Ready

The company handled the disruption exceptionally well and created strong long-term resilience.

### 75–89 — Strong Response

The immediate crisis was managed effectively, with a few areas that could be improved.

### 60–74 — Recovering

The company survived the disruption but exposed several weaknesses.

### 40–59 — High Risk

The response reduced some damage but left important vulnerabilities unresolved.

### 0–39 — Critical

The response created major operational, financial, or customer consequences.

## Screenshots

### Welcome Screen

`screenshots/01-welcome.png`

Introduces business continuity in simple language and explains how the simulation works.

### Crisis Scenario

`screenshots/02-crisis-scenario.png`

Shows the randomly generated company and disruption.

### Decision Screen

`screenshots/03-decision-screen.png`

Shows the current crisis-management decision with explanations and trade-offs.

### Live Dashboard

`screenshots/04-live-dashboard.png`

Shows how the business metrics change after each decision.

### Final Assessment

`screenshots/05-final-dashboard.png`

Shows the final continuity score, strengths, weaknesses, biggest risk, and recommended actions.

## Generated Application

**File:** `business-continuity-simulator.html`

The application is designed as a single-file interactive experience.

It uses:

- React
- React state
- HTML
- CSS
- JavaScript
- Responsive UI
- Randomized scenarios
- Interactive decision logic
- Live metric calculations

No backend or database is required.

## Key Learnings

1. **Business continuity is about preparation, not just reaction.**

2. **The fastest response is not always the best response.** A rushed decision can create additional problems later.

3. **Prioritization becomes critical during a crisis.** Companies rarely have unlimited people, money, inventory, or time.

4. **Customer communication is part of crisis management.** Operational problems can become reputation problems when customers are left without clear information.

5. **Backup suppliers reduce dependency risk.** A company becomes more resilient when critical operations do not depend on a single point of failure.

6. **Recovery should be designed in stages.** Stabilizing the business comes first, followed by restoring normal operations and strengthening the system.

7. **Cost optimization alone can create hidden risk.** A very lean operation may become fragile when an unexpected disruption occurs.

8. **Resilience requires trade-offs.** Extra inventory, backup suppliers, alternate routes, and redundancy cost money, but they can protect the business when normal operations fail.

## Biggest Insight

The biggest lesson from this simulation was:

> **A resilient business is not one that avoids every disruption. It is one that can absorb a disruption, keep its most important operations running, recover quickly, and become stronger afterward.**

## GitHub Repository Structure

```text
business-continuity-simulator/
├── business-continuity-simulator.html
├── README.md
└── screenshots/
    ├── 01-welcome.png
    ├── 02-crisis-scenario.png
    ├── 03-decision-screen.png
    ├── 04-live-dashboard.png
    └── 05-final-dashboard.png
