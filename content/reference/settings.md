---
title: "Settings & Services"
description: "Configuration, service authentication, and preferences"
weight: 5
showToc: true
---

The Settings screen configures your profile, service connections, and app preferences.

## Profile

### Callsign

Your primary operating callsign. This is used as "your call" for all logged QSOs.

### Callsign Aliases

Additional callsigns you operate under:
- Previous callsigns
- Club callsigns
- Special event callsigns

Aliases help with sync matching and duplicate detection.

### Name

Your name as you'd like it displayed.

### QTH

Your location (city, state/province, country).

### Grid Square

Your Maidenhead grid locator. If location permissions are granted, this auto-updates based on GPS.

### License Class

Your amateur license class (Technician, General, Amateur Extra for US operators). Used for band plan validation warnings.

## Services

### QRZ.com

**Authentication:** Username and password

**Features:**
- Callsign lookups (name, QTH, grid)
- QSO upload to QRZ Logbook
- QSO download from QRZ Logbook

**Settings:**
- Enable/disable auto-sync
- Download existing log on first sync

### POTA

**Authentication:** OAuth (sign in via web view)

**Features:**
- Activation upload
- Park reference lookup

**Settings:**
- Enable/disable auto-upload
- View upload history

### Ham2K LoFi

**Authentication:** Email-based device linking

**Setup:**
1. Enter your email address
2. Check email for device link
3. Tap link to authorize this device

**Features:**
- Bidirectional QSO sync
- Cross-device synchronization

**Settings:**
- Enable/disable auto-sync
- Sync frequency

### Logbook of The World (LoTW)

**Authentication:** Username and password (same as ARRL website)

**Features:**
- Download confirmations
- Mark QSOs as confirmed

**Limitations:**
- Download only - use TQSL for uploads
- Confirmation data only, not full QSOs

### HAMRS

**Authentication:** OAuth

**Features:**
- Bidirectional QSO sync
- Compatible with HAMRS cloud

## iCloud Sync

**Enable iCloud:** Toggle to sync app data across your Apple devices.

**What syncs:**
- QSO database
- App settings
- Callsign notes

**What doesn't sync:**
- Service credentials (stored in Keychain per-device)

See [iCloud Sync](/reference/icloud/) for details.

## Callsign Notes

Import additional callsign data from external files:

**Sources:**
- Club rosters
- Contest exchange lists
- Custom callsign databases

**Format:** CSV or JSON files with callsign → notes mapping.

**Usage:** When you work a callsign in your notes file, the notes appear during logging.

## Appearance

### Theme

- **System** - Follow iOS dark/light mode
- **Light** - Always light
- **Dark** - Always dark

## Advanced

### Sync Debugging

View detailed sync logs for troubleshooting:
- Request/response logs
- Error details
- Timing information

### Bug Reports

Generate a diagnostic report including:
- Device information
- App version
- Recent error logs
- Database statistics (no personal data)

Reports can be emailed to support.

## See Also

- [Service Sync Flow](/reference/sync-flow/) - How and when syncing works
- [iCloud Sync](/reference/icloud/) - Cross-device synchronization
- [Troubleshooting](/reference/troubleshooting/) - Common issues and solutions
