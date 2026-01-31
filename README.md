# Goal Tracker - The "Uncomfortable" Companion

A prompt-based operating system for tracking goals and confronting avoidance behaviors, powered by Claude Code.

## Setup
1.  Ensure you have Claude Code installed.
2.  Open this directory in your terminal.
3.  Run the onboarding command to initialize your profile:
    ```bash
    /onboard
    ```

## How to Use
This system uses **Skills** (Slash Commands). You interact with it by typing commands in the Claude Code interface.

### 1. Define Goals & Tasks
*   **Long-Term:**
    ```bash
    /add-goal
    ```
    For big ambitions (e.g., "Learn a Language", "Get Fit").
*   **Short-Term:**
    ```bash
    /add-task
    ```
    For multi-day projects (e.g., "Write Presentation", "Fix Bug").

### 2. Log & Plan (Daily Loop)
```bash
/log-entry
```
This is your main daily interaction.
1.  **Review:** Talk to Claude about what you did today. It checks your progress.
2.  **Plan:** At the end of the conversation, Claude will automatically generate the plan for **tomorrow**.

### 3. Check Progress
```bash
/report
# OR
/report "Learn Rust"
```

## Directory Structure
- `.claude/skills/`: The "Brain" (Command definitions).
- `goals/`: Your active goals (Milestones defined here).
- `tasks/`: Short-term active projects.
- `diary/`: Your daily logs.
- `plans/`:
    - `next_day.md`: The active plan for tomorrow.
    - `YYYY-MM-DD.md`: Archived plans.
- `user_profile.md`: The system's memory.
