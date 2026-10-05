# Todo

A simple, offline-capable personal todo app. Vanilla HTML/CSS/JS — no build step, no dependencies.

## Features

- Add, edit, delete, and complete tasks
- Today / Upcoming / Completed views with live counts
- Search across titles, notes, and priorities
- Due dates, priority levels, and notes per task
- Dark mode (persisted)
- Fully responsive with a mobile navigation drawer
- Offline support via service worker
- Installable as a PWA (Add to Home Screen)

## Run Locally

Any static file server works:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

## Install on Mobile

Serve the app over `localhost` or HTTPS (Chrome requires one of the two), open it in Chrome, then use the browser menu → **Add to Home Screen** / **Install app**.

## Project Structure

```
index.html          # App markup
css/style.css       # Styles, design tokens, dark mode, responsive rules
js/app.js           # App logic (state, rendering, events)
service-worker.js   # Offline cache (must stay at root for full-scope control)
manifest.json       # PWA manifest
icons/              # App icons (192px, 512px)
assets/             # Screenshots
```

## Storage

Tasks and theme preference persist in `localStorage` — no backend required.
