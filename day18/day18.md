# Brain Dump Action Planner

Transform messy notes, meeting transcripts, voice memos, brainstorming sessions, and stream-of-consciousness thoughts into structured, actionable information.

## Purpose

This skill organizes unstructured information into:

- Summary
- Key Takeaways
- Action Items
- Open Questions
- Risks / Blockers
- Conflicts
- Additional Notes
- Source Information when using Merge Mode

## Core Rules

- Preserve names exactly as provided.
- Preserve dates exactly as provided.
- Preserve numbers exactly as provided.
- Preserve terminology exactly as provided.
- Never invent missing information.
- Never assume ownership.
- Never predict deadlines.
- Never resolve conflicts automatically.
- Use `Not specified` when information is missing.

## Required Status Badges

| Badge | Meaning |
|---|---|
| 🔴 High Priority | Important or urgent item |
| 🟠 Medium Priority | Moderate priority |
| 🟢 Low Priority | Lower priority |
| ⚠️ Conflict | Conflicting information |
| ❓ Open Question | Unresolved question |
| ✅ Completed | Completed item |
| ⏳ Pending | Pending item |

## Full Breakdown Output

### 1. Summary

Provide a short overview of the supplied notes or brain dump.

### 2. Key Takeaways

Highlight the most important information in a structured format.

### 3. Action Items

| Task | Owner | Deadline | Status |
|---|---|---|---|
| Not specified | Not specified | Not specified | ⏳ Pending |

### 4. Open Questions

List unresolved topics, missing decisions, and questions requiring clarification.

### 5. Risks / Blockers

Identify only risks, dependencies, blockers, and concerns explicitly present in the source.

### 6. Conflicts

Identify conflicting:

- Deadlines
- Owners
- Decisions
- Statements
- Other information

Do not automatically resolve conflicts.

### 7. Additional Notes

Include supporting information that does not fit into another section.

## Transcript Mode

Transcript Mode additionally includes:

### Speaker Summary

Summarize each speaker using the exact speaker labels provided.

### Decisions by Speaker

List decisions attributed to each speaker.

### Action Items by Speaker

Group action items according to speaker attribution.

### Attribution Notes

Clearly identify cases where ownership or attribution is unclear.

Never invent speaker identities.

## Merge Mode

Merge multiple notes or sources while preserving the original information.

### Duplicate Items

Identify repeated or duplicate items across sources.

### Conflict Resolution Review

Display conflicting information for manual review.

Never automatically resolve conflicts.

### Source Information

Show which source each piece of information came from.

### Source Note

Preserve source-specific context and terminology.

## Missing Information

When information is unavailable, use:

> Not specified

Do not replace missing information with assumptions, estimates, guesses, or predictions.

## Design Requirements

The final Full Breakdown, Transcript Mode, and Merge Mode output must be a complete interactive HTML artifact.

The artifact should:

- Start with a valid HTML document.
- Be self-contained.
- Be mobile responsive.
- Use a modern dashboard layout.
- Use cards and sections.
- Use tables for structured information.
- Use colored status badges.
- Make action items visually prominent.
- Include visual indicators.
- Use clean typography.
- Use strong visual hierarchy.
- Include hover effects.
- Use soft shadows.
- Use collapsible sections for long notes.
- Feel similar to modern tools such as Notion, ClickUp, Linear, Asana, or Airtable.
- Contain no Markdown in the generated HTML artifact.

## Output Rule

For Full Breakdown, Transcript Mode, and Merge Mode:

**Output only the complete HTML artifact.**

Do not include explanations before or after the HTML.

## Processing Principle

**Source information → Structure → Organize → Highlight → Preserve uncertainty**

The skill must organize the supplied information without changing its meaning or filling gaps.
