Day 52 — System Design
SmartSave
AB Talks 60-Day Claude AI Challenge

---

 1. Project Overview

SmartSave is a personal savings-goal planner that helps users create savings goals, calculate the required saving amount, track progress, and understand whether they are on track.

The system is designed to be simple, free, and suitable for a 10-day capstone.

---

 2. System Architecture

```text
┌─────────────────────┐
│        User         │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│    SmartSave UI     │
│ Dashboard + Forms   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────────────┐
│     Application Logic       │
│                             │
│ • Goal Management           │
│ • Savings Calculations      │
│ • Progress Tracking         │
│ • Status Evaluation         │
│ • Saving Suggestions        │
└─────────────┬───────────────┘
              │
              ▼
┌─────────────────────┐
│    Local Storage    │
│     Goal Data       │
└─────────────────────┘
