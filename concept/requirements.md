# Requirements — Refy System

The requirements are derived from user research, personas (Philip & Christof), and behavioral insights collected during the research phase.

They translate qualitative findings into functional system behavior and interaction constraints.

The goal is not only to define system functionality, but to reflect how design decisions support emotional awareness in financial decision-making.

---

## Design Context

The system is designed for two contrasting user types:

- **Philip** — impulsive, emotion-driven spending behavior
- **Christof** — structured, planning-oriented financial behavior

Both personas highlight the need for increased financial awareness, but differ in motivation, goals, and interaction patterns.

This leads to a system that must support both:

- reflective behavior change
- structured financial planning

---

## Functional Requirements

### FR1 — Track Expenses with Emotional Context

Users can record financial transactions and optionally assign an emotional state to each entry.

This supports:

- reflection on emotional spending behavior
- identification of patterns between mood and purchases
- increased awareness of non-rational financial decisions

---

### FR2 — Mark Impulse Purchases

Users can mark individual expenses as impulse purchases.

The system uses this information to:

- highlight repeated impulsive behavior over time
- provide contextual feedback in future financial views
- support behavioral self-reflection

---

### FR3 — Time-Based Financial Overview

Users can view past and upcoming expenses in a calendar-based interface.

This enables:

- temporal understanding of spending behavior
- comparison between planned and actual expenses
- improved awareness of financial patterns over time

---

### FR4 — Financial Forecasting

Users can access budget and spending forecasts based on historical data.

This feature supports:

- anticipation of future financial states
- reflection on long-term spending patterns
- planning-oriented financial behavior

---

## Non-Functional Requirements

### System Responsiveness

System feedback (e.g. warnings, confirmations, updates) must be displayed within 2 seconds.

This ensures immediate user awareness and maintains a smooth interaction flow.

---

### Transparency of Predictions

Financial forecasts should be understandable and interpretable for users.

The system should avoid black-box behavior and instead support users in understanding how predictions are generated.

---

### Usability & Clarity

Core interactions (expense entry, overview, navigation) must remain understandable without prior training.

The system should support users with varying levels of financial literacy and experience.

---

## Delighter Requirements (Begeisterungsfaktoren)

### Emotional Feedback System (Philip)

A visual representation of financial behavior (e.g. a mascot reacting to spending patterns).

Purpose:

- increase user engagement
- support emotional reflection
- make abstract financial data more tangible and intuitive

---

### Shared Financial Overview (Christof)

Users can optionally link multiple accounts (e.g. partners or family members) to view shared financial data.

Purpose:

- support household budgeting
- increase financial transparency in shared contexts
- enable collaborative financial planning

---

## Design Principle

Financial data is not treated as purely numerical information, but as behaviorally and emotionally contextualized information.

The system prioritizes reflection over optimization, supporting users in understanding _why_ they spend money rather than only _how much_ they spend.
