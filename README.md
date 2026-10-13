# Rowfeed SEO Data – MCP tools for keyword volume, competitor keywords and Google Trends

Three pay-per-use SEO data tools for AI agents, served as a remote MCP server through Apify.
Licensed data (Google Ads Keyword Planner figures and DataForSEO's Google ranking database), no scraping, no blocked runs.

| Tool | What it returns | Price |
|---|---|---|
| [Keyword Search Volume](https://apify.com/rowfeed/keyword-search-volume) | Monthly Google search volume, CPC, competition and 12-month trend for a keyword list, or keyword ideas from seed words | $3 per 1,000 keywords + $0.12 per lookup of up to 1,000 |
| [Competitor Keywords](https://apify.com/rowfeed/competitor-keywords) | Every Google keyword a domain ranks for: position, URL, volume, CPC, difficulty, intent, estimated traffic, plus a domain summary | $2 per 1,000 keywords + $0.02 per domain lookup |
| [Google Trends Explorer](https://apify.com/rowfeed/google-trends-explorer) | Google Trends interest over time for up to 5 compared keywords, with average, peak, latest value and trend | $0.003 per keyword + $0.02 per lookup |

Keywords without data and failed lookups are never charged.

## Connect (remote MCP, streamable HTTP)

Server URL:

```
https://mcp.apify.com?tools=rowfeed/keyword-search-volume,rowfeed/competitor-keywords,rowfeed/google-trends-explorer
```

Authenticate with your own Apify API token (free account at [apify.com](https://apify.com)), either via OAuth in clients that support it, or as a header:

```json
{
  "mcpServers": {
    "rowfeed-seo": {
      "url": "https://mcp.apify.com?tools=rowfeed/keyword-search-volume,rowfeed/competitor-keywords,rowfeed/google-trends-explorer",
      "headers": { "Authorization": "Bearer <YOUR_APIFY_TOKEN>" }
    }
  }
}
```

Works in Claude Desktop, Claude Code, Cursor, VS Code and any client that speaks remote MCP. Usage is billed per event to your Apify account; you can cap the cost of every run.

## Example questions for your agent

- "What is the monthly search volume and CPC of these 200 keywords in Germany?"
- "Which Google keywords bring the most traffic to competitor.com, first page only?"
- "Compare Google Trends interest in iphone, samsung galaxy and google pixel over the last 12 months."

## About

Built and maintained by [Rowfeed](https://apify.com/rowfeed). Not affiliated with Google, Semrush or Ahrefs.
