# Conversational AI Appointment Booking

## Overview

This n8n workflow demonstrates a chat-based appointment booking assistant with conversation memory, scheduling rules, Google Calendar availability checks, event creation, and Google Sheets logging.

## Workflow

1. Receive a customer message through the n8n chat trigger.
2. Collect the customer's name, phone number, date, and preferred time.
3. Validate weekday and business-hour rules.
4. Check Google Calendar availability for the full one-hour slot.
5. Create the calendar event when the slot is available.
6. Save appointment information in Google Sheets.
7. Return a concise confirmation to the customer.

## Required Services

- n8n
- OpenAI
- Google Calendar
- Google Sheets

## Setup

1. Import `workflow.json` into n8n.
2. Configure the OpenAI credential.
3. Configure Google Calendar and Google Sheets credentials.
4. Replace `REPLACE_WITH_GOOGLE_CALENDAR_ID` and `REPLACE_WITH_SPREADSHEET_ID`.
5. Confirm the workflow timezone.
6. Create the required Google Sheets columns.
7. Complete the destination-sheet field mapping.
8. Test available, unavailable, weekend, past-date, and failure scenarios before activation.

## Current Export Note

The AI agent instructions describe these appointment fields:

- Name
- Phone
- Date
- Start Time
- End Time
- Status
- Calendar Event ID

The current exported Google Sheets node maps only `Name`, `Phone number`, and `Date/time`. Complete the remaining field mapping after import before using the workflow in production.

The calendar ID and spreadsheet ID are placeholders, and no usable account credentials are included in the public export.
