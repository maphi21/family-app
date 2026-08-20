# Family HQ

A slimmed-down family habit tracker — a single-page web app, used across phone
and iPad, that shows each family member's daily/weekly habits, streaks, and
score at a glance. Free to host (static site, e.g. GitHub Pages), no backend
required.

## Status

Design phase. The `design/` folder holds the current profile-page mockup
(mobile single-profile view with tap-to-switch, and an iPad multi-profile
grid). View it live: https://claude.ai/code/artifact/b5acc9b6-79f6-4a9a-92ff-eff55a152d89

## Design direction

- **Tone**: warm and playful — soft cards, a bright accent color per person,
  pill shapes, bounce animations. Carried over from an earlier build.
- **Profile page** is the app's first screen:
  - Mobile: one profile at a time, switch via swipe or tapping an avatar in
    the picker row.
  - iPad: all profiles shown at once in a grid.
- **Habits** can be daily (a plain checkbox, resets each day) or weekly (a
  target count, e.g. "exercise 3x/week", shown as a progress pill).
- **Streaks are per-habit**, not per-person — each habit tracks its own
  consecutive days (daily) or weeks-hitting-target (weekly) streak.
- **Score** is shown as a progress ring (today's daily habits completed),
  a family leaderboard rank badge (`#1`–`#5`), and a fun escalating level
  title (e.g. "Chore cadet", "Household hero") with a progress bar to the
  next level — carried over from the original build's point-level system.

## What's deliberately left out (for now)

The earlier prototype also had a household jobs table, a rewards shop with
a piggy-bank ledger, birthday/calendar sync, a shared to-do list, an activity
log, an admin PIN, and a kiosk mode. None of that is in this rebuild yet —
the redesign starts from the profile page only, and features get added back
deliberately rather than carried over by default.

## Repo layout

```
design/      <- current design mockup source (Design Components format,
                 viewable live at the artifact link above)
reference/   <- the earlier single-file prototype this rebuild starts from
```

The production app (a single `index.html`, vanilla JS, localStorage-backed)
will land at the repo root once the design settles.
