# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a single-page HTML application that visualizes rainbow song popularity data using Chart.js. The application displays songs categorized by color (red, orange, yellow, green, blue, indigo) with average popularity scores and standard deviations.

## File Structure

- `rainbow_songs.html` - Standalone HTML file containing all HTML, CSS, and JavaScript

## Development

This is a static HTML file with no build process or dependencies. To view:

```bash
open rainbow_songs.html
```

Or serve locally with any HTTP server:

```bash
python3 -m http.server 8000
# Then visit http://localhost:8000/rainbow_songs.html
```

## Architecture

The application is entirely self-contained within a single HTML file:

- **Data Structure**: Song data is hardcoded in the `allData` object (lines 152-310), organized by color with labels, averages, and standard deviations
- **Chart Rendering**: Uses Chart.js 4.4.0 (loaded from CDN) with a custom error bar plugin for visualizing standard deviations
- **Filtering**: Interactive buttons filter and sort data by color category or display all songs together
- **Sorting Modes**: Two sorting modes available - by average score (default) or by standard deviation
- **Dynamic Height**: Chart container adjusts height when displaying all songs vs. a single color category
