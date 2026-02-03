---
title: "Logger"
description: "QSO entry, session settings, and logging features"
weight: 1
showToc: true
---

The Logger is Carrier Wave's primary interface for recording contacts.

## Session Settings

At the top of the Logger screen, configure your operating session:

### Band

Select your operating band from the picker. Available bands include all amateur allocations from 160m through 23cm.

The selected band persists until you change it.

### Mode

Choose your operating mode:
- **SSB** - Single sideband voice (LSB below 10 MHz, USB above)
- **CW** - Morse code
- **FM** - Frequency modulation (VHF/UHF)
- **AM** - Amplitude modulation
- **FT8** - Digital weak-signal
- **FT4** - Fast digital
- **RTTY** - Radioteletype
- **PSK31** - Phase shift keying
- **DATA** - Generic digital mode

### Frequency

Enter your operating frequency in MHz (e.g., 14.250). This is optional but helps with:
- Band plan validation
- Duplicate detection precision
- Historical reference

### Activation Type

If you're operating a special event or activation:
- **None** - Normal operation
- **POTA** - Parks on the Air activation
- **SOTA** - Summits on the Air
- **IOTA** - Islands on the Air

When POTA is selected, additional park reference fields appear.

## QSO Entry Fields

### Callsign

The primary field. Enter the other station's callsign.

**Auto-lookup:** As you type, Carrier Wave queries QRZ.com (if configured) for matching callsigns. When found, the station's name, location, and grid square populate automatically.

**Validation:** The app validates callsign format and warns about obviously invalid entries.

### RST Sent / RST Received

Signal reports exchanged during the contact.

- **Voice (SSB/FM):** Reports are RS (1-5 readability, 1-9 strength). Default: 59.
- **CW/Digital:** Reports are RST (adds 1-9 tone). Default: 599.

Tap the field to enter manually, or use the +/- steppers for quick adjustment.

### Name

The operator's name. Often auto-filled from QRZ lookup.

### State/Province

US state or Canadian province. Auto-filled from QRZ when available.

**QRZ Override:** If the operator gives you a different state than what's in QRZ (portable operation), you can override the auto-filled value.

### Grid Square

The station's Maidenhead grid locator (4 or 6 characters).

### Park Reference

For POTA contacts, enter the park reference (e.g., US-0001 for Acadia).

**Park Search:** Tap the search icon to find parks by name or reference number.

**Nearby Parks:** Tap the location icon to see parks near your current location.

### Operator

The individual operator's callsign, if different from the station callsign (e.g., guest operators at a club station).

### Notes

Free-form text field for anything memorable about the contact.

## Quick Entry Mode

For rapid logging, enable Quick Entry mode. Type everything in one line:

```
K6TEST 599 CA
```

Format: `CALLSIGN RST STATE` (or `CALLSIGN RST GRID`)

The parser understands common formats and extracts the components automatically.

## Duplicate Detection

Carrier Wave warns you when logging potential duplicates:

**Same-band duplicate:** A contact with the same callsign, same band, same UTC date is flagged as a likely duplicate.

**Different-band contact:** Contacts with the same callsign on a different band or date are highlighted (green) to indicate you've worked them before but this is a valid new contact.

## Band Plan Validation

If you've set your license class in Settings, Carrier Wave can warn when logging contacts outside your frequency privileges.

This doesn't prevent logging - you may be logging someone else's QSOs or operating under a different license - but it helps catch mistakes.

## Saving QSOs

Tap **Save QSO** to record the contact. The QSO is:

1. Saved immediately to local storage
2. Queued for sync to all configured services
3. Time-stamped with the current UTC time

Sync happens in the background. You can continue logging without waiting.

## See Also

- [Dashboard & Statistics](/reference/dashboard/) - View your logged contacts
- [Logs & Search](/reference/logs-search/) - Find specific QSOs
- [Service Sync Flow](/reference/sync-flow/) - Understand when syncing happens
