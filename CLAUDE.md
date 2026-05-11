# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a GitHub Pages site (`tonggewu94.github.io`) — a single-page static site with no build system, no dependencies, and no tests. It renders a visual "Timeline of Your Life" showing 100 years as colored horizontal lines in a snake pattern, with the current date highlighted by an animated dot.

## Development

Open `index.html` directly in a browser to preview. No server or build step required.

## Architecture

- `index.html` — the entire application: markup, CSS, and JavaScript in one file
- Birthday is hardcoded as `1994-12-20`; the timeline calculates age and year-progress dynamically from the current date
- Color bands are assigned per decade (0–9 gold, 10–19 orange, etc.)
- Past years are fully colored, the current year is partially colored up to today, future years are grey
- Image assets (`.jpeg`, `.webp`) are reference/decoration files stored at the repo root

## Deployment

Pushed to `main` branch → automatically deployed via GitHub Pages.
