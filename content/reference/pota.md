---
title: "POTA Activations"
description: "Parks on the Air logging and upload workflow"
weight: 4
showToc: true
---

Carrier Wave provides dedicated support for Parks on the Air (POTA) activations.

## Activation Mode

To log a POTA activation:

1. Open the **Logger** tab
2. Set **Activation Type** to **POTA**
3. Enter your park reference (e.g., US-0189)

All subsequent QSOs are tagged with that park reference until you change it.

## Park Reference Entry

### Manual Entry

Type the park reference directly (e.g., `US-0001`, `K-0001`, `VE-0001`).

### Park Search

Tap the search icon to find parks:
- Search by park name ("Acadia")
- Search by reference number
- Browse by state/region

### Nearby Parks

Tap the location icon to see parks near your current GPS position. Useful when you've arrived at an activation site.

## POTA Activations Tab

The **POTA** tab (if enabled in Settings) shows your activations grouped by park:

- Park name and reference
- Date(s) activated
- QSO count per activation
- Upload status

## Upload Workflow

POTA requires activations to be submitted as complete logs per park per day. Carrier Wave handles this automatically:

1. **Grouping:** QSOs are grouped by park reference and UTC date
2. **ADIF Generation:** Each group becomes a separate ADIF file
3. **Upload:** Files are uploaded to POTA via their API

### Manual Upload Trigger

By default, uploads happen automatically when you have network connectivity. To manually trigger:

1. Go to the **POTA** tab
2. Find the activation
3. Tap **Upload**

### Upload Status

| Status | Meaning |
|--------|---------|
| **Uploaded** | Successfully submitted to POTA |
| **Pending** | Queued for upload |
| **Error** | Upload failed - tap for details |

## Park-to-Park (P2P)

When you contact another POTA activator:

1. Enter their callsign
2. Enter their park reference in the **Park** field

Both activators get credit for a park-to-park contact. These are displayed distinctly in your log.

## Minimum QSO Requirement

POTA requires 10 QSOs for a valid activation. Carrier Wave shows your QSO count for the current activation session, helping you track progress toward the minimum.

## Multi-Park Activations

If you're activating multiple parks simultaneously (e.g., a park that qualifies for multiple references):

1. Complete your activation at the first park reference
2. Change the park reference
3. Continue logging

QSOs are grouped by the park reference active when they were logged.

## POTA Service Configuration

In **Settings > Services > POTA**:

- **Sign In:** Authenticate via OAuth
- **Auto-Upload:** Enable/disable automatic uploads
- **Upload History:** View past upload attempts

## See Also

- [Logger](/reference/logger/) - General logging features
- [Service Sync Flow](/reference/sync-flow/) - When uploads happen
- [Spot Monitoring](/reference/spots/) - Find other POTA activators
