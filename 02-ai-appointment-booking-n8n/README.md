# Conversational AI Appointment Booking

## Overview

This n8n workflow provides a chat-based appointment booking assistant with conversation memory.

## Workflow

1. Receive a customer message through the n8n chat trigger.
2. Collect the customer's name, phone number, date, and preferred time.
3. Validate weekday and business-hour rules.
4. Check Google Calendar availability for the full one-hour slot.
5. Create the calendar event when the slot is available.
6. Save appointment information in Google Sheets.
7. Return a concise confirmation to the customer.

## Required services

- n8n
- OpenAI
- Google Calendar
- Google Sheets

## Setup

1. Import `workflow.json` into n8n.
2. Configure the OpenAI credential.
3. Configure Google Calendar and Google Sheets credentials.
4. Replace the calendar and spreadsheet placeholders.
5. Confirm the workflow timezone.
6. Create the required Google Sheets columns.
7. Test available, unavailable, weekend, past-date, and failure scenarios before activation.

## Important review

The agent instructions describe Name, Phone, Date, Start Time, End Time, Status, and Calendar Event ID fields. Confirm that the Google Sheets node maps every required field before production use.
