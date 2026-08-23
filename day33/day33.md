# Media Integrity Analyzer

## Day 33 — Media Literacy Through Interactive Discovery

An interactive, offline-first learning application designed to help users recognize misleading headlines, emotional manipulation, audience targeting, and source/context problems.

## Project Overview

The Media Integrity Analyzer turns media literacy into a guided investigation rather than a traditional quiz.

Users observe a fictional media scenario, make an initial judgment, identify suspicious signals, and then reveal the evidence and explanation.

The application was built as a single self-contained HTML file using:

- HTML5
- Vanilla CSS
- Vanilla JavaScript
- No frameworks
- No backend
- No APIs
- No external assets
- Fully functional offline

## Features

### 1. Theme Selection

Users can choose from multiple visual themes:

- Claude Orange
- Ocean Signal
- Violet Focus
- Forest Lens
- Rose Signal

The selected theme is stored locally for a consistent experience.

### 2. Headline Detective

The first challenge teaches users how headlines can exaggerate or remove important context.

The user:

1. Reads a fictional headline.
2. Reads the matching article.
3. Chooses whether they would click it.
4. Identifies potentially misleading wording.
5. Reveals the evidence.
6. Receives an accuracy score.
7. Compares the headline with a fair rewritten version.

Key lesson:

> A compelling headline is not automatically an accurate one.

### 3. Emotion Detector

The second challenge focuses on emotional framing.

The user:

1. Reads a fictional social media post.
2. Identifies their emotional reaction.
3. Finds the words that influenced that reaction.
4. Reveals the intended audience.
5. Identifies the emotional response being targeted.
6. Learns the manipulation technique.
7. Compares the original post with a neutral rewrite.

Key lesson:

> Notice the feeling first. Then investigate the claim.

## Live Media Integrity Metrics

The application continuously tracks:

| Metric | Purpose |
|---|---|
| Headline Accuracy | Measures how closely a headline reflects its supporting article |
| Source Reliability | Encourages thinking about evidence and context |
| Emotional Manipulation | Identifies emotional intensity and persuasive framing |
| Audience Targeting | Highlights who the message is designed to influence |

## Media Integrity Dashboard

After completing both challenges, the application generates a final dashboard containing:

- Overall Media Integrity Score
- What the user learned
- Biggest red flag
- Three practical media literacy habits
- Personal investigation profile
- Replay option with new scenarios

## Key Learnings

### 1. Read beyond the headline

A headline is a compressed version of a story. Important qualifications can disappear when information is simplified for attention.

### 2. Separate correlation from causation

A study can show that two things are associated without proving that one caused the other.

### 3. Watch for absolute language

Words such as "always", "never", "proves", "forever", and dramatic claims deserve additional scrutiny.

### 4. Identify emotional triggers

Fear, anger, excitement, pride, urgency, and fear of missing out can influence how quickly people react.

### 5. Ask who the message is for

Understanding the intended audience can reveal why particular words, emotions, and arguments were selected.

### 6. Pause before sharing

The most useful media literacy habit is creating a small gap between seeing information and reacting to it.

## Screenshots

### Application Home Screen

![Media Integrity Analyzer Home](screenshots/media-integrity-home.png)

### Headline Detective

![Headline Detective Challenge](screenshots/headline-detective.png)

### Emotion Detector

![Emotion Detector Challenge](screenshots/emotion-detector.png)

### Media Integrity Dashboard

![Media Integrity Dashboard](screenshots/media-integrity-dashboard.png)

## Generated Application

The complete application is available in:

`media-integrity-analyzer.html`

It can be opened directly in a browser without installing dependencies or running a server.

## Project Structure

```text
media-integrity-analyzer/
│
├── media-integrity-analyzer.html
├── README.md
└── screenshots/
    ├── media-integrity-home.png
    ├── headline-detective.png
    ├── emotion-detector.png
    └── media-integrity-dashboard.png
