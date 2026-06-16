# Pawprint — Project Context for Claude Code

## What Pawprint Is

Pawprint is a multi-agent AI workflow for an online pet products retailer. It detects lifecycle signals embedded in customer support conversations — for example, a customer saying "I just got a new puppy" — and automatically generates a personalized email care package for that customer.

The application runs in a browser. During the workflow, every agent's reasoning and decisions are visible on screen in real time (no black boxes). At the end, the generated email renders in a clean, formatted view.

It is being built to solve a real customer problem first. A leadership demo and GitHub portfolio artifact are byproducts of a well-built feature — not design inputs. It is being built entirely using Claude Code by a non-technical product manager.

---

## Build Sequence

1. **Multi-agent workflow** — build and validate the agent logic first
2. **Chat interface** — browser-based UI with live agent thinking panel
3. **Polish** — final presentation layer; emerges from the feature, not the other way around

---

## Sample MVP Customer Journey — Elizabeth

**Customer:** Elizabeth. First-time pet owner. Golden retriever puppy. No prior relationship with the retailer.

**Trigger:** Places her first order (puppy food) and contacts customer care to ask about delivery status.

**Signal moment:** During the support chat she mentions *"this is my first puppy, my first pet ever."*

**What happens after the chat ends:**

| Step | What happens |
| --- | --- |
| Chat transcript saved | Stored in the database after the conversation closes |
| Agent 1 — Signal Detector | Reads the transcript, identifies lifecycle event: new puppy, first-time owner |
| Agent 2 — Content Curator | Pulls blog posts, top products, top-performing sponsored ad results |
| Email generated | Personalized email sent to Elizabeth |

This is the primary lifecycle event used in the MVP.

---

## What's Been Decided

- **Product brief written** — [Pawprint-Product-Brief-v1.md](./Pawprint-Product-Brief-v1.md) is the source of truth for the problem statement, goals, and constraints.
- **README created** — [README.md](./README.md) is live and written in a "building in public" style. It will be updated incrementally as decisions are made.
- **GitHub connected** — The project is live at `https://github.com/vtyagibuilds/careflow-pawprint`. All changes should be pushed after each session.
- **Pet scope** — Dogs only for MVP.
- **Planning sequence** — MVP customer journey → database design → agent architecture → tech stack.
- **Documentation approach** — Key design decisions captured in markdown files in the `/design` folder. Agent designs will live in an `/agents` folder, one file per agent.
- **Builder agent team assembled** — Four meta-agents created to help the founder build Pawprint: Product Manager, Staff Engineer, Devil's Advocate, Chief of Staff. Defined in `/builder-agents/`. Demo Director was considered and explicitly cut — product decisions are not driven by demo considerations.
- **Baseline context artifacts built** — Five documents created in `/builder-agents/context/` to give the builder agents what they need to operate: problem statement, MVP scope, Elizabeth's customer persona, assumptions log, decision log.

---

## Folder Structure

```
/design              ← blueprints and decisions (frameworks, mappings, what we're building and why)
/data                ← simulated retailer data (seeds the database when we start coding)
  /content-library   ← mock blog posts, tagged by lifecycle event
  /products          ← mock product catalog, tagged
  /customers         ← mock customer profiles
  /transcripts       ← mock chat transcripts (including Elizabeth's)
/agents              ← one file per agent, defined when we get to agent architecture (Pawprint workflow agents)
/builder-agents      ← meta-agents that help the founder build Pawprint; separate from the product agents
  /context           ← baseline artifacts the builder agents operate from
```

---

## Design Files (Source of Truth)

| File | What it tracks |
| --- | --- |
| [database-design-framework.md](./design/database-design-framework.md) | The ordered framework for designing the database. Status tracker included. |
| [lifecycle-events.md](./design/lifecycle-events.md) | All 13 lifecycle events across 4 categories. Needs mapping for Pet Parent Journey Milestones included. |

---

## Lifecycle Events (13 total, Dogs only)

Defined in full in [lifecycle-events.md](./design/lifecycle-events.md). Categories:

- **Pet Parent Journey Milestones** (6) — first-time owner new puppy, first-time owner rescue adoption, experienced pet owner, dog's birthday, moved to new home, new baby at home
- **Life Stage Transitions** (3) — puppy to adult, adult to senior, senior health concerns
- **Health Events** (2) — illness or injury, surgery or procedure
- **Loss & Grief** (2) — dog passed away, end of life care

