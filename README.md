# Work Location & Vehicle Tracker

A single-page app to log work-from-home vs office time and work vehicle trips, for EOFY tax records.

## Features

- Clock in/out for Home or Office, with a live elapsed timer while active.
- Manual backfill for a past day you forgot to clock.
- Edit any past entry — tap it in the list to load it into the form, change it, and save.
- Recent entries show the 5 most recent by default; "Show all entries" expands the full list so you can find and edit any day of the year.
- Vehicle trip log: date, origin, destination, purpose, start/end odometer — km calculated automatically. The trip list shows the odometer range for each trip.
- Validation blocks duplicate/overlapping entries: an overlapping time range on the same day, or an overlapping odometer range on the same date, is rejected with a message telling you to edit the existing entry instead.
- Financial year report: total home/office hours, home/office days, and vehicle km. Selectable for the current Australian financial year (1 Jul–30 Jun) and the next 5 years ahead.
- PDF export of the full report (day-by-day and trip-by-trip) for the selected financial year, via the browser's print dialog.
- Data backup: download all entries as a `.json` file, and restore/merge them on another device.
- Auto-save to a local file, on browsers that support it (see below).

## Host it on GitHub Pages (free, takes ~5 minutes)

1. Create a new repository on GitHub (e.g. `work-tracker`), public or private — Pages works either way on a paid GitHub plan; on the free plan the repo must be public.
2. Upload `index.html` from this folder to the repository (via the GitHub web UI: Add file > Upload files).
3. Go to the repo's Settings > Pages.
4. Under "Build and deployment", set Source to "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
5. GitHub gives you a URL like `https://yourusername.github.io/work-tracker/`. Open that on your phone and your computer — both work independently.
6. On your phone, open the link in your browser and use "Add to Home Screen" (Safari: Share > Add to Home Screen; Chrome: menu > Add to Home screen) so it behaves like an app icon.

## Auto-save to file

On **desktop Chrome, Edge, or Opera**, the "Enable auto-save to file" button lets you pick a `.json` file once — the app then writes every change to that file automatically, so your data survives a cleared browser cache without you having to remember to back up.

This relies on a browser feature (the File System Access API) that is **not supported on Safari, Firefox, or any mobile browser (iOS or Android)** as of 2026. On those browsers the button is disabled, and the app reminds you to use the manual **Download data backup** button instead.

Practically: on your phone, use manual backup/restore as described below. On a desktop Chrome or Edge browser, turn on auto-save once and it keeps itself current from then on.

## Important: data does not sync automatically

This app stores your entries in the browser's local storage on each device — there is no server or account behind it. That means:

- Entries you log on your phone stay on your phone's browser.
- Entries you log on your computer stay on that computer's browser.
- Clearing your browser data/cache will erase entries.

To move data between devices, use the **Download data backup (.json)** button on one device, then **Restore data from backup** on the other. Do this periodically (e.g. weekly, or before EOFY) to keep both in sync.
