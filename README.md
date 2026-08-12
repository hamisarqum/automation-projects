# Workflow Automation Portfolio

## Overview

This repository contains reusable workflow automation projects built with n8n and Make.com. The projects demonstrate AI-assisted workflows, Google Workspace automation, appointment scheduling, content processing, API integration, file handling, and automated email delivery.

The exported workflows are sanitized for public portfolio use. Credentials, private resource IDs, personal email addresses, and API keys are not included.

## Projects

| Project | Platform | Integrations | What it demonstrates |
|---|---|---|---|
| [Certificate Email Automation](01-certificate-email-automation-make/) | Make.com | Google Sheets, Google Slides, Google Drive, Gmail | Reads awardee data, creates personalized certificates, sends email, and updates tracking data |
| [AI Appointment Booking](02-ai-appointment-booking-n8n/) | n8n | OpenAI, Google Calendar, Google Sheets | Conversational data collection, scheduling rules, calendar availability checks, event creation, and appointment logging |
| [AI Article Analysis](03-ai-blog-summary-n8n/) | n8n | OpenAI, Google Sheets | Structured AI content analysis, summarization prompts, trigger-based processing, and spreadsheet output |
| [Pexels Image Automation](04-pexels-image-automation-n8n/) | n8n | OpenAI, Pexels API, Google Drive, Google Sheets | API-based image search, link extraction, file download, Drive upload, and metadata logging |

## Automation Skills Demonstrated

- n8n workflow design and node orchestration
- Make.com scenario development
- AI agents and prompt-driven workflow logic
- REST API integration
- Google Sheets automation
- Google Calendar availability and event creation
- Google Drive file handling
- Gmail-based delivery workflows
- Trigger, schedule, loop, and branching patterns
- Workflow credential sanitization for public sharing

## Repository Structure

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

## Importing the Workflows

### n8n

1. Open n8n and go to **Workflows**.
2. Select **Import from File**.
3. Import the required `workflow.json`.
4. Configure your own OpenAI and Google credentials where required.
5. Replace all `REPLACE_WITH_...` resource placeholders.
6. Review node mappings and workflow timezone settings.
7. Test the workflow with non-production data before activation.

### Make.com

1. Create or open a Make.com scenario.
2. Select **Import Blueprint**.
3. Import `workflow.blueprint.json`.
4. Reconnect the required Google services.
5. Select your own Sheets, Slides, Drive folders, and Gmail account.
6. Review field mappings and test with a sample record before scheduling the scenario.

## Implementation Notes

These exports are portfolio templates and require environment-specific configuration after import.

- **Appointment Booking:** The current Google Sheets export maps `Name`, `Phone number`, and `Date/time`. The agent instructions describe additional appointment fields, so complete the destination-sheet mapping before production use.
- **Article Analysis:** The current workflow passes an article URL to the AI agent but does not include a dedicated article-content retrieval node. Add a supported HTTP/content extraction step before treating it as a production article-reading workflow.
- **Pexels Image Automation:** The link extraction step expects Markdown image links from the agent output. Production use should include handling for empty or differently formatted responses.

These notes are also documented inside the individual project folders.

## Security

The workflow exports use placeholders such as:

```text
REPLACE_WITH_SPREADSHEET_ID
REPLACE_WITH_GOOGLE_CALENDAR_ID
REPLACE_WITH_GOOGLE_DRIVE_FOLDER_ID
REPLACE_WITH_PEXELS_API_KEY
```

Do not replace these placeholders with real secrets in files that will be committed to GitHub. Configure API keys, OAuth connections, and credentials inside n8n or Make.com whenever possible.

See [SECURITY.md](SECURITY.md) for the repository security checklist.

## Contact

**Muhammad Hamis Arqum**

[LinkedIn Profile](https://www.linkedin.com/in/hamis-arqum/)
