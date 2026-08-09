# Architecture

## System components

### 1. Instagram entry point
A prospect interacts with CTA-based content.

### 2. ManyChat trigger
ManyChat detects the relevant interaction and launches the corresponding DM scenario.

### 3. ManyChat conversation flow
The scenario contains the conversational steps, branching logic, questions, fields and tags needed for that entry point.

### 4. Make automation
Make receives data from the workflow, transforms or routes it, and coordinates updates between connected services.

### 5. Google Sheets
Google Sheets acts as a lightweight structured data layer for lead status, conversation-related fields and booking-related state.

### 6. Routing / next step
Based on captured information and workflow state, the system can continue the conversation, provide a resource, move toward a demo/call or leave the case for human follow-up.

## Context handling

There is no separate AI context-recognition service in the current architecture.

Context is primarily deterministic: the trigger and scenario define why the conversation started. This is simpler, easier to test and more reliable for a prototype than asking a model to infer context that the system already knows.

## Architecture philosophy

Use the simplest reliable component for each job.

ManyChat handles Instagram and conversational flow. Make handles integration and orchestration. Google Sheets provides transparent structured storage.

The architecture can later evolve if scale, complexity or maintainability creates a concrete reason to introduce custom code.

## Booking layer

When a prospect reaches the appropriate stage, the workflow can send a **Cal.com** booking link. Booking events can then be written back through the automation layer so the lead record reflects whether a call was booked and includes relevant booking state.

This closes the loop between qualification and the real-world conversion event rather than treating the booking link as the end of the automation.
