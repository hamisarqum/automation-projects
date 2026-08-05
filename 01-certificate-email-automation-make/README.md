# Certificate Email Automation

## Overview

This Make.com scenario automates certificate delivery from a Google Sheets awardee list.

## Workflow

1. Read one awardee row from Google Sheets.
2. Create a personalized certificate from a Google Slides template.
3. Email the certificate to the awardee through Gmail.
4. Update the tracking sheet after the email is sent.

## Required services

- Make.com
- Google Sheets
- Google Slides
- Google Drive
- Gmail

## Setup

1. Import `workflow.blueprint.json` into Make.com.
2. Reconnect all Google modules.
3. Select your awardee spreadsheet and sheet.
4. Select your certificate template and output folder.
5. Confirm the template fields for name, email, and date.
6. Review the final Google Sheets status-column mapping.
7. Test with one sample row before scheduling the scenario.
