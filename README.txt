Hidaya Analytics — Data-loaded Frontend Preview
================================================

Open index.html in a modern browser.

Source: Hidaya_Combined_PowerBI_Source_2021_2026.xlsx, sheet "Unified Fact Data".
Embedded rows: 22,570 source records, date range 2021-05-24 through 2026-10-09.
Apps: Android / Hidaya; iOS / Quran Hidaya.
Metrics: 10 Android source metrics and 3 iOS source metrics.

Functional in this preview:
- Platform, metric, year, and month filters
- Summary KPIs and source-record counts
- Monthly trend for a selected metric
- Monthly detailed results
- CSV export of filtered monthly results
- Latest source records

Data integrity notes:
- Country-level data is absent from the supplied workbook, so country values are not fabricated.
- Android and iOS metric definitions are preserved separately.
- "Active Device Installs" is a daily snapshot and is not summed across days; table/chart show the latest daily snapshot for each month.
- Other metric monthly values are sums of source daily values, and interpretation remains source-specific.
- This is still a static frontend with embedded data, not a database connection or automatic refresh. Database integration remains a separate next step after UI review.
