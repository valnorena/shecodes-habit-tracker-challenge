# SPROUT — 8-Bit Daily Habit Tracker

**SPROUT** is a responsive, single-file habit tracker web app built with vanilla HTML, CSS, and JavaScript for the [SheCodes "Build a Habit Tracker" challenge](https://www.shecodes.io/contests/build-a-habit-tracker/instructions). Styled with a Botanical Sage + 8-bit aesthetic, it helps you build daily routines, track streaks, navigate week by week, and review monthly analytics right in your browser.

---

## Features

- **Habit Management**:
  - Add habits with a name, category tag (`Health`, `Mind`, `Craft`, `Wellness`, `Other`), and an 8-bit pixel SVG icon picker (8 custom icons).
  - Edit existing habits in an accessible modal dialog, filter the list by category, and remove habits with a 5-second **Undo** toast.
  - Pre-loads 3 starter habits (`Drink water`, `Read 20 minutes`, `Code for 1 hour`) on first visit.
- **Daily Progress & Streaks**:
  - Custom 24-block pixel-segmented daily progress ring showing live completion percentage, `done / total`, and `TOP STREAK`.
  - Automatic current and all-time best streak calculation per habit using timezone-safe local `YYYY-MM-DD` date keys.
  - Subtle 8-bit pixel confetti and celebration banner when completing 100% of active habits for the day (respects `prefers-reduced-motion`).
- **Week-to-Week Navigation (Mon–Sun)**:
  - `< PREV`, `THIS WEEK`, and `NEXT >` controls sync both the 7-day segmented bar chart and every habit card's interactive 7-day check-in strip.
  - Upcoming days are disabled and excluded from weekly averages; bars always scale against active habits.
- **Monthly Report & Analytics**:
  - Dedicated **Monthly Report** tab with `< PREV`, `THIS MONTH`, and `NEXT >` switching plus a **PRINT / PDF** button with print-optimized styling.
  - **4 Summary KPIs**: Completion Rate, Total Check-ins (with Perfect Days count), Best Habit, and Garden Changes (`+ADDED`, `~EDITED`, `-ERASED`).
  - **8-Bit Monthly Calendar Heatmap**: Mon–Sun grid with 5 completion-intensity tiers and per-day tooltips.
  - **Per-Habit Breakdown & Activity Changelog**: Segmented progress meters, monthly best streaks, and a filterable log (`ALL`, `ADDED`, `EDITED`, `ERASED`) of habit lifecycle events.
- **Light & Dark Botanical Sage Themes**:
  - Toggle between **Sunlit Botanical Parchment** (Light) and **Moonlit Greenhouse** (Dark), saved automatically in `localStorage`.
- **Persistence & Reliability**:
  - Stores habits (`sprout_habits_v1`), lifecycle events (`sprout_events_v1`), and theme (`sprout_theme_v1`) in browser `localStorage` with `try/catch` storage guards and date/data validation.
- **Accessibility & Performance**:
  - WCAG 2.1 AA color contrast across both themes, skip link, `<main>` landmark, keyboard tablist navigation (`ArrowLeft`/`ArrowRight`/`Home`/`End`), modal focus trap & restoration, and live screen-reader announcements (`#sr-announcer`).
  - Zero external JS dependencies, zero raster images, shared SVG `<symbol>` sprite, and non-blocking Google Fonts (`Press Start 2P`, `Silkscreen`, `Space Mono`).

---

## Project Structure

```text
shecodes-habit-tracker-challenge/
├── index.html   # Self-contained app (HTML, inline CSS, inline JavaScript)
└── README.md    # Project overview and documentation
```

---

## Quick Start

No build step or server is required:

1. Clone the repository:
   ```bash
   git clone https://github.com/valnorena/shecodes-habit-tracker-challenge.git
   ```
2. Open `index.html` directly in any modern browser.

---

## Credits

- **Coded by**: [Valentina Noreña](https://github.com/valnorena)
- **Challenge**: [SheCodes](https://www.shecodes.io)
