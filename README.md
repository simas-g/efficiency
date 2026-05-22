# Efficiency

A personalized productivity dashboard — track goals, tasks, calendar, notes, charts, and projects, all in one dark-themed single-page app.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
  - [Dashboard](#dashboard)
  - [Goals (OKRs)](#goals-okrs)
  - [Tasks](#tasks)
  - [Calendar](#calendar)
  - [Notes (Markdown)](#notes-markdown)
  - [Progress Chart](#progress-chart)
  - [Projects](#projects)
- [Tech Stack](#tech-stack)
- [How to Use](#how-to-use)
  - [Getting Started](#getting-started)
  - [Navigation](#navigation)
  - [Data Management](#data-management)
- [Screenshots](#screenshots)
- [License](#license)

---

## Overview

**Efficiency** is a zero-dependency, single-file productivity dashboard that runs entirely in the browser. It consolidates the core tools you need to stay organized — OKR-style goal tracking, a task list with priorities, a calendar, a markdown note editor, progress charts, and project management — into one clean, dark-themed interface.

No accounts, no servers, no frameworks. Just open `dashboard.html` and everything works. All data is persisted locally using `localStorage`.

---

## Features

### Dashboard

The landing view provides an at-a-glance summary of your entire workspace:

- **Smart greeting** — "Good Morning," "Good Afternoon," or "Good Evening" based on the time of day.
- **Stat cards** — Live counts of active goals, today's pending tasks, upcoming events, and active projects.
- **Goal card** — OKR objectives with key result progress bars.
- **Task card** — Today vs. week toggle, priority indicators, inline task creation with priority selection.
- **Mini calendar** — Month grid with event dots, click to view events for a day.
- **Progress chart** — Dual canvas chart (bar + line) showing task completions and goal progress over 7 days.
- **Notes card** — Three most recent notes with previews, markdown rendering, and relative timestamps.
- **Projects card** — Active projects with progress bars, status badges, and task counts.

### Goals (OKRs)

Full Objectives and Key Results management:

- Create and delete objectives with color coding (indigo, green, amber, pink, blue).
- Add multiple key results per objective, each with a progress percentage (0–100%).
- Update individual key result progress via prompt.
- Average objective progress calculated and displayed automatically.

### Tasks

A focused to-do system:

- Two views: **Today** (shows only tasks due today) and **Week** (all tasks).
- Three priority levels: high (red), medium (amber), low (green) — shown as glowing dots.
- Toggle tasks done/undone with one click.
- Inline task creation with priority dropdown; press Enter to add.
- Sidebar badge shows a live count of pending today tasks.
- Delete tasks with confirmation.

### Calendar

A lightweight event tracker:

- **Mini calendar** on the dashboard and a **full month calendar** in the Calendar view.
- Month navigation (previous/next arrows).
- Event dots on days; days with multiple events get a highlighted accent ring.
- Click a day to filter and view its events in a sorted list.
- Add events via prompt (date auto-populates to the selected day).
- Events store date, title, optional time, and color.

### Notes (Markdown)

A built-in markdown editor and previewer:

- Modal-based editor with title and content fields.
- **Edit / Preview toggle** — write markdown in one mode, see rendered HTML in the other.
- Supported syntax: headings (`#`–`######`), bold (`**text**`), italic (`*text*`), inline code (`` `code` ``), blockquotes (`>`), unordered lists (`-`), ordered lists (`1.`), and links (`[text](url)`).
- Relative timestamps on note cards ("just now", "5m ago", "2h ago").
- Click outside the modal or press `Escape` to close.
- Preview snippets truncated to 80 characters on cards, 150 in the notes browser.

### Progress Chart

A hand-drawn `<canvas>` chart with no external charting libraries:

- **Bar chart** — tasks completed per day over the past 7 days, with value labels.
- **Line chart** — average goal progress trend over 7 days, with data-point markers.
- High-DPI (Retina) aware via `devicePixelRatio` scaling.
- Responsive — automatically redraws on window resize.
- Dark-themed grid lines and axis labels.

### Projects

Track work across multiple projects:

- Status badges: **Active** (indigo), **Review** (amber), **Done** (green).
- Progress bars with percentage and task-completion counts (e.g., "8/12 tasks").
- Four inline actions via prompt: update progress %, change status, set task counts, or delete.
- Progress auto-calculated when task counts are updated.

---

## Tech Stack

| Layer      | Technology    |
| ---------- | ------------- |
| Structure  | HTML5         |
| Styling    | CSS3 (custom properties, flexbox, grid) |
| Logic      | Vanilla JavaScript (ES6+) |
| Storage    | `localStorage` (single JSON key) |
| Charting   | Native `<canvas>` API |
| Markdown   | Custom regex-based parser |
| Fonts      | System font stack (`Inter`, `-apple-system`, `BlinkMacSystemFont`, `Segoe UI`) |
| Dependencies | **None** |

The entire application is a **single file** — `dashboard.html`. No `node_modules`, no build step, no framework, no CDN imports.

---

## How to Use

### Getting Started

1. Clone or download this repository.
2. Open `dashboard.html` in any modern web browser.
3. The application loads with sample data pre-populated. Start exploring or replace it with your own.

### Navigation

| Button | View |
| ------ | ---- |
| ◉ Dashboard | Overview with all card widgets |
| ◎ Goals | OKR objectives and key results |
| ☰ Tasks | Full task list with today/week toggle |
| ▦ Calendar | Full month calendar and event list |
| ✎ Notes | Notes browser with markdown previews |
| ◫ Projects | All projects with status and progress |

Use the **"Reset Sample Data"** button in the sidebar footer to restore the demo data at any time.

### Data Management

- All data is stored automatically in `localStorage` under the key `prime_dashboard_data`.
- No sign-up, no cloud sync — your data stays in your browser.
- To back up: open DevTools → Application → Local Storage → copy the value of `prime_dashboard_data`.
- To clear: click "Reset Sample Data" or clear the localStorage key manually via DevTools.

---

## Screenshots

> **Screenshots coming soon**
>
> *Placeholder for: Dashboard overview, Goals view, Tasks view, Calendar view, Notes editor modal, Projects view, and the progress chart.*

```
+---------------------------------------------------------------+
|                                                               |
|                   [ Dashboard Screenshot ]                    |
|                                                               |
|   Dark-themed single-page with stat cards, goal progress      |
|   bars, task list, mini calendar, chart, notes, and projects  |
|                                                               |
+---------------------------------------------------------------+
```

---

## License

MIT ©

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
