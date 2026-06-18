# Concept Review Minutes Tool

A lightweight, browser-based tool for logging product concept reviews in real time. No server, no database, no dependencies — just open `index.html` and go.

## Features

- **Session control** — Start/Stop Session button kicks everything off; Break button is locked until the session is running
- **Project gate** — the note-taking area is locked behind a Start Project button, so the timer always runs before you type. Selecting an outcome immediately resets the gate for the next project
- **Live session timer** with per-project stopwatch and break tracking
- **Three outcomes** — Continue Project, Vision Agreed Approval, Cancel Project
- **Inline edit** — edit any logged project's name, owner, and notes directly in the table via the edit button, without disrupting the session
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

## Session flow

1. Enter the **Stage** and **Season** at the top (e.g. CR4 / SS28)
2. Click **Start Session** — the session timer starts and the project gate unlocks
3. Click **Start Project** — the project timer starts automatically and the form unlocks
4. Fill in the **project name**, **owner**, and **notes** as the review happens
5. Click **Continue Project**, **Vision Agreed Approval**, or **Cancel Project** to log it — the gate resets immediately for the next project
6. Use **Break** to pause everything between reviews
7. Click the **pencil icon** on any logged project to edit its name, owner, or notes inline, then click **Save changes**
8. Click **Export HTML report** at the end to download a shareable report

## Exporting

The exported `.html` file includes:
- Session stats (elapsed time, project count, averages, break time)
- Full timeline SVG with colour-coded segments and project labels
- Complete project log with notes
- Owner summary cards

The exported file is fully self-contained and matches the same visual style as the tool.

## Customising

All logic and styling lives in a single `index.html` file. To change outcome labels, find the `OUTCOMES` array near the top of the `<script>` block and update the values. Colours are controlled by the `COLORS` and `EXPORT_COLORS` objects directly below it.
