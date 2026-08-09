# Architecture

## Components
- **ManyChat:** Instagram triggers, DM scenarios, branching, fields and tags.
- **Make:** webhooks, integration, routing and booking-event handling.
- **Google Sheets:** lightweight lead/conversation state and booking data.
- **Cal.com:** scheduling and booking.

## End-to-end flow
`Instagram → ManyChat → Make → Google Sheets → routing → Cal.com → Make → Google Sheets`

The trigger/scenario supplies the entry context; no separate AI context-recognition layer is required.
