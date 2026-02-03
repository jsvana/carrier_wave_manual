---
title: "Dashboard & Statistics"
description: "Activity statistics, streaks, and drill-down views"
weight: 2
showToc: true
---

The Dashboard provides an overview of your logging activity and service status.

## Statistics Grid

The main statistics display shows your QSO counts across several dimensions:

### By Band

Total contacts per amateur band. Includes:
- HF bands: 160m, 80m, 60m, 40m, 30m, 20m, 17m, 15m, 12m, 10m
- VHF/UHF: 6m, 2m, 1.25m, 70cm, 33cm, 23cm

### By Mode

Contacts grouped by operating mode:
- SSB, CW, FM, AM
- Digital modes: FT8, FT4, RTTY, PSK31, etc.

### By Country/DXCC

Unique DXCC entities worked. The count represents distinct entities, not total QSOs.

### Additional Statistics

- **Grid Squares** - Unique Maidenhead grids
- **States** - US states and Canadian provinces
- **Parks Activated** - POTA parks you've activated
- **Parks Worked** - POTA parks you've contacted

## Drill-Down Views

Tap any statistic to see the underlying contacts:

- Tap a band count to see all QSOs on that band
- Tap a mode count to filter by that mode
- Tap a country to see contacts with that DXCC entity

Drill-down views support further filtering and sorting.

## Streaks

Below the statistics grid, your current logging streak is displayed:

**Current Streak:** Consecutive days with at least one QSO logged.

Streaks reset at UTC midnight. Missing a day resets the counter to zero.

## Service Status

Each configured service shows its sync status:

| Status | Meaning |
|--------|---------|
| **Synced** (green) | All QSOs uploaded, no pending |
| **Syncing** (yellow) | Upload or download in progress |
| **Error** (red) | Last sync failed - tap for details |
| **Pending** | QSOs waiting to sync |

Tap any service to see:
- Last successful sync time
- Number of pending uploads
- Error details (if any)
- Manual sync trigger

## Background Computation

Statistics are computed on a background thread to keep the app responsive. When opening the Dashboard:

1. Cached statistics display immediately
2. A background task recomputes current totals
3. Display updates when computation completes

For large logs (thousands of QSOs), you may see a brief progress indicator during recomputation.

## Pull to Refresh

Pull down on the Dashboard to trigger:
- Statistics recomputation
- Sync check for all services

## See Also

- [Logs & Search](/reference/logs-search/) - Query your contacts directly
- [Service Sync Flow](/reference/sync-flow/) - Understand sync timing
- [Settings & Services](/reference/settings/) - Configure service connections
