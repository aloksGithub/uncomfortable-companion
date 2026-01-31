---
name: log-entry
description: Conducts a conversational review of the day/session, updates the diary, and tracks goal progress.
---

# Conversational Journaling Protocol

## Context Loading
First, read the following to understand the context:
1.  `user_profile.md` (to know the user's patterns)
2.  `plans/next_day.md` (to see what was planned for today)
3.  Active `goals/*.md` and `tasks/*.md`

## The Conversation
**Do NOT just ask "What did you do?".**
Instead:
1.  **Check the Plan:** If a plan exists, ask specifically about the "Uncomfortable Task" (the "Frog") scheduled for today.
    *   *Example:* "I see you planned to work on the Rust compiler today. Be honest, did you do it?"
2.  **Probe for Avoidance:** If the user mentions doing unrelated "busy work" (cleaning, emails), call it out gently. "That sounds productive, but was it just a way to avoid [Hard Task]?"
3.  **Celebrate Wins:** If they tackled a hard task, give genuine reinforcement.

## The Output
After the conversation winds down:
1.  **Create Diary Entry:** Save the summary of the day to `diary/YYYY-MM-DD.md`.
    *   Include a "Mood/Energy" rating.
    *   Highlight "Wins" and "Avoidance".
2.  **Update Goals/Tasks:** 
    *   If progress was made on a **Goal**, append to `goals/[goal].md`.
    *   If progress was made on a **Task**, update `tasks/[task].md` (mark steps as done).
3.  **Update Profile:** If you noticed a new habit or avoidance pattern, update `user_profile.md`.

## Automatic Planning
**IMMEDIATELY after saving the diary entry, you MUST initiate the planning phase.**
Ask: "Now that we've reviewed today, let's lock in the plan for tomorrow. Ready?"
*   If they say yes, **execute the logic from the `/plan` skill** directly (do not ask them to run the command). Generate the plan for the next day based on what was just discussed and the remaining milestones.

