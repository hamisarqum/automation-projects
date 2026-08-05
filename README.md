# Automation Projects

A portfolio of workflow automation projects built with n8n, Make.com, OpenAI, Google Workspace, and the Pexels API.

## Projects

| Project | Platform | Main integrations |
|---|---|---|
| Certificate Email Automation | Make.com | Google Sheets, Google Slides, Gmail |
| AI Appointment Booking | n8n | OpenAI, Google Calendar, Google Sheets |
| AI Blog Summary | n8n | OpenAI, Google Sheets |
| Pexels Image Automation | n8n | OpenAI, Pexels API, Google Drive, Google Sheets |

## Repository structure

```text
automation-projects/
|-- 01-certificate-email-automation-make/
|   |-- README.md
|   `-- workflow.blueprint.json
|-- 02-ai-appointment-booking-n8n/
|   |-- README.md
|   `-- workflow.json
|-- 03-ai-blog-summary-n8n/
|   |-- README.md
|   `-- workflow.json
|-- 04-pexels-image-automation-n8n/
|   |-- README.md
|   `-- workflow.json
|-- SECURITY.md
`-- README.md
```

## Import instructions

### n8n

1. Open n8n.
2. Select Workflows.
3. Select Import from File.
4. Choose the required `workflow.json`.
5. Configure credentials and replace all `REPLACE_WITH_...` values.
6. Test the workflow before activating it.

### Make.com

1. Create or open a scenario.
2. Select Import Blueprint.
3. Choose `workflow.blueprint.json`.
4. Reconnect Google services and select your own Sheets, Slides, Drive, and Gmail resources.
5. Test the scenario before scheduling it.

## Security

The workflow exports in this repository are sanitized for public sharing. They do not include usable API keys or account credentials. Personal Google resource IDs, email addresses, webhook IDs, and instance metadata were removed or replaced with placeholders.

Never commit real API keys, OAuth tokens, passwords, or private customer data.
