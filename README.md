# Life Dashboard

Static dashboard app for tracking finances, mood, roof log, goals, skills, books, journal, and reflection.

## Google Maps Timeline visualizer

The dashboard now includes a **Maps** tab where you can upload a Google Maps Timeline export in JSON format and:

- map trips and route points,
- review estimated distance traveled,
- inspect top visited places, and
- filter/sort trips directly in the browser.

Timeline files are parsed locally in your browser and can also be included in the app's export/import backup flow.

## Open it locally

### On your computer
1. Open `life-path-dashboard.html` in your browser, or run a local server in this folder:
   ```bash
   python3 -m http.server 8000
   ```
2. Visit `http://localhost:8000/`.

### On your Android phone from your computer
1. Start the local server:
   ```bash
   python3 -m http.server 8000
   ```
2. Make sure your computer and phone are on the same Wi‑Fi.
3. Find your computer's local IP address.
4. On your phone, open `http://YOUR-IP:8000/` in Chrome.
5. In Chrome, tap the menu and choose **Add to Home screen** or **Install app**.

## Publish with GitHub Pages

This repo now includes a GitHub Pages workflow at `.github/workflows/deploy-pages.yml` and a root `index.html` entry point so the dashboard opens directly from the site root.

### Step by step
1. Push this repository to GitHub.
2. Make sure your default branch is named `main`.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **GitHub Actions**.
5. Push a new commit to `main`, or run the **Deploy static site to Pages** workflow manually from the **Actions** tab.
6. Wait for the workflow to finish.
7. Open your site at:
   ```text
   https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPOSITORY-NAME/
   ```
8. On Android, open that URL in Chrome.
9. Tap the menu and choose **Add to Home screen** or **Install app**.

## Files that matter for Pages/PWA
- `index.html` redirects the site root to the dashboard page.
- `life-path-dashboard.html` is the main app.
- `manifest.webmanifest` enables installable app behavior.
- `sw.js` handles offline caching.
