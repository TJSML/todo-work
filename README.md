# To do Work Lite

A lightweight Task & Project Management web app for personal use, organized around the Eisenhower Matrix. Fast, clean, and built to run entirely in your browser — no backend, no database, no login.

## Features

- **Eisenhower Matrix layout** — four quadrants: Important + Urgent, Important + Not Urgent, Not Important + Urgent, Not Important + Not Urgent
- **Groups** — create, rename, delete, collapse/expand, and move between quadrants
- **Automatic Group status & progress** — calculated from tasks (IN PROGRESS / COMPLETE), with a progress bar and percentage
- **Tasks** — create, rename, delete, reorder (move up/down), toggle Not Done / Done, and edit a start/end timeline
- **Instant search** — filters by Group name or Task name as you type
- **Export / Import JSON** — back up and restore all your data as a file
- **Thai / English** — full UI translation with a language switch
- **Light / Dark mode**
- **LocalStorage persistence** — everything saves automatically, no Save button
- **Responsive layout**, desktop-first

## Installation

```bash
npm install
```

## Run (development)

```bash
npm run dev
```

Then open the URL Vite prints (typically `http://localhost:5173`).

## Build (production)

```bash
npm run build
```

Output is generated in the `dist/` folder. Preview it locally with:

```bash
npm run preview
```

## Folder Structure

```
src/
├── components/     # Reusable UI components (Card, GroupCard, TaskRow, Quadrant, Sidebar, SearchBox, SettingsPanel, ConfirmDialog)
├── pages/          # (reserved for future page-level views)
├── hooks/          # useGroups (data + operations), useTheme (light/dark)
├── utils/          # date formatting, id generation, group status/progress, search, LocalStorage, import/export
├── types/          # Task, Group, QuadrantId type definitions
├── assets/         # (reserved for static assets)
├── locales/        # en.json, th.json translation files
├── i18n.ts         # i18next configuration
├── App.tsx         # Application shell
├── main.tsx        # Entry point
└── index.css       # Tailwind + global styles
```

## Tech Stack

React · Vite · TypeScript (strict mode) · Tailwind CSS · i18next · Lucide Icons

## Data & Privacy

All data is stored in your browser's LocalStorage only. Nothing is sent to any server. Use **Export JSON** in Settings to back up your data, and **Import JSON** to restore it (e.g. on a new device or browser).
