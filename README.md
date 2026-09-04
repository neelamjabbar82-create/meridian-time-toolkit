# Meridian — All-in-One Time Toolkit

A single website that replaces five separate apps: a live world clock, a customizable focus timer, an interval trainer for workouts, a meeting-time overlap finder, and alarms. No login, no backend, no cost — everything runs in your browser and saves itself for next time.


---

## Why this exists

I kept solving the same small problems manually — restarting a workout timer by hand every round, googling "what time is it in Dubai," guessing whether a client in another timezone was even awake. Meridian is what happens when you get tired of doing that manually and build the automation instead.

## Features

### 🕰️ Clock Studio
Three instrument-grade clock faces — a hybrid analog/digital display, a hand-built CSS seven-segment digital clock (not a font), and a classic roman-numeral analog face. Switch styles, pick an accent color, toggle 12h/24h.

### 🌍 World Clock
Pick a country, then a city, and add it to your board. Live-updating time, date, and UTC offset for every city you track — built for anyone juggling clients, teams, or family across time zones.

### 🎯 Focus Timer
A pomodoro-style timer with fully custom focus and break lengths (set it in minutes and seconds — not locked to 25/5). Every completed session is logged automatically, so focus becomes something you can actually see over time.

### 💪 Interval Timer
Work/rest rounds that cycle themselves — set a duration, a rest length, and a number of rounds (or go endless), hit start, and put your phone down. Includes Tabata, HIIT, and beginner presets. Built for workouts and drills where you don't want to touch a screen mid-set.

### 🤝 Meeting Finder
Pick two cities and instantly see a 24-hour grid highlighting where both sides' working hours (9 AM–6 PM) overlap, plus a plain-language "best time to meet" summary.

### ⏰ Alarms
Simple, reliable alarms with custom labels — set them and they ring, with an in-page overlay and an audio alert (no external sound files, generated with the Web Audio API).

---

## Tech Stack

- **HTML5** — semantic structure, hash-based client-side routing
- **CSS3** — custom design tokens, no framework, fully responsive
- **Vanilla JavaScript** — no build step, no dependencies
- **Intl.DateTimeFormat** — real timezone-aware time calculations
- **Web Audio API** — generated alarm/timer beep sounds (no audio files)
- **Google Fonts** — Instrument Serif, Inter, JetBrains Mono
- **Font Awesome** — icons

## Data & Privacy

Everything you add — world clock cities, alarms, focus history, timer durations, and your accent color — is saved directly in your browser (no account, no server, no tracking). Clear your browser storage and it resets to defaults.

## Getting Started

This is a single self-contained HTML file — no build tools, no npm install.

```bash
git clone https://github.com/your-username/meridian.git
cd meridian
open index.html   # or just double-click the file
```

To deploy it yourself, drop `index.html` into any static host — GitHub Pages, Netlify, Vercel, or a plain web server all work with zero configuration.

## Design Notes

- Every clock, timer, and grid runs on your device's real clock — nothing is simulated.
- The seven-segment digital display is built entirely in CSS, segment by segment, rather than using a monospace/digital font — so it looks identical everywhere and scales cleanly.
- Meeting Finder's timezone math assumes whole-hour offsets for simplicity; half-hour timezones (like India) are approximated.

## Roadmap

-  MERN backend for cross-device sync (accounts, MongoDB-backed alarms/history)
-  Push notifications for alarms and timers when the tab isn't open
-  Half-hour/quarter-hour timezone precision in the Meeting Finder
-  Shareable/exportable custom clock themes

## Credits

Designed and built by **Neelam Jabbar**.

---

*Found a bug or have a feature idea? Open an issue or reach out — this project started from solving my own problems, and I'm happy to hear about yours too.*
If you really like it give it a star 