---

## Categories of Owner Needs

These map directly to email components. Not all apply to every lifecycle event.

1. **Education & Information** — guides, articles, breed-specific info
2. **Product Recommendations** — essential purchases, curated lists
3. **Health & Wellness Guidance** — vet timing, nutrition, preventive care
4. **Training & Behavior** — obedience, house training, socialization
5. **Emotional Acknowledgment** — the human connection layer
6. **Action Checklist** — concrete next steps

---

## Database Design — Mental Model

Two distinct layers:

**Layer 1 — The Retailer's Assets** (defined once, shared across all milestones)
- Blog content library — categories, posts, tagged by lifecycle event relevance
- Product catalog — all products, tagged
- Sponsored ad results — tagged

**Layer 2 — The Milestone Logic** (per lifecycle event)
- Which blog content is relevant
- Which products to surface
- Which email components to include
- Tone and framing of the email

The agent sits between these two layers — it knows the active milestone, queries the retailer's assets using tags, and assembles the email.

---

## Content Library (Retailer Asset)

Defined in [content-library.md](./data/content-library/content-library.md).

**7 categories · 16 mock blog posts · all 13 lifecycle events covered**

| Category | What belongs here |
| --- | --- |
| Vet Care | Clinical and medical — vet visits, illness, surgery, symptoms |
| Food & Nutrition | Feeding, diet, ingredients, nutrition across life stages |
| Training & Behavior | Obedience, house training, behavioral guidance |
| Pet Parenting | Emotional and relational — the owner's journey, milestones, grief, celebration |
| New Dog | Practical, event-specific content about arrival and first days |
| Dog Breeds | Breed-specific personalization lens — agent uses when breed is known |
| Grooming | Coat care, bathing, brushing, nail trims across life stages |

Each post is tagged with lifecycle event relevance. Agents query by tag, not category. Dog Breeds posts are a personalization layer — they surface when the customer's breed is known (e.g. Elizabeth = golden retriever).

---

## Builder Agent Team

Four meta-agents that help the founder make good decisions throughout the build. These are separate from the Pawprint workflow agents. Defined in `/builder-agents/`.

| Agent | File | Mandate |
|---|---|---|
| Product Manager | [product-manager.md](./builder-agents/product-manager.md) | Are we solving the right problem? Keeps Elizabeth in the room. |
| Staff Engineer | [staff-engineer.md](./builder-agents/staff-engineer.md) | Are we building it the right way? Flags technical debt before it's created. |
| Devil's Advocate | [devils-advocate.md](./builder-agents/devils-advocate.md) | What are we missing? What's wrong? Invoked when confidence is high. |
| Chief of Staff | [chief-of-staff.md](./builder-agents/chief-of-staff.md) | What did we decide and why? Synthesizes decisions, maintains the log. |

**How to invoke:** Say "let me check with the Product Manager on this" or "what would the Devil's Advocate say here?" — the agent's definition file is loaded and that perspective is applied for the exchange.

**When to invoke:** For decisions that are hard to reverse — schema design, scope calls, content architecture. Not for small implementation details.

### Builder Agent Context Artifacts

Baseline documents the builder agents operate from. In `/builder-agents/context/`.

| File | What it is |
|---|---|
| [problem-statement.md](./builder-agents/context/problem-statement.md) | The customer problem, what we're solving, what we're not |
| [mvp-scope.md](./builder-agents/context/mvp-scope.md) | What's in v1, what's out, the test for adding scope |
| [customer-persona-elizabeth.md](./builder-agents/context/customer-persona-elizabeth.md) | Elizabeth — fully fleshed out, the MVP anchor persona |
| [customer-persona-template.md](./builder-agents/context/customer-persona-template.md) | Reusable template for the other 12 lifecycle events |
| [assumptions-log.md](./builder-agents/context/assumptions-log.md) | Named assumptions across signal detection, customer behavior, content, and tech |
| [decision-log.md](./builder-agents/context/decision-log.md) | Running record of all significant decisions, alternatives considered, and reasoning |

---

## Where We Are Now

Builder agent team assembled and context artifacts built. Database design is in progress (step 4 of 8). Content library is done. Next: define the **product catalog** as a retailer-level asset, then sponsored ad results, then return to each milestone to define what gets pulled.
