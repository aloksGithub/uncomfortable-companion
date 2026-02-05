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

## The Logic
1.  **Identify the Frog:** Look at active `goals` AND `tasks`.
    *   **Intelligent Neglect Check:** Look for goals that are stalling *without* a valid reason.
    *   *Constraint:* Do not force a goal if the user has explicitly stated they are "Blocked" or "Waiting" in recent diary entries.
    *   Is there an urgent `task` with a deadline soon? -> **Priority Frog**.
    *   Else, find a stalled `goal` milestone.
2.  **Scheduling Rule:** Create a plan for *tomorrow*.
3.  **Capacity Check:** 
    *   1 "Frog" (Major Goal Step or Urgent Task)
    *   2-3 supporting items (from other Tasks or small Goal steps).

## The Output
2.  **Update Pointer:** Update `next_day_plan.md` with the content of this new plan.

## Plan Template
```markdown
# Plan for [Tomorrow's Date]

## 🎯 The "Frog" (Priority #1)
- [ ] [The Hardest Task from Goal Milestones]
  *Why:* [Reason from goal definition]

## 🛠️ Supporting Tasks
- [ ] [Task 2]
- [ ] [Task 3]

## 🧠 Mindset Note
[Specific advice based on user's recent avoidance patterns]
```
