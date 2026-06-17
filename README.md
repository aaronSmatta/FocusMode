# 🌱 Bloom — Focus & Grow (FocusMode)

A gamified focus web app. Run focus sessions with proven techniques, earn XP and coins,
grow and customize a cute sprout avatar, and climb a community leaderboard — all wrapped
in a calm, cozy interface. Installable on iPhone as a Home Screen web app (PWA).

## Features
- **Focus techniques** — Pomodoro (25/5 ×4), 52/17, Deep Work (50/10 ×2), Quick Sprint (15/3), and a Custom timer with full break-cycle handling.
- **Gamification** — earn ~3 XP and ~2 coins per focused minute (plus completion bonuses), level up with celebratory rewards.
- **Avatar + shop** — ~28 cosmetics across body color, background, hat, glasses, and a companion pet. Items are gated by both level and coin cost; buying auto-equips.
- **Community board** — weekly focus leaderboard; you're ranked among sample users by real focused minutes.
- **Ambient soundscapes** — Rain, Forest, Lo-fi pad, Deep Drone, and Ocean, generated live via the Web Audio API (no audio files).
- **Focus Lock** — full-screen breathing mode that detects and counts when you leave the page/switch apps.
- **Offline + installable** — works offline via a service worker and installs to the iPhone Home Screen.

## Files
| File | Purpose |
|------|---------|
| `index.html` | The app (iPhone-tuned PWA) |
| `manifest.webmanifest` | Makes it installable (name, icon, full-screen) |
| `sw.js` | Service worker for offline use |
| `icon-180/192/512.png`, `icon-512-maskable.png` | App icons |
| `bloom-standalone.html` | Single-file version — open directly in a browser, no hosting needed |

## Run it
**Quick (no install):** open `bloom-standalone.html` in any browser.

**As an installed iPhone app:**
1. Host this folder (e.g. enable **GitHub Pages** on this repo, or drag the folder to https://app.netlify.com/drop).
2. Open the resulting `https://…` link in **Safari on your iPhone**.
3. Tap **Share** → **Add to Home Screen** → **Add**.
4. Launch **Bloom** from your Home Screen. 🌱

> A `file://` path runs the app but Safari won't offer "Add to Home Screen" and offline caching is disabled — hosting over https unlocks the full experience.

## Data & privacy
All progress is stored locally in the browser via `localStorage` — nothing is uploaded. The community board uses sample data.

## Known limitation
A web app — even installed — **cannot silence iOS notifications or block other apps**. That requires a native iOS app using Apple's Screen Time framework (FamilyControls / ManagedSettings / DeviceActivity). Bloom's "Focus Lock" is the web-possible version. This PWA is a working blueprint for a future native build.

## Tech
Vanilla HTML/CSS/JS, no build step. SVG avatars, Web Audio soundscapes, PWA manifest + service worker.
