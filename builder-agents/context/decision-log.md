# Decision Log

*Running record of significant product, technical, and design decisions made during the Pawprint build. Maintained by the Chief of Staff agent. Each entry captures what was decided, what was considered, why this was chosen, and what assumption it rests on.*

---

## How to Read This Log

Each entry follows this structure:
- **Decision** — what was decided, in one sentence
- **Alternatives considered** — what else was on the table
- **Why this** — the reason this option was chosen
- **Assumption** — what needs to be true for this to hold
- **Revisit if** — the condition that would cause us to reopen this

---

## Decisions

---

### D001 — Dogs only for MVP
**Date:** Pre-build
**Decision:** MVP is scoped to dogs only. No cats, birds, or other pets.
**Alternatives considered:** All pets from the start; dogs + cats
**Why this:** Dogs are the primary category for most pet retailers and the lifecycle events are more clearly defined. Cats and other pets introduce enough variation that they would dilute the MVP signal.
**Assumption:** The core loop (signal → email) is the same regardless of pet type; dogs are sufficient to prove it.
**Revisit if:** A major lifecycle event for cats emerges as a clear high-value case before MVP ships.

---

### D002 — One lifecycle event for MVP (first-time puppy owner)
**Date:** Pre-build
**Decision:** MVP is built around a single lifecycle event: first-time pet owner, new puppy.
**Alternatives considered:** Two events (new puppy + rescue adoption); all 13 events
**Why this:** One event forces clarity. It's also the highest-signal event — the customer's need is urgent, the content is well-defined, and the email has an obvious through-line.
**Assumption:** If the loop works for this event, it works for others. The architecture generalizes.
**Revisit if:** The first-time puppy owner case turns out to be an outlier (e.g., signal is too obvious to be realistic).

---

### D003 — Post-chat processing, not real-time detection
**Date:** Pre-build
**Decision:** Pawprint processes the transcript after the support chat closes, not during the conversation.
**Alternatives considered:** Real-time agent intervention during the chat
**Why this:** Post-chat is significantly simpler to build and sufficient to prove the concept. Real-time detection introduces latency, error-handling, and live chat integration complexity that is not necessary for MVP.
**Assumption:** A 24-48 hour email delay is still timely enough to feel relevant to the customer.
**Revisit if:** Testing reveals that the email arriving after the chat feels disconnected or too late.

---

### D004 — Email is the MVP delivery channel
**Date:** Pre-build
**Decision:** The personalized care package is delivered by email only.
**Alternatives considered:** SMS, in-app notification, combination
**Why this:** Email is the right format for longer-form curated content. SMS is too brief. In-app assumes the customer is actively using the retailer's app, which cannot be assumed for a first-time buyer.
**Assumption:** Elizabeth checks email regularly and it is her expected channel for this type of content.
**Revisit if:** Email open rates in testing are low enough to suggest the channel assumption is wrong.

---

### D005 — Builder agent team: Product Manager, Staff Engineer, Devil's Advocate, Chief of Staff
**Date:** 2026-06-14
**Decision:** Four builder agents to support the founder during the build. No Demo Director.
**Alternatives considered:** Adding a Demo Director agent; adding a User Proxy as a separate agent
**Why this:** The Demo Director was cut because product decisions should not be driven by demo considerations — the demo is a byproduct of a good feature. The User Proxy function is folded into the Product Manager's mandate (Elizabeth stays in the room through them).
**Assumption:** Four agents with clean lanes are more useful than five with overlapping concerns.
**Revisit if:** The PM agent is not surfacing the customer perspective clearly enough in practice.

---

*Add new decisions as they are made. Do not delete superseded decisions — mark them with a note and link to the decision that replaced them.*
