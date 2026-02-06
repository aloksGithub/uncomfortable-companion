---
name: weekly-review
description: Conducts a weekly review of diary entries and goal progress, then produces a weekly report with a planning guide for the coming week.
---

# Weekly Review Protocol

## When to Run
Run this at the end of the week (ideally Sunday evening or Monday morning) to reflect on the past week and set direction for the next one.

## Context Loading
Read the following:
1.  `user_profile.md` (patterns, triggers, strengths)
2.  All `diary/*.md` entries from the past 7 days
3.  All active `goals/*.md` and `tasks/*.md`
4.  The most recent 2-3 files in `weekly_reports/` (to track week-over-week trends)

## The Analysis

### 1. Week in Review
Go through each diary entry for the past 7 days and extract:
-   **Frog Completion Rate:** How many days did the user actually do the planned Frog? (X/7)
-   **Plan Adherence:** How often did reality match the plan? Note days where the plan was ignored or derailed.
-   **Key Wins:** Concrete accomplishments (shipped work, milestones hit, habits maintained).
-   **Key Struggles:** Recurring blockers, avoidance patterns that showed up multiple times, energy crashes.
-   **Pattern Detection:** Look for repeating triggers across diary entries. Did the same avoidance pattern fire on multiple days? Did a specific time of day consistently fail?

### 2. Goal Progress Audit
For each active goal:
-   What milestones were completed this week?
-   What milestones were *supposed* to progress but didn't?
-   Is the goal moving, stalled, or regressing?
-   **Honest Assessment:** Is there a legitimate blocker, or is this avoidance dressed up as "waiting"?

### 3. Task Checkpoint
-   Any tasks completed this week? Archive or mark done.
-   Any tasks overdue? Flag them.
-   Any new tasks that emerged from the week's work?

### 4. Coming Week Planning Guide
Based on the analysis above, produce guidance for daily planning:
-   **Weekly Frog:** The single most important goal milestone to push forward this week. This is the thing that, if done, makes the week a success regardless of everything else.
-   **Goal Priorities:** Rank the active goals by urgency/neglect for the coming week (which ones need attention, which ones can coast).
-   **Suggested Daily Frogs:** For each day of the coming week, suggest what the Frog should be. These are suggestions, not rigid assignments — the daily `/plan` skill will make the final call, but should use these as input.
-   **Watch List:** Specific avoidance patterns or triggers to watch for based on what happened last week.
-   **Capacity Note:** Based on last week's energy patterns, any adjustments needed? (e.g., "You crashed every Thursday — plan lighter that day")

## The Conversation
This is NOT a silent report. Engage the user:
1.  **Open:** "Let's do a weekly review. Looking at your diary entries from this past week..."
2.  **Highlight the honest truth:** Call out the gap between intentions and actions if it exists.
3.  **Ask:** "What felt like the biggest win this week?" and "What are you most avoiding going into next week?"
4.  **Discuss** the coming week's priorities before finalizing the report.

## The Output
After the conversation, save the report to `weekly_reports/YYYY-MM-DD.md` (using the date of the review).

### Report Template
```markdown
# Weekly Review: [Start Date] to [End Date]

## 📊 Week Summary
- **Frog Completion Rate:** X/Y days
- **Plan Adherence:** [Brief assessment]
- **Overall Trajectory:** [Moving forward / Plateauing / Slipping]

## 🏆 Wins
- [Win 1]
- [Win 2]

## 🚧 Struggles & Patterns
- [Struggle/pattern 1]
- [Struggle/pattern 2]

## 🎯 Goal Progress
| Goal | Status | This Week | Notes |
|------|--------|-----------|-------|
| [Goal 1] | [Moving/Stalled/Blocked] | [What happened] | [Honest assessment] |

## 📋 Coming Week: Planning Guide

### Weekly Frog
[The single most important thing to push forward this week]

### Goal Priorities (Ranked)
1. [Goal] - [Why it needs attention]
2. [Goal] - [Why]

### Suggested Daily Frogs
- **Monday:** [Suggestion]
- **Tuesday:** [Suggestion]
- **Wednesday:** [Suggestion]
- **Thursday:** [Suggestion]
- **Friday:** [Suggestion]
- **Weekend:** [Suggestion]

### ⚠️ Watch List
- [Pattern to watch for]
- [Trigger to manage]

### 🔋 Capacity Notes
[Any energy/scheduling adjustments based on last week]
```

## After the Report
-   If `user_profile.md` needs updating based on new weekly patterns, update it.
-   If any goal progress logs need entries, update them.
