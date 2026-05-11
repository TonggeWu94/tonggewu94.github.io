# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a GitHub Pages site (`tonggewu94.github.io`) — a single-page static site with no build system, no dependencies, and no tests. It renders a visual "Timeline of Your Life" showing 100 years as a continuous SVG snake pattern, with life stage labels and the current date highlighted by a breathing white dot.

## Development

Open `index.html` directly in a browser to preview. No server or build step required.

## Architecture

- `index.html` — the entire application: markup, CSS, and JavaScript in one file
- Renders using SVG with programmatic element creation (no external libraries)
- Birthday is hardcoded as `1994-12-20`; the timeline calculates age and year-progress dynamically
- Snake pattern: even ages go left-to-right, odd ages go right-to-left, connected by SVG arc U-turns
- 6 life stage color bands: yellow (0-12), orange (13-19), pink (20-34), purple (35-49), blue (50-79), green (80-99)
- Past years are fully colored, current year is partially colored up to today, future years are grey
- White dot on current position has breathing animation and hover/touch tooltip showing week count
- Vertical life stage labels positioned on the right side outside the snake area
- Font: SF Hello with -apple-system fallback
- `archive/` — old image assets not used by the current site

## Deployment

Pushed to `main` branch → automatically deployed via GitHub Pages.
