# CULINES Terminal Throughput Dashboard

Interactive pivot table dashboard for CULINES Terminal Throughput data (2025–2026 YTD).

## Features

- **6 interactive pivot tables**: Port x Month, Lane x Month, Port x Lane x Type, Outbound Report, Inbound Report, Booking vs Actual
- **Full drag-and-drop**: PivotTable.js — freely drag fields between rows, columns, filters, and values
- **Quick presets**: Filter by year, quarter, IN/OUT type, or view all data
- **Browser-native**: No server needed — pure static HTML + JavaScript

## Quick Start (Local)

1. Clone this repo
2. Open `index.html` in a modern browser (Chrome/Edge recommended)

> Note: `data/pivot_data.json` must be served via HTTP (not `file://`) due to browser CORS. Use:
> ```bash
> npx serve .
> ```
> or any static server.

## Deploy to GitHub Pages

1. Create a new **public** repository on GitHub (e.g. `culines-throughput`)
2. Push this folder to the repo:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/culines-throughput.git
   git push -u origin main
   ```
3. Go to **Settings → Pages → Source**: select `main` branch and `/ (root)`, click **Save**
4. Wait ~2 minutes, your dashboard will be live at:
   ```
   https://YOUR_USERNAME.github.io/culines-throughput/
   ```

## Data Source

Raw data is exported from CULINES BI (FineBI) via automated scripts. Update `data/pivot_data.json` to refresh with new data.

## Updating Data

When new BI data is available, re-run the export script to regenerate `data/pivot_data.json`, then push the updated JSON to GitHub. The dashboard auto-loads the latest data on refresh.
