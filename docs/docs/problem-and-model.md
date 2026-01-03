# QuickShaw — Problem & Business Model (Stage-0)

## Problem

QuickShaw targets short-distance daily commutes (typically within ~5 km) in Tier-2 and Tier-3 cities,
where rickshaws and e-autos dominate local mobility.

In these cities, pooling demand exists naturally, but coordination is manual and inefficient.
Passengers and drivers rely on roadside negotiation, shouting destinations, or waiting for
co-passengers without any system-level visibility.

This results in:
- Increased roadside congestion and chaos
- Longer waiting times for both passengers and drivers
- Low vehicle occupancy despite high demand
- Frustration caused by uncertainty and repeated negotiation

---

## Why Cab-Style Platforms Don’t Fit

Short-distance rickshaw and e-auto trips are low-cost but high-frequency.
Commission-based ride-hailing models are poorly suited to this category because:

- Per-ride commissions significantly reduce already small driver earnings
- Drivers are incentivized to avoid pooling in favor of faster solo trips
- Platform economics favor longer, higher-value rides rather than dense local movement

As a result, cab-oriented platforms fail to align with the daily economics of local mobility.

---

## Solution (Stage-0 / MVP-Level)

QuickShaw introduces lightweight, real-time pooling coordination without full route optimization
or heavy map dependency.

At a high level:
- Passengers select destination, vehicle mode (rickshaw / e-auto), and pooling preference
- The backend groups requests using **basket + route similarity + time-gap matching**
- Drivers receive real-time visibility into pooled demand instead of individual ride requests

This approach focuses on **coordination**, not full automation, making it suitable for early-stage deployment.

---

## Driver-First Economics (Daily Subscription Model)

Instead of per-ride commission, QuickShaw uses a small **daily login fee** paid when drivers open the app.

This model is designed to:
- Keep per-ride earnings intact for drivers
- Align platform revenue with daily usage rather than ride value
- Reduce friction for high-frequency, low-value trips
- Encourage pooling behavior instead of discouraging it

The daily model matches the operational reality of rickshaw and e-auto drivers,
who think in terms of **daily earnings**, not per-ride margins.

---

## Scope Notes (Stage-0)

Stage-0 intentionally excludes:
- Dynamic pricing algorithms
- Full route optimization
- Real-time navigation or ETA prediction

The goal at this stage is to validate pooling coordination and driver adoption
before introducing additional complexity.
