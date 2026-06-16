# Database Design Framework for Pawprint

## Purpose

This file is the evolving framework for designing the Pawprint database. The database simulates a real online pet products retailer. Agents query it to detect lifecycle signals and generate personalized email outreach.

---

## The Framework (In Order)

### 1. Pet Type
What animal are we supporting?
**Decided: Dog (MVP)**

---

### 2. Lifecycle Events
What moments in a dog's life (or owner's life) are we trying to detect?
**Decided: 13 events across 4 categories.**
See [`lifecycle-events.md`](lifecycle-events.md) for the full map.

---

### 3. Per Lifecycle Event — What Does the Owner Need?
For each lifecycle event, what products, content, and guidance is relevant?
This determines what the email contains, and therefore what data the agents need to pull.
**In progress — starting with First-time owner, new puppy.**

---

### 4. Product Catalog
What products does the retailer sell?
Scoped by lifecycle event — not just "all dog products" but what a specific owner needs at a specific moment.
**To be defined.**

---

### 5. Content Library
What non-product content does the retailer have?
Blog posts, care guides, how-to articles — the educational layer of the email.
**To be defined.**

---

### 6. Customer Data
What do we know about the customer?
Profile, order history, pet info (breed, age, name if captured), communication preferences.
**To be defined.**

---

### 7. Behavioral & Engagement Data
What signals from other customers inform the recommendations?
Most bought products for new puppy owners, most clicked sponsored ads, most read blog posts.
**To be defined.**

---

### 8. The Email Output
What does the final email need to contain?
Reverse-engineer this to validate that everything above is sufficient to generate it.
**To be defined.**

---

## Status

| Step | Status |
|---|---|
| 1. Pet type | ✅ Done |
| 2. Lifecycle events | ✅ Done |
| 3. Owner needs per event | 🔄 In progress |
| 4. Product catalog | ⏳ Not started |
| 5. Content library | ⏳ Not started |
| 6. Customer data | ⏳ Not started |
| 7. Behavioral & engagement data | ⏳ Not started |
| 8. Email output | ⏳ Not started |
