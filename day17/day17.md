Day17
# Vehicle Fuel & Cost Analytics Dashboard

## Objective

Build an interactive, responsive HTML dashboard that analyzes vehicle fuel performance, operating cost, emissions, maintenance, refueling/recharging time, vehicle age, and E85 economics.

The dashboard must use **only the data provided in the attached CSV**.

## Vehicle Details

| Field | Value |
|---|---|
| Vehicle | `[YOUR VEHICLE MODEL]` |
| Fuel | `[Petrol/Diesel/CNG/E85/EV]` |
| Usage | `[City/Highway/Mixed/Fleet]` |
| KM/month | `[e.g. 1000]` |
| Car Age | `[e.g. 3 yrs]` |

## Role

**Data Analyst**

Read the attached CSV, calculate all required metrics, and generate **one self-contained HTML dashboard**.

### Output Requirements

- HTML only
- No explanatory text outside the HTML
- No external CDN
- Pure SVG charts
- CSS embedded inside `<style>`
- JavaScript embedded inside `<script>`
- Responsive from **375px to 1440px**
- Dark navy glassmorphism design
- All numerical values must come from the CSV

---

# Required Calculations

Group analysis by `Fuel_Type`.

### 1. Average Cost/km

```text
Cost/km =
Fuel_Cost_INR ÷ Distance_km
