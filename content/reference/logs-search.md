---
title: "Logs & Search"
description: "Query language, filters, and QSO management"
weight: 3
showToc: true
---

The Logs tab provides access to all your logged contacts with powerful search and filter capabilities.

## Log List

By default, the Logs tab shows your most recent contacts in reverse chronological order. Each entry displays:

- Callsign
- Date and time (UTC)
- Band and mode
- RST exchanged
- Sync status indicators

Tap any entry to view full details.

## Search

The search bar at the top supports two modes:

### Simple Search

Just type a callsign or partial callsign:

```
K6TEST
W1A
```

Searches across all callsign fields (their call, your call, operator call).

### Query Language

For more precise searches, use the query language:

#### Field Queries

| Query | Meaning |
|-------|---------|
| `call:K6TEST` | Exact callsign match |
| `band:20m` | Contacts on 20 meters |
| `mode:cw` | CW contacts only |
| `state:CA` | California contacts |
| `grid:CM87` | Grid square (4 or 6 char) |
| `park:US-0001` | POTA park reference |

#### Date Queries

| Query | Meaning |
|-------|---------|
| `date:today` | Today's contacts (UTC) |
| `date:yesterday` | Yesterday's contacts |
| `after:7d` | Last 7 days |
| `after:2024-01-01` | Since January 1, 2024 |
| `before:2024-06-01` | Before June 1, 2024 |

#### Status Queries

| Query | Meaning |
|-------|---------|
| `confirmed` | Confirmed via LoTW |
| `synced` | Synced to all services |
| `pending` | Awaiting sync |

#### Combining Queries

Use spaces to AND conditions:

```
band:20m mode:cw after:30d
```

Finds CW contacts on 20 meters in the last 30 days.

#### Examples

```
call:W1AW band:40m
```
All W1AW contacts on 40 meters.

```
state:CO mode:ssb after:2024-01-01
```
SSB contacts with Colorado stations this year.

```
park:* after:7d
```
All POTA contacts in the last week.

## Full-Table Search

By default, search queries the most recent 1,000 contacts for performance. For complete searches:

1. Enter your query
2. Tap **Search All** to scan your entire log

Full-table searches may take a moment for very large logs.

## QSO Details

Tap any contact to view the full QSO record:

- All logged fields
- Sync status per service
- Confirmation status
- Edit option
- Delete option

## Editing QSOs

From the detail view, tap **Edit** to modify any field. Changes are:

1. Saved locally
2. Re-queued for sync (services that support updates)

Note: Some services don't support updating previously uploaded QSOs.

## Deleting QSOs

From the detail view, tap **Delete** to remove a contact. Deletion:

1. Removes from local storage
2. Does NOT delete from cloud services (most services don't support remote deletion)

## See Also

- [Dashboard & Statistics](/reference/dashboard/) - View aggregated stats
- [Service Sync Flow](/reference/sync-flow/) - Understand sync behavior
