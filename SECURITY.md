# Security Guidelines

Before publishing or sharing workflow exports:

1. Remove API keys, access tokens, passwords, OAuth secrets, and credential IDs that identify private accounts.
2. Remove personal email addresses, customer information, and production data.
3. Replace Google Calendar, Google Sheets, Google Drive, and other private resource IDs with placeholders.
4. Remove webhook URLs, instance URLs, execution data, and instance-specific metadata that is not needed for import.
5. Configure secrets through n8n credentials, Make.com connections, or environment variables instead of hardcoding them in workflow nodes.
6. Keep local `.env`, n8n state, credential exports, private keys, and secret files outside version control.
7. Test imported workflows with non-production data before activation.
8. Re-check exported JSON files before every public commit because workflow platforms may include resource metadata during export.

The workflow files in this repository use `REPLACE_WITH_...` placeholders for environment-specific values that must be configured after import.

If a real credential is ever committed, removing it from the latest file is not enough. Revoke or rotate the credential and clean the Git history if necessary.
