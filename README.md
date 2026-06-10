# AdCrunch MCP Server

**Ask AI about your ads.** AdCrunch is a remote [MCP](https://modelcontextprotocol.io) server that connects **Meta Ads, TikTok Ads, and Google Ads** to AI agents like Claude, ChatGPT, and Cursor — query campaign setup and performance in natural language, no dashboards needed.

- **Server URL:** `https://mcp.adcrunch.dev/mcp` (streamable HTTP, OAuth)
- **Website:** [adcrunch.dev](https://adcrunch.dev?utm_source=github&utm_medium=directory)
- **Docs:** [docs.adcrunch.dev](https://docs.adcrunch.dev)
- **Security:** read-only access to your ad platforms by default; credentials are never exposed to the AI model.

> Free during early access — no credit card. [Pricing](https://adcrunch.dev/?utm_source=github&utm_medium=directory#pricing).

## Connect

### Claude (claude.ai / Claude Desktop)

Settings → **Connectors** → **Add custom connector** → `https://mcp.adcrunch.dev/mcp`, then authorize with your AdCrunch account.

### Cursor

Add to your MCP settings (`.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "adcrunch": {
      "url": "https://mcp.adcrunch.dev/mcp"
    }
  }
}
```

### ChatGPT

Settings → **Connectors** → **Add custom connector** → `https://mcp.adcrunch.dev/mcp`.

Full per-client guides: [docs.adcrunch.dev](https://docs.adcrunch.dev).

## Tools

| Tool | What it does |
|---|---|
| `list_advertisers` | Connected ad accounts across platforms |
| `list_campaigns` | Campaigns for an advertiser |
| `list_ad_groups` | Ad-group structure |
| `list_ads` | Individual ads |
| `query_insights` | Time-series performance: spend, ROAS, CPA, impressions, clicks, conversions |
| `search_ads` | Search ad creative |
| `skill_list` / `skill_get` | Discover and fetch your org's reusable ad-ops playbooks |
| `skill_create` / `skill_update` / `skill_delete` | Author and maintain playbooks (Skills store) |

## Example questions

- "Which campaign had the best ROAS in the last 30 days?"
- "Compare TikTok vs Meta spend efficiency for the last 14 days"
- "Which ad set has the highest CPA this month — and show its creative"

---

This repository hosts documentation for connecting to the AdCrunch MCP server. The service itself is hosted at [adcrunch.dev](https://adcrunch.dev).
