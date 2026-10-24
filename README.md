# Kanso

A habit tracker for phone and laptop: streak goals, weekly and monthly analytics, timer habits, streak freezes, weekly review, dark and light mode. Installable as an app (PWA).

## Deploy
1. Create a GitHub repo and upload these files to the root.
2. On vercel.com choose **Add New > Project**, import the repo, keep all defaults (no build step), and press **Deploy**.

No Supabase or other service is needed for this version. It is a static site.

## How data works
Accounts and habits are saved in the browser (localStorage) on each device. Passwords are hashed, but there is no server, so data does not sync between devices. Use **Settings > Export file / Import file** to move data.

## Adding real sync later
For accounts that work across devices, add a backend such as Supabase (Auth + a table of habit rows). Replace the `auth()` and `save()` functions in `index.html`.

## Manual test checklist
Create account, add a habit, open the Month tab and tick days, log mood and sleep, check it off, add a timer habit and finish it, open Analytics (Weekly, Monthly, Streak goals), open Review and save a note, switch theme, sign out and back in.
