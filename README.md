# Sales Summarizer (n8n Workflow)
### Overview

This project helps sellers stay informed about their sales activity by automatically summarizing new or updated orders and sending the summary via email.

The automation is built using n8n and is powered by a free DeepSeek large language model. It monitors a Google Sheets sales list, generates a human-readable summary using AI, and delivers the result to a specified Gmail address.

This workflow is suitable for small sellers or teams who want lightweight, cost-effective sales awareness without complex dashboards.

![n8n Workflow](images/n8n-Workflow.png)

### How It Works

The workflow consists of three main nodes:

## 1. Google Sheets Trigger

Monitors a Google Sheets document containing sales data

Triggers the workflow when:

A new sale is added

An existing sale is updated or modified

Sends the sales row data to the AI agent for processing

## 2. Summarize (AI Agent)

Receives sales information from Google Sheets

Converts raw sales data into a clean, readable summary

Formats the output as:

Email Subject

Email Body

Powered by the following model:

deepseek/deepseek-r1-0528:free


⚠️ Note:
For more advanced automation, higher accuracy, or multi-agent reasoning, a more powerful (paid) AI model may be required.

## 3. Send Email

Sends the AI-generated summary to a specified Gmail address

Uses Gmail OAuth2 authentication

Ensures the sales team is immediately notified of new or updated orders
