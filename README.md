# AdCrunch MCP Server

[![smithery badge](https://smithery.ai/badge/adcrunch/adcrunch)](https://smithery.ai/servers/adcrunch/adcrunch)

**Ask AI about your ads.** AdCrunch is a remote [MCP](https://modelcontextprotocol.io) server that connects **Meta Ads, TikTok Ads, and Google Ads** to Claude and ChatGPT — query campaign setup and performance in natural language, no dashboards needed.

- **Server URL:** `https://mcp.adcrunch.dev/mcp` (streamable HTTP, OAuth)
- **Website:** [adcrunch.dev](https://adcrunch.dev?utm_source=github&utm_medium=directory)
- **Docs:** [docs.adcrunch.dev](https://docs.adcrunch.dev)
- **Security:** read-only access to your ad platforms by default; credentials are never exposed to the AI model.

> Free during early access — no credit card. [Pricing](https://adcrunch.dev/?utm_source=github&utm_medium=directory#pricing).

## Connect

### Claude (claude.ai / Claude Desktop)

Settings → **Connectors** → **Add custom connector** → `https://mcp.adcrunch.dev/mcp`, then authorize with your AdCrunch account.

### ChatGPT

Settings → **Connectors** → **Add custom connector** → `https://mcp.adcrunch.dev/mcp`.

Full per-client guides: [docs.adcrunch.dev](https://docs.adcrunch.dev).

## Tools

Every tool, with its inputs and its outputs, is in the [tool reference](https://docs.adcrunch.dev/mcp?utm_source=github&utm_medium=directory).

## Example questions

- "Which campaign had the best ROAS in the last 30 days?"
- "Compare TikTok vs Meta spend efficiency for the last 14 days"
- "Which ad set has the highest CPA this month — and show its creative"

---

This repository hosts documentation for connecting to the AdCrunch MCP server. The service itself is hosted at [adcrunch.dev](https://adcrunch.dev).
