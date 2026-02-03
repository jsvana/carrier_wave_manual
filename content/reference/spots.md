---
title: "Spot Monitoring"
description: "RBN spots, POTA spots, and propagation info"
weight: 8
showToc: true
---

The Spot Monitoring panel helps you find stations to work and understand current conditions.

## Accessing Spot Monitoring

From the Logger tab, tap the **Spots** button to open the monitoring panel.

## Spot Types

### RBN (Reverse Beacon Network)

The RBN is a network of receiving stations that automatically decode CW and digital signals, reporting:

- Callsign spotted
- Frequency
- Mode (CW, FT8, etc.)
- Signal strength (dB)
- Spotting station location

**Use for:** Finding CQ'ing stations, checking if you're being heard.

### POTA Spots

Active Parks on the Air activators:

- Activator callsign
- Park reference and name
- Frequency and mode
- Time spotted

**Use for:** Hunting park activators, finding P2P opportunities.

### Park-to-Park (P2P)

If you're activating a park, this filter shows other active POTA stations - potential park-to-park contacts.

## Filtering Spots

Use the filter controls to narrow results:

### By Band

Show only spots on specific bands (20m, 40m, etc.).

### By Mode

Filter to CW, SSB, FT8, or other modes.

### By Region

Focus on specific geographic areas.

## Spot Map

The map view shows:

- Your location
- Spotted stations as pins
- RBN receiver locations
- Signal paths

Pin size or color may indicate signal strength.

## Solar & Weather Conditions

The conditions panel shows:

- **Solar Flux Index (SFI)** - Higher is better for HF
- **A Index** - Geomagnetic activity (lower is better)
- **K Index** - Short-term geomagnetic (lower is better)
- **Band conditions** - Good/Fair/Poor per band

Data sourced from NOAA.

## Refresh Interval

Spots refresh automatically:
- Every 45 seconds while the panel is open
- Manual refresh by pulling down

## Using Spots While Logging

The spot panel can remain open while logging:

1. See a spot you want to work
2. Tap the spot to populate the Logger
3. Make the contact
4. Callsign and frequency pre-filled

## QRM Assessment

For some spots, the app shows frequency activity:
- How busy is that frequency?
- Are there other stations nearby?

Helps you decide if it's worth calling.

## Data Sources

| Data | Source |
|------|--------|
| RBN spots | Vail ReRBN API |
| POTA spots | POTA API |
| Solar data | NOAA |

## See Also

- [Logger](/reference/logger/) - Log contacts from spots
- [POTA Activations](/reference/pota/) - POTA-specific features
