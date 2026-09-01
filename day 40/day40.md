Day 40 — AI Assistant Builder
 BudgetPilot — AI Budget & Expense Coach

A purpose-built AI budgeting assistant for salaried professionals who want to understand their monthly spending, identify unnecessary expenses, and build practical next steps.

Project Overview

BudgetPilot combines AI-powered financial coaching with a focused budgeting dashboard.

Instead of functioning as a generic chatbot, the application converts a user's financial snapshot into:

- Financial health score
- Monthly income overview
- Total expense overview
- Savings rate
- Spending category analysis
- Priority actions
- Key financial insight
- Follow-up AI coaching

 Features

 Budget Analysis

Users can provide:

- Monthly income
- Current savings
- Housing expenses
- EMI/debt payments
- Spending by category
- Additional financial context

The assistant analyzes the information and creates a structured budget overview.

 Financial Health Score

BudgetPilot generates an educational 0–100 budgeting health score using factors such as:

- Savings capacity
- Expense burden
- Fixed-cost pressure
- Debt burden
- Controllable spending

The score is a coaching indicator and is not a scientifically validated financial measurement.

 Spending Profile

The dashboard highlights important spending categories so users can quickly understand where their money is going.

 Priority Actions

The assistant focuses on a small number of high-impact actions instead of overwhelming users with too many recommendations.

Each action includes:

- Action title
- Explanation
- Practical next step

### AI Financial Insight

BudgetPilot identifies the most important spending pattern from the user's financial information and explains why it matters.

### Conversational Coaching

Users can continue the conversation after the initial analysis.

Example questions:

- Where can I reduce spending without affecting my lifestyle?
- Which expense should I focus on first?
- How can I increase my monthly savings?
- Is my current spending balanced?

## Technology

- HTML5
- CSS3
- Vanilla JavaScript
- Claude API
- Fetch API
- Responsive CSS
- No frontend frameworks
- No external UI libraries

## Architecture

```text
User Financial Data
        |
        v
Budget Snapshot
        |
        v
System Prompt
        |
        v
Claude API
        |
        v
Structured JSON Response
        |
        +------------------+
        |                  |
        v                  v
Health Score       Spending Profile
        |
        +------------------+
        |                  |
        v                  v
Priority Actions    Financial Insight
        |
        v
AI Follow-up Coach
