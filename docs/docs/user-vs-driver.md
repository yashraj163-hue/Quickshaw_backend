# User vs Driver View — Information Design

QuickShaw is intentionally designed with **asymmetric information visibility**
between passengers and drivers.

This separation is a deliberate product decision aimed at reducing cognitive load,
preventing misaligned incentives, and improving operational efficiency
in short-distance, high-frequency mobility scenarios.

---

## User View (Passenger App)

Passengers are shown only the information required to make fast,
low-effort decisions.

Visible to users:
- Estimated pickup time
- Estimated fare per person
- Pooling confirmation status
- Vehicle type and available seats

Hidden from users:
- Demand heat zones
- Surge, boost, or incentive logic
- Other passengers’ identities
- Internal basket or routing logic

By hiding operational complexity, the user experience remains calm,
predictable, and suitable for frequent daily usage.

---

## Driver View (Driver App)

Drivers are provided with operational data needed to maximize daily earnings
and minimize idle time.

Visible to drivers:
- Demand heat zones
- Pooling routes and basket coverage
- Seat availability across pooled requests
- Boosts and incentive signals

Hidden from drivers:
- Passenger personal details beyond pickup requirements

This view enables informed decision-making without exposing
unnecessary personal data.

---

## Design Rationale

Separating information visibility allows each side of the platform
to focus on what matters most:

- **Passengers** experience a simple, predictable flow without
  cognitive overload or pricing anxiety.
- **Drivers** gain operational tools to optimize routing, timing,
  and earnings throughout the day.
- **The system** avoids manipulation, confusion, and incentive conflicts
  that can arise when all actors see the same data.

This asymmetric design is essential for maintaining trust,
scalability, and behavioral alignment in pooled, short-distance mobility.
