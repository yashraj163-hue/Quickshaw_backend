# Pooling Logic — Stage-1 (MVP)

QuickShaw uses a rule-based pooling system designed specifically for short-distance trips
in dense Tier-2 and Tier-3 city environments.

The goal of Stage-1 is to enable **fast, predictable pooling coordination**
without relying on heavy routing algorithms or real-time navigation systems.

---

## Rider Basket

Each ride request is stored as a **rider basket**, representing a lightweight snapshot
of a passenger’s intent rather than a fully optimized route.

A rider basket includes:
- Pickup location
- Destination
- Preferred pickup time
- Number of passengers
- Vehicle mode (rickshaw / e-auto)
- Pooling preference

Baskets are used as the primary unit for pooling decisions in the MVP.

---

## Primary Pooling Rules (MVP)

For two or more riders to be pooled together, all of the following conditions must be met:

### 1. Destination Alignment (Route Subset Rule)

- The second rider’s route must match or be a logical subset of the first rider’s route.
- Exact turn-by-turn route matching is **not required** at this stage.
- The focus is on shared direction and major path overlap rather than full route optimization.

This keeps matching simple while preserving rider expectations.

---

### 2. Time Gap Constraint

- The difference between preferred pickup times must be within **5 minutes**.

This ensures:
- Minimal waiting time
- High predictability for riders
- Reduced drop-off risk due to delays

---

### 3. Pooling Radius (Basket Compatibility)

- The service area is divided into predefined, route-based baskets.
- Only riders whose pickup points fall within compatible baskets are considered poolable.

This prevents inefficient detours and reduces computational complexity in the MVP.

---

## Driver Allocation

Once a valid rider pool is formed:

- Drivers are considered only if they can reach the first pickup point within approximately **2 minutes**
- Seat availability is verified before final pool confirmation

The short reach-time constraint minimizes idle waiting and keeps turnaround fast
for high-frequency trips.

---

## Why This Works for Stage-1

This rule-based approach prioritizes:
- Simplicity over full optimization
- Predictable behavior over algorithmic complexity
- Fast matching for short, high-frequency trips

By constraining scope at Stage-1, QuickShaw can validate pooling behavior,
driver adoption, and operational feasibility before introducing
advanced routing, pricing, or AI-driven optimization.
