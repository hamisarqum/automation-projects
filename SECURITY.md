# Security Guidelines

Before publishing or sharing workflow exports:

1. Remove API keys, access tokens, passwords, and OAuth secrets.
2. Remove personal email addresses and customer information.
3. Replace Google Calendar, Google Sheets, and Google Drive resource IDs.
4. Remove webhook URLs and instance-specific metadata.
5. Store secrets in n8n credentials, Make.com connections, or environment variables.
6. Test imported workflows with non-production data before activation.

The included workflow files use `REPLACE_WITH_...` placeholders for values that must be configured after import.
