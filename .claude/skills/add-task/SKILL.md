---
name: add-task
description: Creates a short-term task (1-7 days) that needs focus but isn't a massive life goal.
---

# Task Definition Protocol

## Purpose
For short-term projects (e.g., "Refactor Auth System", "Write Blog Post", "Plan Vacation") that are too big for a single to-do item but smaller than a Life Goal.

## Process
1.  **Quick Inquiry:** Ask what the task is.
2.  **Deadline Check:** "When does this need to be done by?" (Must be < 2 weeks, ideally < 1 week).
3.  **The "Frog" Check:** "Is this something you are avoiding?" (If yes, mark it as a High Priority Frog).
4.  **Steps:** "What are the 3-5 rough steps to finish this?"

## Output
Create a new file in `tasks/[task_name_slug].md` using this format:

```markdown
# Task: [Title]

## Context
[Brief description]
- **Deadline:** [Date]
- **Status:** Active

## The Steps
- [ ] Step 1
- [ ] Step 2
- [ ] Step 3

## Notes
[Any extra details]
```
