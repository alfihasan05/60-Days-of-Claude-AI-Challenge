 Day 29 — Operation Lifeline: Supply Chain Crisis Lab

Project Overview

For Day 29 of the #60DayClaudeChallenge, I built **Operation Lifeline: Supply Chain Crisis Lab** — an interactive simulation that puts the player in the role of a supply chain crisis leader.

Instead of simply reading about supply chain management, the player has to make decisions under pressure and see how those decisions affect the business.

What I Built

The simulation randomly creates a fictional company with different:

Industries
Revenue levels
Factories
Warehouses
Suppliers
Inventory coverage
Supplier lead times
 Operating countries
It then introduces a random crisis such as:
Factory fire
Supplier bankruptcy
Port strike
Cyberattack
Flood
Raw material shortage
Political conflict
Shipping delay

Every playthrough can produce a different scenario and outcome.

Simulation Flow

 1. Mission Brief

The player starts with a short explanation of the mission and enters the crisis simulation.

The goal is simple:

**Keep the business running while protecting customers, cash and long-term resilience.**

---

### 2. Understand the Company

Before making any decision, the simulation presents the company's operating profile.

Key information includes:

- Annual revenue
- Number of factories
- Number of warehouses
- Supplier network
- Inventory buffer
- Average lead time
- Countries involved
- Core product category

This creates context before the player has to act.

---

3. Crisis Event

A random disruption is introduced.

The crisis explains:

- What happened
- Why it matters
- Immediate operational exposure
- Potential business consequences

This helped make the simulation understandable even for someone with no prior supply chain experience.

---

 4. War Room

The player receives six possible response actions and must select exactly three.

Possible actions include:

1. Activate Backup Suppliers
2. Use Safety Stock
3. Premium Air Freight
4. Prioritize Strategic Customers
5. Shift Production Capacity
6. Freeze Non-Critical Orders

Each action has a different trade-off.

For example:

Premium Air Freight**

Improves delivery speed but increases emergency transportation costs.

Use Safety Stock**

Protects customer deliveries immediately but reduces the remaining inventory buffer.

The objective is not to find a perfect answer.

The objective is to understand the consequences of each decision.

5. Business Impact Dashboard

After the War Room decisions, the simulation updates five important metrics:

| Metric | What It Measures |
|---|---|
| Cost Control | How efficiently emergency spending is managed |
| Inventory Health | How well available inventory is protected |
| Profit Protection | Ability to reduce financial damage |
| Delivery Speed | Ability to maintain customer commitments |
| Customer Satisfaction | Impact on customer relationships |

This turns operational decisions into measurable business outcomes.

---
6. Supplier Negotiation

The next stage is a four-round negotiation with a strategic supplier.

Every decision affects:

- Trust
- Price Advantage
- Lead-Time Advantage

The negotiation tests whether the player can balance short-term pressure with long-term supplier relationships.

A low price is not automatically the best result.

A supplier relationship with better trust and faster recovery can be more valuable during a crisis.

---

 7. CEO Boardroom

The player then enters five executive decision scenarios.

The questions focus on:

- Prioritization
- Risk management
- Quality vs. speed
- Cross-functional leadership
- Crisis recovery
- Learning from failure

The purpose is to move from tactical decision-making to executive thinking.

---

8. AI Strategy

The player receives a limited AI investment budget and must select two capabilities.

Available options:

Demand Forecasting

Improve visibility into changing customer demand.

Inventory Optimization

Create smarter safety-stock decisions across the network.

 Supplier Risk Monitoring

Detect supplier exposure and disruption signals earlier.

Warehouse Vision

Improve warehouse accuracy and operational visibility.

Procurement Copilot

Support procurement teams with faster sourcing and negotiation decisions.

The player must choose based on the company's weaknesses rather than simply selecting the most impressive technology.

 Executive Dashboard

At the end of the simulation, the player receives an overall crisis score from 0–100.

The dashboard evaluates:

- Overall Crisis Score
- Leadership
- Negotiation
- Resilience
- Cost Control
- Risk Management
- Customer Satisfaction

It also generates personalized feedback.

 Biggest Mistake

Identifies the area where the player's decisions created the greatest weakness.

 Best Decision

Highlights the strongest crisis-response decision.

### Expert Recommendation

Provides a strategic recommendation for improving future resilience.

### Lessons Learned

Summarizes the key concepts demonstrated during the simulation.

---

# Key Learnings

## 1. Supply chain decisions are connected

A decision that improves delivery speed can increase costs.

A decision that saves money can hurt customer satisfaction.

A decision that protects inventory today can create shortages tomorrow.

The important lesson is to optimize the **system**, not one metric.

---

## 2. Resilience requires options

Backup suppliers, alternative transportation routes and flexible production capacity may look inefficient during normal operations.

During a crisis, they become strategic assets.

---

## 3. Supplier relationships are more than price negotiations

A strong supplier relationship can provide:

- Better capacity access
- Faster recovery
- Greater flexibility
- Better communication
- Shared contingency planning

---

## 4. Good leadership means prioritization

During a crisis, resources are limited.

Leaders need to determine:

**What matters most right now?**

That means considering:

- Customer impact
- Financial impact
- Operational risk
- Strategic importance
- Recovery time

---

## 5. AI should improve decisions

The simulation reinforced an important AI lesson:

**Technology is not the strategy.**

AI becomes valuable when it improves an important business decision.

Examples include:

- Predicting demand
- Identifying supplier risk
- Optimizing inventory
- Improving warehouse operations
- Supporting procurement

---

# Biggest Takeaway

The biggest lesson I learned is that supply chain resilience is not about predicting every possible crisis.

It is about building a network that can **adapt quickly when something unexpected happens.**

Visibility, supplier diversity, inventory strategy, flexible operations and good decision-making all work together.

---

# Technology Used

- React
- Babel JSX
- HTML5
- CSS3
- JavaScript
- React useState
- Responsive UI
- Randomized simulation logic
- Interactive decision engine
- Animated progress indicators

---

# Project Structure

```text
operation-lifeline/
│
├── operation-lifeline.html
├── README.md
│
└── screenshots/
    ├── welcome-screen.png
    ├── company-setup.png
    ├── crisis-event.png
    ├── war-room.png
    ├── war-room-results.png
    ├── supplier-negotiation.png
    ├── ceo-boardroom.png
    ├── ai-strategy.png
    └── executive-dashboard.png
