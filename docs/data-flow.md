# Data Flow

## ManyChat → Make

ManyChat can send captured fields and state to Make through webhook-based automation.

## Make → Google Sheets

Make writes or updates structured records in Google Sheets.

The data layer can include items such as:

- platform
- contact identifiers
- conversation state
- qualification status
- booking ID
- email
- user notes
- next action
- call-booked status
- booking timestamps
- created/modified timestamps

## Why Google Sheets?

For this prototype, a spreadsheet is transparent, easy to inspect and quick to modify.

It makes debugging easier because the workflow state can be inspected without building a custom database interface.

## Cal.com booking flow

For qualified prospects, the workflow can route toward a **Cal.com** booking page.

The booking layer is part of the system rather than an external afterthought:

```text
Qualified prospect
      ↓
Cal.com booking link
      ↓
Booking event
      ↓
Make
      ↓
Google Sheets status / booking fields updated
```

This allows booking state to remain visible in the same lightweight data layer used by the rest of the prototype.
