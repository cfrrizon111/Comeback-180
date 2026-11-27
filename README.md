# Comeback v10: build your own plans

## New in v10
- **Plans:** create any plan from scratch, with a name, start date and length (1–365 days). Open it from Journey (gear button), from the Plans chip on Today, or from Me > Plans.
- **Missions:** each one has an icon, a colour, an optional time and duration, which weekdays it runs, an optional day range (for example days 1–20 only) and a "catch up if missed" switch.
- **Phases:** name the stages of your plan and the day each one starts.
- **Events:** exams, deadlines, live classes, matches and personal events, either once or every week. They show on Today, in the morning brief (the day before as well), and as red dots on the constellation.
- **Edit a single day:** tap any star, then "Edit this day" to rename or skip missions, add extras or leave a note for that date.
- **Templates:** Blank, Study sprint (30 days) or Portfolio sprint (60 days, from your career roadmap). You can also duplicate an old plan to a new start date.
- **One active plan at a time.** You can switch, pause or delete plans. Ticks are stored by date, so you never lose history.
- Your old 60-day plan became an ordinary editable plan, "60-Day Comeback", with all your ticks intact.
- XP now counts every tick you've ever made, so switching plans never lowers your level.
- The weekly review for Claude now lists your plan's missions and their keys, so the coach plan works with any plan.


A full rebuild of Comeback OS around your 60-Day Comeback.

## What's new
- **Today**: the day number, a progress ring, what you should be doing right now, and today's missions as big tap-to-complete cards with chimes, vibration, sparkles and XP. Finish every mission and you get a "Perfect day" celebration.
- **Journey**: your 60 days drawn as a constellation. Every day you show up lights a star, and a perfect day becomes a bright one. Tap any star to see or fix that day. Also shows phases, progress per track, and match nights.
- **Focus** (the gold button): a full-screen timer with pause, background sound and screen-stay-awake. Stop & log saves the session and can tick the matching mission.
- **Tasks**: quick add, due dates, overdue in red, undo.
- **Me**: level and rank, 12 badges, weekly stats, degree credits/CGPA, night reviews, study sessions.
- **Night review**: 60 seconds (mood, focus, one win, first thing tomorrow). The next morning, Today shows what you planned to start with.
- **Late nights count**: until 5 AM (you can change this in Settings), ticks still count for the previous day.

## New in v9.1: Coach
- **Coach tab**: (1) Copy weekly review: your last 7 days, missed items, backlog and next week's plan, plus instructions for Claude. (2) Paste Claude's reply: the app finds the plan, shows every change, and applies it only after you tap Apply. Coach plans can rename, skip or add missions on any date, including after 7 January (Chapter 2).
- **Catch up**: Krish and Sherlock classes you missed in the last 14 days stay visible until you do them or let them go. Ticking one brightens that day's star.
- **Minimum day**: after two quiet days, Today asks for just one 25-minute session, one mission and a night review.
- **Morning brief**: how yesterday went, what to start with, match nights, phase changes and the weekly review nudge.
- **Decoration**: moon phase, shooting stars, a sky that changes colour through the day, track-coloured mission cards and a daily line at the bottom of Today.
- Tasks moved under Today ("All tasks") and Me.

## Your data
Same database (`comeback` / `kv`) and data format (9). Every 60-day tick, study session, task, review, grade and setting carries over. Projects, skills, applications, courses, flashcards, goals and reminders are no longer shown, but they're still stored and included in every backup.

## Deploy (GitHub Pages, repo `comeback`)
1. In the current app, go to Settings > Export JSON backup.
2. Upload every file in this folder to the repo root, replacing the old ones. You can delete the old `README`/`CHANGELOG`/`TECHNICAL-AUDIT` files.
3. Open the site in Chrome and reload twice. Settings should say "Comeback v9".
4. If you installed it as an app, close and reopen it. To get the new star icon on your home screen, remove the app and install it again. This does not delete your data.

## Roll back
Re-upload the V8.2 files. Your data stays because v9 only adds settings fields (`roll`, `sfx`, `hap`, `bseen`, `px`, `letgo`, `wr`).
