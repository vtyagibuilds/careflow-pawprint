# MVP Scope

## What MVP Must Prove

One thing: that a lifecycle signal detected from a support chat can produce a personalized email that feels genuinely relevant to the customer in that moment.

Not that it scales to 13 lifecycle events. Not that it works across channels. Not that it handles every edge case. Just that the core loop works — signal in, relevant email out — and that the output is good enough that a real customer would engage with it.

---

## What Is In MVP

| Capability | Detail |
|---|---|
| Lifecycle event | First-time puppy owner only |
| Signal source | Post-chat transcript (after support conversation closes) |
| Signal detection | Agent reads transcript, identifies lifecycle event |
| Content curation | Blog posts, product recommendations, sponsored ad results |
| Output | One personalized email per triggered customer |
| Delivery mechanism | Email only |
| Pet scope | Dogs only |
| Customer | Elizabeth — first-time pet owner, golden retriever puppy |

---

## What Is Deliberately Out of MVP

| Out of scope | Reason |
|---|---|
| All other 12 lifecycle events | Validate the core loop first; expanding before proving value is premature |
| Real-time detection (during chat) | Post-chat is simpler to build and sufficient to prove the concept |
| SMS, push, in-app | Email is the right channel for this type of content; multi-channel adds complexity without adding proof |
| Customer opt-in / preference management | Infrastructure concern; not relevant until the feature is proven |
| A/B testing email variants | Optimization comes after validation |
| Feedback loop (did the customer engage?) | Important long-term; not needed to prove the core concept |
| Non-dog pets | Scope creep; dogs are the primary category and sufficient for MVP |
| Customers who don't signal | Pawprint only acts on detected signals; inference is a future capability |
| Admin UI for managing content | Content is seeded manually in MVP; management tooling comes later |

---

## The MVP Success Condition

Elizabeth's transcript is processed. The correct lifecycle event is identified. An email is generated that:
- Acknowledges her specific moment (first-time puppy owner)
- Includes relevant blog content, product recommendations, and sponsored results
- Reads as personally relevant, not templated
- Would plausibly be opened and engaged with by a real person in her situation

If that works end-to-end, MVP is proven.

---

## What Moves Something From Out-of-Scope to In-Scope

A single question: does this need to exist for the core loop to work?

If the answer is no — if the loop functions without it — it's out of scope for MVP. Arguments about "it would be better with X" are not sufficient. The bar is necessity, not improvement.
