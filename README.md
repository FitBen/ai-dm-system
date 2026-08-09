# AI DM Qualification System

> A no-code Instagram DM automation case study focused on conversational qualification, structured data capture and routing.

## Overview

This repository documents a working Instagram DM prototype built primarily with **ManyChat, Make, Google Sheets and Cal.com**.

The system does not rely on a separate AI context-recognition layer. Context is mainly established by the trigger and by which ManyChat scenario is launched. The workflow guides the conversation, captures structured information, sends data through Make, updates Google Sheets, and routes the prospect toward the appropriate next step.

## Architecture

![AI DM Qualification System Architecture](assets/architecture-final.png)

### Core stack

- **ManyChat** — Instagram triggers, DM flows, scenario branching, fields and tags
- **Make** — automation, webhooks, data routing and updates
- **Google Sheets** — lightweight lead/conversation database and status tracking
- **Cal.com** — booking layer for qualified prospects and booking-status events

### High-level flow

```text
Instagram CTA / comment
        ↓
ManyChat trigger
        ↓
Relevant ManyChat scenario
        ↓
Conversation / qualification
        ↓
Make automation
        ↓
Google Sheets / workflow state
        ↓
Routing / next step
        ↓
Cal.com booking when appropriate
```

Possible next steps include continuing the conversation, sending a resource, moving toward a demo or call, or handing the conversation to a human.

## Real workflow

### ManyChat flow

![ManyChat flow](screenshots/manychat-flow.png)

### Make scenario

![Make scenario](screenshots/make-flow.png)

### Google Sheets data layer

![Google Sheets](screenshots/google-sheets.png)

## Conversation demo

The repository also includes anonymized conversation examples and a short screen recording of the working DM flow.

- [Conversation screenshot 1](conversations/conversation-1-anonymized.jpg)
- [Conversation screenshot 2](conversations/conversation-2-anonymized.jpg)
- [Conversation screenshot 3](conversations/conversation-3-anonymized.jpg)
- [Watch the anonymized conversation demo](conversations/conversation-demo-anonymized.mp4)

These files are kept separate so the README stays easy to scan while the full interaction remains available to reviewers.

## Design principles

1. **Conversation before conversion** — do not treat a CTA comment as an automatic request for a booking link.
2. **One useful question at a time** — qualification should feel conversational rather than form-like.
3. **Use deterministic context where possible** — the trigger/scenario already provides useful context.
4. **Store useful answers as structured data** — fields, tags and spreadsheet records make routing testable.
5. **Automation should support the conversation** — the objective is the right next step, not automation for its own sake.

## Repository structure

```text
docs/
  architecture.md
  qualification-logic.md
  conversation-design.md
  data-flow.md
  testing-and-iteration.md
  lessons-learned.md
  before-vs-after.md
  future-improvements.md
  demo-video-script.md

examples/
  anonymized-conversations.md

assets/
  architecture-final.png

screenshots/
  manychat-flow.png
  make-flow.png
  google-sheets.png

conversations/
  conversation-1-anonymized.jpg
  conversation-2-anonymized.jpg
  conversation-3-anonymized.jpg
  conversation-demo-anonymized.mp4
```

## Skills demonstrated

- No-code AI / automation prototyping
- Workflow architecture
- ManyChat scenario design
- Make automation
- Cal.com booking integration
- Webhook-based integration
- Structured data handling
- Conversational UX
- Lead qualification logic
- Testing and iteration
- Translating a business problem into a working prototype

## Privacy

The public repository intentionally excludes credentials, webhook secrets, API keys and identifiable prospect data. Conversation examples and screenshots have been anonymized for portfolio use.

## Status

**Working prototype / portfolio case study**

This project is intentionally documented as a no-code system rather than presented as a custom-coded application.
