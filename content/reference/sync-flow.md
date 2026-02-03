---
title: "Service Sync Flow"
description: "When and how QSOs sync to cloud services"
weight: 6
showToc: true
---

Understanding Carrier Wave's sync behavior helps you know when your data is safely backed up.

## Sync Timing

### Automatic Sync

QSOs sync automatically when:

1. **After saving:** A few seconds after you save a QSO, sync begins
2. **App foreground:** When the app becomes active
3. **Network restored:** When connectivity returns after being offline
4. **Pull to refresh:** When you pull down on Dashboard

### Batching

QSOs are batched for efficiency:
- Multiple QSOs pending? They upload together
- Reduces API calls and battery usage

### Rate Limiting

Services impose rate limits. Carrier Wave respects these:
- Spreads requests over time if needed
- Won't hammer services during bulk operations

## Sync Direction by Service

| Service | Upload | Download |
|---------|--------|----------|
| QRZ.com | ✓ QSOs | ✓ QSOs, Callsign info |
| POTA | ✓ Activations | ✗ |
| Ham2K LoFi | ✓ QSOs | ✓ QSOs |
| LoTW | ✗ | ✓ Confirmations |
| HAMRS | ✓ QSOs | ✓ QSOs |

## Service-Specific Behavior

### QRZ.com

**Upload format:** ADIF via XML-RPC API

**Timing:** Near real-time after QSO save

**Duplicate handling:** QRZ deduplicates on their end based on date/time/call/band

**Callsign lookups:** Happen during QSO entry, cached locally

### POTA

**Upload format:** ADIF files, one per park per UTC date

**Timing:** After activation is complete (manual or automatic)

**Grouping:** QSOs grouped by park reference and date

**Validation:** POTA validates on their end; errors returned if issues

### Ham2K LoFi

**Upload format:** JSON via REST API

**Timing:** Near real-time bidirectional

**Conflict resolution:** Latest timestamp wins

**Full sync:** Initial connection downloads entire history

### LoTW

**Download only:** Carrier Wave fetches confirmations

**Timing:** Periodic check (configurable)

**Matching:** Confirmations matched to local QSOs by date/time/call/band

### HAMRS

**Upload format:** JSON via REST API

**Timing:** Near real-time bidirectional

**Compatibility:** Works with HAMRS cloud accounts

## Offline Operation

Carrier Wave works fully offline:

1. Log QSOs normally
2. QSOs saved to local database
3. Marked as "pending sync"
4. When online, sync resumes automatically

No data is lost if you're in a park without signal.

## Sync Status Indicators

On the Dashboard, each service shows:

| Indicator | Meaning |
|-----------|---------|
| ✓ Green | Synced, nothing pending |
| ↻ Yellow | Sync in progress |
| ! Red | Error on last sync |
| ○ Gray | Service not configured |
| n Pending | Count of QSOs awaiting sync |

## Retry Logic

When sync fails:

1. **Transient errors** (network timeout): Automatic retry with exponential backoff
2. **Auth errors** (expired token): Prompts for re-authentication
3. **Permanent errors** (invalid data): Marked as failed, requires manual intervention

## Conflict Resolution

When the same QSO exists locally and remotely with different data:

**LoFi:** Most recent modification wins (timestamp-based)

**QRZ:** Remote is authoritative for downloads; local edits create updates

**POTA:** Upload-only, no conflicts possible

## Monitoring Sync

To see detailed sync activity:

1. **Settings > Advanced > Sync Debugging**
2. Enable verbose logging
3. View request/response details

Useful for troubleshooting sync issues.

## See Also

- [Settings & Services](/reference/settings/) - Configure service connections
- [Troubleshooting](/reference/troubleshooting/) - Sync problems and solutions
- [iCloud Sync](/reference/icloud/) - Device-to-device sync
