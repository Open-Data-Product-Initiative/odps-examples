
# How to use ODPS spec with LLMs.txt?

An ODPS spec file is an excellent source for generating an LLMs.txt file. The ODPS (Open Data Product Specification) YAML contains structured, machine-readable metadata on access methods, pricing, SLA, data quality, API specs, and licensing — all of which are key inputs for creating a clear and informative LLMs.txt.

Since LLMs.txt is designed to help AI models understand and interact with your API or data product, pulling details from ODPS ensures accuracy and completeness

This guide helps you set up a `llms.txt` to enhance AI agent and LLM interaction with your API or website.

## What is `llms.txt`?

`llms.txt` is a structured file that gives LLMs (Large Language Models) essential information about how to interact with your APIs, datasets, or documentation. It helps automate integrations, testing, and AI-driven discovery.

## 📝 What to include

- **Purpose**: Summary of what the API or dataset offers.
- **Authentication**: Methods like Bearer Token, API Key, OAuth.
- **Input/Output**: Formats (e.g., JSON, YAML) and example payloads.
- **Usage limits**: Rate limits, query caps, pricing cues.
- **Examples**: Sample queries and expected responses.

## Where to place

Host `llms.txt` at your domain root:
```
https://dataproduct.com/llms.txt
```
AI agents and tools will discover it automatically.

## Example Snippet

In the below example we have used [ODPS Data product spec file](yaml/full-example.yml) as source. 

```
# LLMs.txt for UrbanPulse Events

## Purpose
Provides structured, real-time public event data for travel apps, tourism platforms, and smart city services.

## Auth
- Method: Bearer Token
- Example: Authorization: Bearer {token}

## Input Format
JSON MCP query with:
- eventType (string)
- location (string)
- dateRange (object: from, to)

## Output Format
JSON MCP response:
- eventID
- title
- location
- startTime
- endTime
- category

## Example Query
{
  "eventType": "concert",
  "location": "Abu Dhabi",
  "dateRange": { "from": "2025-07-01", "to": "2025-07-31" }
}

## Example Response
{
  "events": [
    { "eventID": "E123", "title": "Summer Beats", "location": "Louvre Abu Dhabi", "startTime": "2025-07-15T20:00", "endTime": "2025-07-15T23:00", "category": "concert" }
  ]
}

## Rate Limits
- Basic Reader: 100 queries/month
- Extended User: 1000 queries/month
- High Volume: 500,000 queries/month

```
