# Lifecycle Events Map

## Overview

This file is the evolving map of lifecycle events that Pawprint detects from customer support conversations. Each event represents a meaningful moment in a dog owner's journey that triggers a personalized outreach.

**Scope:** Dogs only (MVP)
**Detection method:** Multi-agent workflow reads chat transcripts and identifies signals

---

## Lifecycle Events

### Pet Parent Journey Milestones

| Event | Description |
|---|---|
| First-time pet owner, new puppy | No prior pet experience. Just got a puppy. |
| First-time pet owner, rescue adoption | No prior pet experience. Adopted from a shelter or rescue. |
| Experienced pet owner | Has owned pets before. Adding or transitioning to a new dog. |
| Dog's birthday | Owner mentions the dog's birthday, or derivable from pet profile. |
| Moved to a new home | Owner mentions relocating. New environment for the dog. |
| New baby at home | Owner mentions introducing dog to a newborn. |

### Life Stage Transitions

| Event | Description |
|---|---|
| Puppy to adult | Dog transitioning out of puppyhood (~12 months depending on breed). |
| Adult to senior | Dog entering senior years (~7 years depending on breed). |
| Senior health concerns | Owner mentions joint issues, mobility challenges, or diet changes. |

### Health Events

| Event | Description |
|---|---|
| Illness or injury | Dog is sick or recovering from an injury. |
| Surgery or procedure | Dog is post-op or preparing for a procedure. |

### Loss & Grief

| Event | Description |
|---|---|
| Dog passed away | Owner mentions losing their dog. |
| End of life care | Dog is in final stages. Owner may need palliative or comfort products. |

---

## Event Count

| Category | Events |
|---|---|
| Pet Parent Journey Milestones | 6 |
| Life Stage Transitions | 3 |
| Health Events | 2 |
| Loss & Grief | 2 |
| **Total** | **13** |

---

## Demo Scenario

**Elizabeth** — First-time pet owner, new puppy (golden retriever).
This is the primary lifecycle event used in the MVP leadership demo.

---

---

## Categories of Owner Needs

These categories define what an owner needs at a given lifecycle moment. They translate directly into components of the outreach email. Not all categories apply to all events.

| # | Category | Description |
|---|---|---|
| 1 | Education & Information | What do I need to know? Guides, articles, tips, breed-specific info. |
| 2 | Product Recommendations | What do I need to buy? Essential purchases, curated lists. |
| 3 | Health & Wellness Guidance | How do I keep my dog healthy? Vet timing, nutrition, preventive care. |
| 4 | Training & Behavior | How do I shape my dog's behavior? Obedience, house training, socialization. |
| 5 | Emotional Acknowledgment | You see me and this moment matters. The human connection layer. |
| 6 | Action Checklist | What should I actually do right now? Concrete next steps. |

---

## Pet Parent Journey Milestones — Needs Mapping

| Category | First-Time Owner, New Puppy | First-Time Owner, Rescue Adoption | Experienced Pet Owner | Dog's Birthday | Moved to New Home | New Baby at Home |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| Education & Information | ✅ | ✅ | ⚠️ | ❌ | ✅ | ✅ |
| Product Recommendations | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Health & Wellness Guidance | ✅ | ✅ | ⚠️ | ❌ | ⚠️ | ⚠️ |
| Training & Behavior | ✅ | ✅ | ⚠️ | ❌ | ⚠️ | ✅ |
| Emotional Acknowledgment | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Action Checklist | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ |

**Key:** ✅ Always applies — ⚠️ Situational — ❌ Doesn't apply

**Category notes by event:**
- **First-time owner, new puppy** — All categories apply fully. Highest education and checklist need of any event.
- **First-time owner, rescue adoption** — Same as new puppy but with more emphasis on behavioral unknowns and settling-in guidance.
- **Experienced pet owner** — Light touch. Skip education and checklist. Lead with products and emotional acknowledgment.
- **Dog's birthday** — Celebratory only. Products (treats, toys, gifts) and emotional acknowledgment. No guidance needed.
- **Moved to new home** — Transition-focused. Education and checklist are high priority. Health and training are situational (stress, anxiety).
- **New baby at home** — Dual celebration and practical need. Strong on training (dog-baby introduction), education (safety, boundaries), and action checklist. Health is situational (stress signals in the dog).

---

## What's Next (To Be Filled In)

- Needs mapping for remaining lifecycle categories (Life Stage Transitions, Health Events, Loss & Grief)
- For each event: specific products, content, and email components
- Agent mapping — which agent handles detection and response per event
