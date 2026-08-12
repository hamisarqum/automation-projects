# AI Article Analysis and Blog Summary

## Overview

This n8n workflow demonstrates trigger-based AI content analysis using article links from Google Sheets. It sends each link into a structured analysis prompt and writes the generated blog-style output back to Google Sheets.

## Workflow

1. Detect or retrieve article links from a Google Sheet.
2. Send each link to an OpenAI-powered AI agent.
3. Generate a headline, executive summary, takeaways, benefits, risks, market impact, long-term perspective, lessons, and final thought.
4. Generate a short image prompt related to the article.
5. Append the generated output to a blog sheet.

## Required Services

- n8n
- OpenAI
- Google Sheets

## Setup

1. Import `workflow.json` into n8n.
2. Configure OpenAI and Google Sheets credentials.
3. Replace `REPLACE_WITH_SPREADSHEET_ID`.
4. Select the source and destination sheets.
5. Configure a supported method for retrieving article content from each URL.
6. Map the generated AI output into the destination `Blogs` column.
7. Choose either the sheet trigger, schedule trigger, or a controlled combination.
8. Test with publicly accessible articles before activation.

## Current Export Note

The current workflow sends the article URL to the AI agent but does **not** include a dedicated HTTP request, scraping, or article-content extraction tool. A language model should not be assumed to have automatically read the linked webpage.

Before production use, add a content-retrieval step and pass the retrieved article text into the analysis prompt. Also confirm that the AI output is explicitly mapped into the destination Google Sheets column.

The spreadsheet resource is represented by a placeholder, and no usable account credentials are included in the public export.
