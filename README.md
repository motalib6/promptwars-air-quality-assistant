# BreatheEasy — PromptWars Challenge 06: Urban Air Quality Assistant

A single-page Urban Air Quality Assistant: search any city, see live AQI and pollutants, check the 24-hour outlook, and get a personalised plan from a free-text prompt.

## What it does
1. **City search** — free Open-Meteo geocoding API (no key needed), with suggestions. Default city: Delhi; your last city is remembered in the browser (localStorage).
2. **Live AQI** — current US AQI from the Open-Meteo Air Quality API (CAMS data), shown as a big number with its category (Good / Moderate / Unhealthy for Sensitive Groups / Unhealthy / Very Unhealthy / Hazardous) and colour, plus health advice for that level.
3. **Pollutant breakdown** — PM2.5, PM10, ozone (O₃) and nitrogen dioxide (NO₂), with a plain-English note on what each means (including WHO guideline values).
4. **24-hour outlook** — hourly AQI bars for the next 24 hours, with the cleanest and worst hours picked out, so you can choose the best window to go outside.
5. **Prompt-driven plan** — type your situation in your own words (e.g. "I have asthma, plan my outdoor run in Delhi today") and get a verdict plus a plan adapted from the keywords: asthma, running/exercise, kids, elderly, pregnancy, masks, indoor air, commute.
6. **Practical tips** — masks, best outdoor hours, indoor air, exercise, children & elderly.

## How to run
Open `index.html` in any browser. No build step, no server, no sign-up, no external CDN — the page is a single HTML file and fetches live data directly from Open-Meteo (internet needed for the live AQI; the advice and layout work without it once loaded).

## Honest note on data and "GenAI"
- **Data is real:** AQI, pollutants and the 24-hour outlook come live from the free Open-Meteo Air Quality API (CAMS) and the Open-Meteo Geocoding API. No values are invented or hard-coded.
- **Advice is prompt-driven, not a hosted LLM:** the planner reads your prompt's keywords (asthma, run, kids, mask, indoor…) and adapts the plan from the live AQI. It calls no hosted LLM API, needs no API key, and no data leaves your browser. The demo video shows the real app loading real AQI for real cities.
- Health advice is general information, not medical advice.

## Submission checklist (PromptWars Challenge 06)
- Live App URL: GitHub Pages URL for this repo (see repo Pages settings)
- GitHub Repo: this public repository (<10 MB, single HTML page + README)
- Walkthrough Video: <4 min screen recording of the core features (demo.mp4)
