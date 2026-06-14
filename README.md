# Pawprint 🐾

> **A multi-agent AI workflow that detects lifecycle signals in customer support conversations and generates personalized email care packages — automatically.**

🚧 **Status: In Progress** — actively being designed and built using Claude Code.

---

## What This Is

When a customer contacts support and mentions something like *"I just got a new puppy,"* that's not just a support ticket — it's a life moment. Pawprint detects these signals in real time, runs a multi-agent workflow behind the scenes, and generates a personalized email care package tailored to that customer and their new pet.

The whole process — the agent reasoning, the handoffs, the decisions — is visible on screen as it happens. No black boxes.

---

## The Problem

Customer support interactions are treated as isolated, transactional events. We resolve the issue and move on — missing richer signals embedded in the conversation. Phrases like *"I just got a new puppy"* reveal significant life moments that are an opportunity to deepen the customer relationship.

Today, these signals go undetected and unacted upon. Pawprint is an attempt to change that.

---

## How It Works

```
1. Customer chats with support
        ↓
2. Multi-agent workflow runs in the background
   (reasoning and decisions visible on screen in real time)
        ↓
3. A personalized email care package is generated
   and displayed — tailored to this customer and their pet
```

---

## Agent Architecture

> 🔧 *Agents are currently being designed. This section will be updated as the architecture is finalized.*

**Design principle:** Every agent's reasoning and decisions are visible during the demo. Leadership should be able to see exactly what each agent is doing, why, and what it decided — in real time.

---

## Tech Stack

> 🔧 *Tech stack is currently being decided. This section will be updated once finalized.*

**Known constraints:**
- Runs in a browser (proper web UI, not a terminal)
- Powered by the [Anthropic API](https://www.anthropic.com/) (Claude)
- Minimal dependencies — runs locally on a personal laptop

---

## Project Status

- [x] Product brief written
- [ ] Demo scenario defined
- [ ] Database schema designed
- [ ] Agent architecture designed
- [ ] Tech stack decided
- [ ] App built
- [ ] Demo tested and recorded

---

## About This Project

Pawprint is being built as both a **leadership demo** — making the case for this as a full in-house product feature at an online pet retailer — and a **GitHub portfolio artifact** showing hands-on technical capability.

It is being built entirely using [Claude Code](https://www.anthropic.com/claude-code) by a non-technical product manager. No prior coding experience. Claude Code writes everything; I provide product direction.

---

*Built with Claude Code · Powered by the Anthropic API*
