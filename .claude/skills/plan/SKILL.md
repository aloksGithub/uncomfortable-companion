---
name: plan
description: Generates a plan for the next day, prioritizing uncomfortable tasks based on goal milestones.
---

# Smart Planning Protocol (Next Day)

## Input
Read:
1.  `user_profile.md` (specifically "Avoidance Patterns")
2.  All active `goals/*.md` (Focus on next uncompleted Milestones)
3.  All active `tasks/*.md` (Short-term projects)
4.  Recent `diary/` entries (to gauge current momentum)
5.  **The most recent `weekly_reports/*.md`** (if one exists). Use the "Coming Week: Planning Guide" section to inform today's Frog selection and priorities. The weekly report provides strategic direction — respect it unless circumstances have clearly changed since it was written.

## The Logic
1.  **Check Weekly Context:** If a weekly report exists and is recent (within the last 7 days):
    *   Look at the "Suggested Daily Frogs" for tomorrow's day of the week.
    *   Look at the "Goal Priorities" ranking.
    *   Look at the "Watch List" for patterns to guard against.
    *   Use these as strong inputs (not overrides) when selecting the Frog and supporting tasks.
2.  **Identify the Frog:** Look at active `goals` AND `tasks`.
    *   **Intelligent Neglect Check:** Look for goals that are stalling *without* a valid reason.
    *   *Constraint:* Do not force a goal if the user has explicitly stated they are "Blocked" or "Waiting" in recent diary entries.
    *   Is there an urgent `task` with a deadline soon? -> **Priority Frog**.
    *   Else, use the weekly report's suggested Frog if available, or find a stalled `goal` milestone.
3.  **Scheduling Rule:** Create a plan for *tomorrow*.
4.  **Capacity Check:**
    *   1 "Frog" (Major Goal Step or Urgent Task)
    *   2-3 supporting items (from other Tasks or small Goal steps).
    *   If the weekly report has "Capacity Notes" (e.g., lighter day suggested), respect that.

## The Output
2.  **Update Pointer:** Update `next_day_plan.md` with the content of this new plan.

## Plan Template
```markdown
# Plan for [Tomorrow's Date]

## 🎯 The "Frog" (Priority #1)
- [ ] [The Hardest Task from Goal Milestones]
  *Why:* [Reason from goal definition]
  *Weekly Context:* [How this connects to the weekly plan, if applicable]

## 🛠️ Supporting Tasks
- [ ] [Task 2]
- [ ] [Task 3]

## 🧠 Mindset Note
[Specific advice based on user's recent avoidance patterns and weekly watch list]
```
