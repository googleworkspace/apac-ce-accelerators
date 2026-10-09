
# Gemini Workspace Studio & Apps Script PoC Starter


A sanitized, customer-ready **Pre-Sales PoC** starter demonstrating how to
connect a Google Forms / Google Sheets workflow to Google Chat and Gmail using
Apps Script during a 30-day Gemini for Google Workspace pilot.

## Prerequisites

1.  A Google Workspace test or pilot domain (`example-bank.com`).
2.  A Google Sheet with columns: `Request_ID`, `Submitter_Email`, `Summary`,
    `Status`.
3.  A Google Chat Space incoming webhook URL (stored in Apps Script
    `ScriptProperties`, never hardcoded).

## Sample Apps Script (`Code.gs`)

```javascript
// Copyright 2026 Google LLC
// SPDX-License-Identifier: Apache-2.0

/**
 * Posts a sanitized PoC triage notification card to a Google Chat webhook.
 * @param {string} requestId Unique PoC request identifier.
 * @param {string} summary AI-generated summary of the request.
 */
function notifyChatSpace(requestId, summary) {
  const webhookUrl = PropertiesService.getScriptProperties().getProperty('CHAT_WEBHOOK_URL');
  if (!webhookUrl) {
    throw new Error('Missing CHAT_WEBHOOK_URL in ScriptProperties.');
  }
  const payload = {
    text: `*PoC Request ${requestId}*\nSummary: ${summary}`
  };
  UrlFetchApp.fetch(webhookUrl, {
    method: 'post',
    contentType: 'application/json',
    payload: JSON.stringify(payload)
  });
}
```
