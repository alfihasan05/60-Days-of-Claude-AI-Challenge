 Day 53 — Project Setup & Foundation

AB Talks 60-Day Claude AI Challenge

**Capstone Project:** SmartSave  
**Capstone Day:** 3 of 10  
**Milestone:** Project Setup & Foundation



1. Working Hello World Screenshot

> **Screenshot required:** Replace the image below with the actual screenshot of the SmartSave application running locally before committing this file.

![SmartSave — Hello World Running Locally](screenshots/day3-hello-world.png)

**Verification:** The application should be visibly running from the local development environment, with the browser address showing the local development URL.

---

# SETUP.md

## Project Overview

SmartSave is a focused savings-goal planner. The v1.0 product is designed around a local-first workflow: a user creates a savings goal, receives a practical saving pace, tracks progress, and understands whether the goal is on track.

## Development Principles

- Free/local tools only
- No paid API required
- Keep the core workflow simple
- Separate data, calculations, and UI
- Avoid unnecessary dependencies
- Preserve previous functionality while extending the project

## Setup Checklist

1. Install the required runtime and development tools defined by the approved system design.
2. Open the project folder in the selected IDE.
3. Install project dependencies, if any.
4. Create the required environment/configuration files.
5. Start the local development server.
6. Open the local URL in a browser.
7. Verify that the Hello World/baseline application loads without blocking errors.
8. Initialize/connect Git and GitHub.
9. Create the Day 3 commit after verification.

## Local Verification

The baseline is considered ready when:

- The application starts successfully.
- The local page loads.
- No blocking console errors are present.
- The project structure matches the approved design.
- The repository is under version control.
- The foundation is ready for the first user-facing feature.

---

# PROJECT-STRUCTURE.md

## Approved Project Direction

SmartSave follows a simple, modular structure so UI, calculation logic, data handling, and configuration can evolve independently.

## Structure

```text
SmartSave/
├── README.md
├── SETUP.md
├── PROJECT-STRUCTURE.md
├── ENVIRONMENT.md
├── DAY3-SUMMARY.md
├── package.json
├── .gitignore
├── .env.example
├── src/
│   ├── components/
│   ├── pages/
│   ├── data/
│   ├── logic/
│   ├── storage/
│   ├── services/
│   └── styles/
├── public/
└── screenshots/
    └── day3-hello-world.png
