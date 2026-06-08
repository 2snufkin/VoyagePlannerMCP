# Pyrenees Trip Planner Agent

This folder is set up for an AI travel-planning workflow for a Pyrenees hike starting near Hendaye, with flexible dates between 14 and 20 July 2026 and a maximum of 20 km per walking day.

The planner is intended to use MCP browser/scraping tools:

- Playwright MCP: navigate unfamiliar websites, click, fill date forms, inspect pages.
- Firecrawl MCP: extract readable Markdown/text from pages when browser interaction is not needed.
- Optional Browserbase MCP: use a hosted browser for longer or more reliable remote sessions.

The expected output is a Markdown itinerary with each stage, distance, elevation, sleeping option, availability, price, booking/contact link, and source confidence.

## Recommended MCP Servers

### Playwright MCP

Use this for interactive sites, booking forms, maps, and pages the agent has never seen before.

```powershell
npx @playwright/mcp@latest
```

### Firecrawl MCP

Use this for extracting clean page content. It requires a Firecrawl API key.

```powershell
npx -y firecrawl-mcp
```

Set:

```powershell
$env:FIRECRAWL_API_KEY="your_key_here"
```

### Browserbase MCP, Optional

Use this if you want the browser to run in the cloud instead of locally. It requires Browserbase credentials.

## How To Use

1. Configure the MCP servers in your AI client using one of the example files in `mcp/`.
2. Give the agent the prompt in `prompts/pyrenees-planner.md`.
3. Ask it to write the final result to `itineraries/pyrenees-hendaye-2026.md`.

## Important Notes

Accommodation availability and prices are time-sensitive. The final Markdown should always include:

- source URL
- date checked
- whether availability was confirmed online or inferred
- whether a manual email/phone confirmation is still needed

