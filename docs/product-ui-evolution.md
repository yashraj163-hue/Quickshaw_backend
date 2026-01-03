# QuickShaw – Product & UI Evolution (Stage-0 → Stage-1)

This repository documents the evolution of the QuickShaw interface from a
generic, marketing-oriented landing page into a real-time, algorithmic
pooling dashboard designed specifically for **Tier-2 and Tier-3 city
transport dynamics**, with Varanasi as the MVP geography.

The purpose of this iteration is to expose backend pooling logic,
pricing rules, time constraints, and driver economics directly to users
through clear and operational UI/UX decisions.

---

## 🔁 The Evolution: From Static to Operational

### V1 – The Marketing Phase (Initial State)

**Concept**
- A standard ride-hailing landing page.

**Shortcoming**
- Treated QuickShaw like a traditional, high-cost cab service.
- Ignored the core business model: **high-frequency, low-cost Rickshaw
  and E-Auto pooling**.
- Pooling logic, pricing rules, and operational constraints were hidden
  from users.

➡️ Result:  
The interface functioned as a **promotional website**, not a mobility system.

---

### V2 – The Operational Pooling Dashboard (Current State)

**Goal**
- Convert the UI into a **real-time operational dashboard**.
- Make algorithmic decisions visible, predictable, and trustworthy.
- Align the frontend 1:1 with **Stage-0 and Stage-1 business logic**.

---

## ✅ Key Implementations (Aligned with Stage-0 & Stage-1)

### 1️⃣ Vehicle Specifics & Capacity

**Business Requirement**
Rickshaw and E-Auto are the foundational transport units, each with
distinct capacity and pricing.

**Implementation**
- **Rickshaw:** Explicitly labeled for 4–5 people, base fare **₹15 per seat**
- **E-Auto:** Labeled for 5–6 people, base fare **₹10 per seat**
- Vehicle-specific icons and capacity indicators added

**Outcome**
Users immediately understand the **capacity-to-price ratio** before booking.

---

### 2️⃣ The 6-Basket Pooling System (Algorithmic Primitive)

**Business Requirement**
The city is divided into **6 operational baskets (B1–B6)**.
Pooling is only allowed for:
- Same route
- Same destination
- Same basket

**UI Implementation**
- Routes tagged with basket labels  
  (e.g. *IIT BHU → Godowlia (B6)*)
- Basket-to-basket flow clearly shown (e.g. *B4 → B6*)

**Outcome**
The Basket system acts as an **algorithmic primitive** rather than a visual tag,
making matching rules transparent and deterministic.

---

### 3️⃣ Time-Sensitive Urgency & Pooling Constraints

**Business Requirement**
- Pickup time gap must be **less than 5 minutes**
- Campus use-cases target **~2 minutes arrival time**

**UI Implementation**
- Real-time indicators such as:
  - *“Leaves in 2 mins”*
  - *“Enroute”*
- Countdown-based urgency signals for short-distance commutes

**Outcome**
Users understand *why* a ride is shown and *why* it may disappear.

---

### 4️⃣ Subscription-Based Driver Model (Critical Correction)

**Problem**
Traditional commission models (20–30%) fail in low-cost,
high-frequency transport categories.

**Solution**
- **Flat Login Fee: ₹30 per day**
- No per-ride commission
- Fee is required once per day and re-asked when the date changes

**UI Implementation**
- Persistent status bar:
  > **Login Fee: ₹30/day — Required once per day. Re-asked when date changes.**

**Outcome**
Driver economics are sustainable and fully aligned with Stage-0 definitions.

---

### 5️⃣ Financial Transparency & Convenience Fee

**Business Requirement**
Fare calculation follows:
> Base Fare (per seat) + Convenience Fee

The Convenience Fee is **distance-based**, calculated dynamically
(e.g. per kilometer), as defined in Stage-1.

**UI Implementation**
- Clear separation between:
  - Base fare
  - Convenience Fee *(calculated based on trip distance)*
- Payment indicators:
  - **UPI / Cash**, reflecting real infrastructure constraints

**Outcome**
No hidden costs, no ambiguity in fare composition.

---

### 6️⃣ Trust Signals Without Marketing Noise

**Business Requirement**
Target users are students and tech-savvy riders who trust data over slogans.

**UI Implementation**
- Passenger profile photos
- Ratings (e.g. 4.8+, 4.9+)
- Ride counts and pooling labels

**Outcome**
Trust is demonstrated through **verifiable signals**, not claims.

---

## 🛠 Architectural Shift Summary

| Feature | Version 1 (Generic) | Version 2 (Operational) |
|------|--------------------|------------------------|
| Pricing | Static / Hidden | Dynamic (Base + Conv. Fee) |
| Logic | Manual booking | Algorithmic (Same Route / Time) |
| Zones | Generic city | 6-Basket System (B1–B6) |
| Driver Fee | Missing | ₹30/day Login Fee |
| Time Rules | Implicit | Explicit (<5 min gap) |
| Trust | Slogans | Ratings & Ride Counts |

---

## 🚀 Next Steps (Stage-2)

- **Pool on the Go:** Matching based on real-time movement direction
- **Heat Mapping:** High-demand density visualization for drivers
- **Empty-State Handling:**  
  Clear UX for cases where no matching vehicle is available,
  including waiting-time preferences and fallback suggestions
- **Cancellation Penalties:**  
  Fare-impact metrics for rider no-shows and late cancellations

---

## 🧾 What Was Corrected in This Final Version

- **Login Fee:** Corrected from monthly pricing to **₹30/day**, re-requested on date change.
- **Basket System:** Explicitly documented as the **core algorithmic primitive**.
- **Convenience Fee:** Clarified as **distance-based (e.g. per km)**.
- **Speed Guarantee:** Campus-level ~2-minute arrival treated as a technical requirement,
  not a marketing claim.

---

## 📌 Project Status

The UI and product logic are finalized for **Stage-1**.  
The system is now **production-ready** for backend implementation
(matching, routing, pooling, and driver-side flows).