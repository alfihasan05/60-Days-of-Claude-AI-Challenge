AI Supply Chain Control Tower — Day 31

 Overview

Built an interactive **AI Supply Chain Control Tower** that simulates the role of a Head of Operations managing a global supply chain under pressure.

The application runs completely offline as a single HTML file using only **HTML, CSS, and Vanilla JavaScript**.

#Dashboard

![Control Tower Dashboard](screenshots/control-tower-dashboard.png)

The dashboard provides real-time visibility into:

- Service Level
- Customer Satisfaction
- Inventory Health
- Transportation Efficiency
- Operating Cost
- Revenue Protected
- Operations Score
- Remaining Time
- Active Supply Chain Alerts
- Network Health
- Operational Event Stream
- Risk Areas

## Supply Chain Alerts

The simulation generates realistic operational disruptions:

- Port Congestion
- Supplier Delay
- Truck Breakdown
- Warehouse Stockout
- Customs Inspection
- Demand Spike
- Factory Machine Failure
- Weather Disruption
- Wrong Inventory Count
- Damaged Shipment

Each alert includes its business impact, priority, decision window, and multiple response options.

![Active Alerts](screenshots/active-alerts.png)

## Decision System

Every operational decision creates different business consequences.

Possible actions include:

- Expedite Shipment
- Use Backup Supplier
- Reroute Trucks
- Increase Production
- Transfer Inventory
- Approve Air Freight
- Delay Decision
- Ignore

Good decisions improve operational KPIs and protect revenue.

Poor decisions increase risk, operating cost, and customer impact.

Some decisions also trigger delayed consequences to simulate real-world supply chain effects.

## Final Score

![Final Score](screenshots/final-score.png)

**Final Supply Chain Score:** 278

**Performance Grade:** A+

**Service Level:** 96%

**Customer Satisfaction:** 93%

**Inventory Health:** 90%

**Transportation Efficiency:** 91%

**Alerts Resolved:** 24

**Correct Decisions:** 20

**Wrong Decisions:** 4

**Revenue Protected:** $1.61M

**Operating Cost:** $96K

> Update these values with the exact results from your final simulation run if they differ.

## Key Learnings

### 1. Prioritization is critical

A control tower cannot treat every disruption equally. High-impact problems affecting customers, inventory, and revenue need immediate attention.

### 2. Every decision involves a trade-off

Expediting can protect service levels but increase cost. Backup suppliers can reduce supply risk but affect efficiency.

The best decision is not always the fastest decision.

### 3. Delayed consequences matter

Some operational decisions create effects several seconds later. This demonstrates why supply chain leaders must consider downstream consequences instead of optimizing only for the immediate result.

### 4. Visibility improves decision quality

Combining alerts, KPIs, risk indicators, and event logs creates a single source of operational visibility.

### 5. Supply chain optimization is a business problem

The goal is not simply to move products faster.

The real objective is to balance:

**Service + Customer Experience + Inventory + Transportation + Cost + Revenue Protection**

## Product Design Insight

The biggest UX lesson from this project was:

> A good operations dashboard should reduce cognitive load, not increase it.

The interface follows a simple decision flow:

**Alert → Business Impact → Recommended Action → KPI Consequence**

This helps an operator quickly understand what needs attention and why it matters.

## Technical Implementation

The project was intentionally built without frameworks or backend services.

### Technologies

- HTML5
- CSS3
- Vanilla JavaScript
- CSS Grid
- Responsive Design
- Browser DOM APIs

### No External Dependencies

- No React
- No Vue
- No Angular
- No Tailwind
- No Bootstrap
- No external APIs
- No backend
- No database
- No external libraries

The entire simulator is contained inside:

`ai-supply-chain-control-tower.html`

## Screenshots

Add the following images to the repository:

```text
screenshots/
├── control-tower-dashboard.png
├── active-alerts.png
├── final-score.png
└── mobile-dashboard.png
