# Concept Review Tool

A lightweight, browser-based tool for logging product concept reviews in real time. No server, no database, no dependencies — just open `index.html` and go.

## Features

- **Live session timer** with per-project stopwatch and break tracking
- **Three outcomes** — Continue Project, Vision Agreed Approval, Cancel Project
- **Session timeline** — visual SVG bar showing the full session at a glance, colour-coded by outcome and annotated with project names
- **Owner summary cards** — per-owner breakdown of projects, time, and outcomes
- **One-click HTML export** — generates a self-contained report file you can share or archive

## How to use

### Option 1 — Run locally
Download or clone the repo, then open `index.html` in any browser. No install needed.

### Option 2 — Host on GitHub Pages
1. Fork or push this repo to your GitHub account
2. Go to **Settings → Pages**
3. Under **Branch**, select `main` and root `/`
4. Click **Save** — your tool will be live at `https://<your-username>.github.io/<repo-name>/`

## During a session

1. Enter the **Stage** and **Season** (e.g. CR4 / SS28) at the top
2. Type the **project name** and **owner**
3. Add **notes** as you go
4. Hit **Start** to run the project timer
5. Click **Continue Project**, **Vision Agreed Approval**, or **Cancel Project** to log it — the form resets automatically for the next project
6. Use **Break** to pause everything between reviews

## Exporting

Click **Export HTML report** at any point to download a self-contained `.html` file with:
- Session stats
- Full timeline SVG
- Complete project log with notes
- Owner summary cards

The exported file matches the same visual style as the tool and can be shared directly or archived.

## Customising

All logic and styling lives in a single `index.html` file. To change outcome labels, find the `OUTCOMES` array near the top of the `<script>` block and update as needed. Colours are controlled by the `COLORS` and `EXPORT_COLORS` objects directly below it.
