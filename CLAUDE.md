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
- `favicon.png` — App icon (32x32, used as browser favicon)
- `favicon512.png` — App icon (512x512, used for PWA install)
- `.github/workflows/deploy.yml` — GitHub Actions deployment
- `README.md` — Project readme
- `CLAUDE.md` — Project context for Claude Code

## Key Notes
- **No build step** — edit `index.html` directly
- **PWA** — installable via manifest + service worker; cache-first strategy
- **IMPORTANT: Always bump `CACHE_NAME` in `sw.js` with every commit** to force clients to refresh cached assets
- **Responsive** — three breakpoints: portrait mobile (default), landscape mobile (`orientation:landscape` + `max-height:500px`, side-by-side layout), desktop (`min-width:768px` + `min-height:500px`, enlarged UI)
- **Audio** — uses MP3 files via `new Audio()`, respects mute toggle
- **Presets** — Boxing and Calisthenics; preset buttons exist both at top level and inside settings
