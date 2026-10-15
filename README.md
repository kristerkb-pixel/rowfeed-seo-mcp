# Rowfeed SEO Data – MCP tools for Google search results, news, keyword volume, competitor keywords and Google Trends

Five pay-per-use search data tools for AI agents, served as a remote MCP server through Apify.
Licensed data (DataForSEO's Google SERP, Google Ads and ranking data) plus Google News' public feeds. No blocked runs.

| Tool | What it returns | Price |
|---|---|---|
| [Google Search Results API](https://apify.com/rowfeed/google-serp-api) | Google results for any query, country, language and device: organic, ads, featured snippet, People Also Ask, AI overview, local pack, and your domain's rank | $4 per 1,000 searches |
| [Google News Monitor](https://apify.com/rowfeed/google-news-monitor) | Google News articles for any query or topic in any edition: headline, source, time and publisher URL; monitor mode returns only new articles | $1 per 1,000 articles |
| [Keyword Search Volume](https://apify.com/rowfeed/keyword-search-volume) | Monthly Google search volume, CPC, competition and 12-month trend for a keyword list, or keyword ideas from seed words | $3 per 1,000 keywords + $0.12 per lookup of up to 1,000 |
| [Competitor Keywords](https://apify.com/rowfeed/competitor-keywords) | Every Google keyword a domain ranks for: position, URL, volume, CPC, difficulty, intent, estimated traffic, plus a domain summary | $2 per 1,000 keywords + $0.02 per domain lookup ($0.04 from 30 Oct 2026) |
| [Google Trends Explorer](https://apify.com/rowfeed/google-trends-explorer) | Google Trends interest over time for up to 5 compared keywords, with average, peak, latest value and trend | $0.003 per keyword + $0.02 per lookup |

Failed lookups are never charged. Each run also costs $0.001 to start.

## Connect (remote MCP, streamable HTTP)

Server URL:

```
https://mcp.apify.com?tools=rowfeed/google-serp-api,rowfeed/google-news-monitor,rowfeed/keyword-search-volume,rowfeed/competitor-keywords,rowfeed/google-trends-explorer
```

Authenticate with your own Apify API token (free account at [apify.com](https://apify.com)), either via OAuth in clients that support it, or as a header:

```json
{
  "mcpServers": {
    "rowfeed-seo": {
      "url": "https://mcp.apify.com?tools=rowfeed/google-serp-api,rowfeed/google-news-monitor,rowfeed/keyword-search-volume,rowfeed/competitor-keywords,rowfeed/google-trends-explorer",
      "headers": { "Authorization": "Bearer <YOUR_APIFY_TOKEN>" }
    }
  }
}
```

Works in Claude Desktop, Claude Code, Cursor, VS Code and any client that speaks remote MCP. Usage is billed per event to your Apify account; you can cap the cost of every run. Live lookups on the paid-data tools need a paid Apify plan (any plan).

## Example questions for your agent

- "Search Google for 'best crm for startups' in the UK and tell me where hubspot.com ranks."
- "Any news about Nvidia in the last hour? Give me the article links."
- "What is the monthly search volume and CPC of these 200 keywords in Germany?"
- "Which Google keywords bring the most traffic to competitor.com, first page only?"
- "Compare Google Trends interest in iphone, samsung galaxy and google pixel over the last 12 months."

## About

Built and maintained by [Rowfeed](https://apify.com/rowfeed). Not affiliated with Google, Semrush or Ahrefs.
