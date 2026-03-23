# Boxing Timer App

## Overview
A single-page PWA boxing/workout interval timer hosted at https://timer.crcibernetica.com.
GitHub repo: https://github.com/CRCibernetica/timerapp

## Architecture
This is a minimal, no-build, single-file web app. All HTML, CSS, and JS live in `index.html`.

## Files
- `index.html` — Entire app (markup, styles, logic)
- `manifest.json` — PWA web app manifest
- `sw.js` — Service worker for offline caching
- `bell.mp3` — Round start/end sound effect
- `warning.mp3` — End-of-round warning sound effect
- `favicon.png` — App icon (32x32)
- `.github/workflows/deploy.yml` — GitHub Actions deployment

## Key Notes
- **No build step** — edit `index.html` directly
- **PWA** — installable via manifest + service worker; cache-first strategy
- **When updating assets**, bump `CACHE_NAME` in `sw.js` to force clients to refresh
- **Responsive** — portrait mobile (default), landscape mobile (side-by-side layout), desktop (enlarged UI)
- **Audio** — uses MP3 files via `new Audio()`, respects mute toggle
- **Presets** — Boxing and Calisthenics; preset buttons exist both at top level and inside settings
