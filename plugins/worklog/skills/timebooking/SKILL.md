---
name: timebooking
description: Prepare and book the user's timesheet from WorkLog (local activity tracking on their Mac) into Jira/Tempo. Use when the user types /timebooking, optionally followed by a day such as "yesterday" or "2026-10-21", or asks to book, log or review their working time.
---

# Time booking with WorkLog

Use the day the user named after /timebooking (e.g. "yesterday", "2026-10-21"); if none, use today.

1. Call the WorkLog tool `get_day_summary` with that date ("today", "yesterday" or YYYY-MM-DD).
2. Follow the `instructions` field of the result exactly. It covers mapping blocks to issues, proposing
   (`propose_timesheet`), booking via the connected time-tracking tool (Tempo) and `mark_booked`, and it
   depends on the user's booking mode and their own instructions in WorkLog.
3. If the WorkLog tools are not available: WorkLog only works in the Claude desktop app on the Mac where the
   WorkLog app runs (claude.ai in a browser can't reach it). In the desktop app's regular chat, the WorkLog
   extension is needed — tell the user to open WorkLog (menu bar) → Settings → Claude → Install. In Cowork, the
   WorkLog app is missing or not in /Applications.
