# AI Pexels Image Search and Google Drive Archive

## Overview

This n8n workflow accepts a chat request, searches Pexels for matching images, downloads the returned images, uploads them to Google Drive, and stores metadata in Google Sheets.

## Workflow

1. Receive an image-search request through chat.
2. Use an AI agent to call the Pexels search API.
3. Extract image links from the agent output.
4. Loop through the image links.
5. Download each image.
6. Upload each image to Google Drive.
7. Store the search query and image link in Google Sheets.

## Required services

- n8n
- OpenAI
- Pexels API
- Google Drive
- Google Sheets

## Setup

1. Import `workflow.json` into n8n.
2. Configure the OpenAI, Google Drive, and Google Sheets credentials.
3. Replace the Pexels API key placeholder.
4. Replace the spreadsheet and Drive folder placeholders.
5. Confirm the HTTP response format and image-link extraction logic.
6. Test the workflow with a simple search query before activation.

## Important review

The link extraction code expects Markdown image links in the AI agent output. Add error handling for empty or differently formatted responses before production use.
