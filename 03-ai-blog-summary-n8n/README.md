# AI Article Analysis and Blog Summary

## Overview

This n8n workflow reads article links from Google Sheets, sends them to an AI agent for structured analysis, and writes blog-style summaries back to Google Sheets.

## Workflow

1. Detect or retrieve article links from a Google Sheet.
2. Send each link to an OpenAI-powered AI agent.
3. Generate a headline, executive summary, takeaways, benefits, risks, market impact, long-term perspective, lessons, and final thought.
4. Generate a short image prompt related to the article.
5. Append the generated output to a blog sheet.

## Required services

- n8n
- OpenAI
- Google Sheets

## Setup

1. Import `workflow.json` into n8n.
2. Configure OpenAI and Google Sheets credentials.
3. Replace the spreadsheet placeholder.
4. Select the source and destination sheets.
5. Confirm the output mapping in the destination Google Sheets node.
6. Choose either the sheet trigger, schedule trigger, or a controlled combination.
7. Test with articles that are publicly accessible.

## Important review

Confirm that the AI agent has a supported method for retrieving article content from each URL. Also verify that the generated output is mapped into the destination `Blogs` column before activation.
