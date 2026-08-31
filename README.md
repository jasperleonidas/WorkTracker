# Work Location & Vehicle Tracker

A single-page app to log work-from-home vs office time and work vehicle trips, for EOFY tax records.

## Host it on GitHub Pages (free, takes ~5 minutes)

1. Create a new repository on GitHub (e.g. `work-tracker`), public or private — Pages works either way on a paid GitHub plan; on the free plan the repo must be public.
2. Upload `index.html` from this folder to the repository (via the GitHub web UI: Add file > Upload files).
3. Go to the repo's Settings > Pages.
4. Under "Build and deployment", set Source to "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
5. GitHub gives you a URL like `https://yourusername.github.io/work-tracker/`. Open that on your phone and your computer — both work independently.
6. On your phone, open the link in your browser and use "Add to Home Screen" (Safari: Share > Add to Home Screen; Chrome: menu > Add to Home screen) so it behaves like an app icon.

## Important: data does not sync automatically

This app stores your entries in the browser's local storage on each device — there is no server or account behind it. That means:

- Entries you log on your phone stay on your phone's browser.
- Entries you log on your computer stay on that computer's browser.
- Clearing your browser data/cache will erase entries.

To move data between devices, use the **Download data backup (.json)** button on one device, then **Restore data from backup** on the other. Do this periodically (e.g. weekly, or before EOFY) to keep both in sync.
