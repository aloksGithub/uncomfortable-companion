---
name: report
description: Generates a progress report for a specific goal or the system overall.
---

# Progress Reporting Protocol

## Usage
*   `report` -> Overall summary.
*   `report "Goal Name"` -> Specific deep dive.

## Overall Report Logic
1.  Read all `goals/*.md` and recent `diary/*.md` entries.
2.  **Trajectory Check:** Are goals moving forward? Or are they stagnant?
3.  **Honesty Audit:** Check diary entries to see if the user is following what is planned on each day. Is the user planning A but doing B?
4.  **Output:** Display a summary to the console (no file creation needed unless requested).

## Specific Goal Report Logic
1.  Read the specific `goals/[goal].md`.
2.  Summarize all entries in the "Progress Log".
3.  Calculate time since last significant progress.
4.  **Output:** Display summary.
