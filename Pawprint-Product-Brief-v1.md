# Project Brief: Pet Lifecycle Multi-Agent Workflow
### Claude Code Starter Document

---

## What I'm Building

A multi-agent AI workflow for an online pet products retailer that detects lifecycle signals from customer support conversations — such as a customer mentioning they just got a new puppy — and automatically generates a personalized email care package for new pet parents.

---

## Problem Statement

Customer support interactions are treated as isolated, transactional events. When a customer reaches out about an order, we resolve the issue and move on — missing richer signals embedded in the conversation. Phrases like "I just got a new puppy" reveal significant life moments that are an opportunity to deepen the relationship. Today, these signals go undetected and unacted upon.

---

## What I Want to Build

A browser-based application where:

1. **A customer has a support chat conversation** — the user types messages as a customer.
2. **A multi-agent workflow runs behind the scenes** — agents detect lifecycle signals, analyze the conversation, and decide whether to act. Each agent's reasoning and decisions must be visible on screen during the demo. No black boxes.
3. **A personalized email care package is generated** — displayed beautifully on screen at the end. This is the payoff moment of the demo.

---

## Critical Demo Requirements

**1. The thinking must be visible.** Leadership needs to see what the agents are doing — the reasoning, the handoffs, the decisions. This is the most important part of the demo.

**2. The final email must be displayed on screen.** At the end of the workflow, the generated care package email should render in a clean, formatted, readable way.

**3. The interface should run in a browser.** Not a terminal. A proper web-based chat UI that looks polished and professional for a leadership audience.

---

## Database & Retailer Data

This project simulates a real online pet products retailer. The agents will have access to a database containing the kind of information a real retailer would have — things like customer profiles, order history, product catalog, and anything else relevant to personalizing the experience. The agents will query this database to inform their decisions and make the email output genuinely personalized, not generic.

The database type and structure will be decided in collaboration with Claude Code — the goal is to keep it simple enough to run locally while being realistic enough to make the demo compelling.

---

## Personal Goals

1. **GitHub Portfolio** — The finished project will be uploaded to GitHub as a PM portfolio artifact showing hands-on technical capability.
2. **Leadership Demo** — A live demo showing the inner workings of the multi-agent system, with the goal of making the case to build this as a full in-house product feature.
3. **Built entirely using Claude Code** — No prior coding experience. Claude Code writes everything. I run it and provide product direction.

---

## Constraints

- Runs locally on a personal laptop
- No physical packages — the "care package" is an email displayed on screen (not actually sent)
- No existing codebase — starting from scratch
- Non-technical builder — Claude Code does the coding, I provide product direction

---

## Tech Stack

Let Claude Code decide the best approach. The only requirements are:

- Runs in a **browser** — a proper web-based chat interface, not a terminal
- Uses the **Anthropic API** (Claude) to power the agents
- Has a **live agent thinking panel** visible alongside the chat during the conversation
- Displays the **final email on screen** in a clean, formatted, readable way at the end of the workflow
- Keep dependencies minimal — this runs on a personal laptop with no server setup

---

## First Ask for Claude Code

> "Read this brief. We are going to plan and build a multi-agent pet lifecycle workflow that runs in a browser. Before we write any code, I want to first discuss and agree on three things in order: one, the database design — what data we simulate and how agents will query it; two, the agent design — how many agents, what each one does, and how they hand off to each other; three, the tech stack. Start by asking me the right questions about the database, then we will work through the rest."
