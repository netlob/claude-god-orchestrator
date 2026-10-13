---
name: catch-me-up
description: Give the person an overview of where everything stands, what is waiting and what to do next. Use when they say "catch me up", "where was I", "what's the status", "what's going on", "what should I do today", or when they start a session after a break. Includes the weekly plan review and tidy when seven or more days have passed since the last review.
---
# Catch me up

Goal: in two minutes of listening, they know where everything stands, what is waiting, and what to do next. They are listening more than reading, so keep it short: no list longer than five items unless they ask.

1. **Read.** `plan.md`, `me/goals.md`, and the "Where it stands" section of every `projects/*/CLAUDE.md`. Count the items in `inbox/` (ignore `README.md`). Check the Git history for what changed since the last wrap-up.
2. **Report, most important first.**
   - What changed since last time, one line each.
   - Each project: status and next step. Flag anything stale (not updated in fourteen days) or waiting on someone.
   - Inbox: how many items are waiting. Offer to process them.
   - The seven-day tasks in `plan.md`: done, in progress, not started.
   - Suggested focus for today: at most three things.
3. **Weekly review and tidy.** Run this when "Last reviewed" in `plan.md` is seven or more days ago, or when they ask for it.
   - Walk through the 7/30/90 plan with them: what got done, what moves, what drops. Propose the next seven days' three tasks. Update `plan.md` with their answers and set "Last reviewed" to today.
   - Tidy check: statuses that look stale, knowledge notes that contradict each other, files nothing points to, inbox items older than seven days, names in notes that are missing from `me/names.md`. Report what you found. Fix only what they confirm.
4. **Save** with Git if anything changed.
