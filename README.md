# Hidaya Analytics Web App — MVP

## Included
- Responsive black-and-gold analytics dashboard.
- Multi-select filters for platform, metric, year, and month.
- KPI total, monthly trend chart, results table, CSV export.
- Demo-only values; no real Hidaya source data is embedded or exposed.

## Data safety / production architecture
The page is a frontend MVP. It intentionally does **not** connect to a live database yet and does not contain real Hidaya business metrics. Do not publish actual metrics as a public static file unless they have been approved for public disclosure.

Recommended production flow:
1. Keep the original Excel/source exports read-only and versioned.
2. Load normalized records into a private database (PostgreSQL or managed equivalent).
3. Preserve platform-specific metric definitions and the source app label. Map `Hidaya` (Android) and `Quran Hidaya` (iOS) to logical app `Hidaya Main App` only in a reporting view; never rewrite source labels.
4. Expose only approved aggregate values through a read-only API. Add allowlisted metric IDs, date filters, and rate limits.
5. Public page calls that API; secrets and database credentials remain server-side, never in browser code.
6. Add a validation job comparing record counts and totals against source exports before each import.

## Current metric scope
- Android: `Daily Device Installs` is a platform-specific metric.
- iOS: `First-Time Downloads`, `Total Downloads`, and `Redownloads` are distinct platform-specific metrics.
- Avoid adding unlike metrics into a single headline total. When multiple metrics are selected, display separate groups/series by metric and platform.

## Run locally
Open `index.html` in a modern browser. All interactive values are demo values until the backend/API is connected.
