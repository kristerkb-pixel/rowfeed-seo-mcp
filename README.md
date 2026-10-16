# Rowfeed Search & Market Data – MCP tools for ChatGPT brand visibility, Google search, news, Amazon, App Store, company jobs, keyword volume and Google Trends

Ten pay-per-use data tools for AI agents, served as a remote MCP server through Apify.
Licensed data (DataForSEO's Google SERP, Amazon, Google Ads and ranking data) plus Google News' public feeds, Apple's public App Store feeds and companies' public job boards. No blocked runs.

| Tool | What it returns | Price |
|---|---|---|
| [AI Search Visibility Tracker](https://apify.com/rowfeed/ai-search-visibility-tracker) | Asks ChatGPT and Google AI Mode your prompts: is your brand mentioned, its position versus competitors, cited sources and the full answer | $0.04 per answer ($0.03 until 31 Oct 2026) |
| [Google Search Results API](https://apify.com/rowfeed/google-serp-api) | Google results for any query, country, language and device: organic, ads, featured snippet, People Also Ask, AI overview, local pack, and your domain's rank | $3 per 1,000 searches |
| [Google News Monitor](https://apify.com/rowfeed/google-news-monitor) | Google News articles for any query or topic in any edition: headline, source, time and publisher URL; monitor mode returns only new articles | $1 per 1,000 articles ($2 from 30 Oct 2026) |
| [Amazon Product Tracker](https://apify.com/rowfeed/amazon-product-tracker) | Amazon search results (rank, price, rating, ratings count, badges, sponsored) and product details per ASIN (price, discount, Best Sellers Rank) on any marketplace | $1 per 1,000 products + $0.005 per ASIN detail |
| [Google Shopping Prices](https://apify.com/rowfeed/google-shopping-prices) | Google Shopping results for any product search: price, old price and discount, seller, rating, delivery and rank, with seller tracking | $1 per 1,000 products + $0.002 per search |
| [Apple App Store Scraper](https://apify.com/rowfeed/apple-app-store-scraper) | App Store top charts (free, paid, grossing, iPad, new) for any country and category, App Store search and app details: rank, developer, price, rating, ratings count, version | $1 per 1,000 apps |
| [Career Site Jobs Scraper](https://apify.com/rowfeed/career-site-jobs-scraper) | Open jobs from company career sites on Greenhouse, Lever, Ashby, Workday and SmartRecruiters, with filters and a monitor mode for new jobs | $1 per 1,000 jobs |
| [Keyword Search Volume](https://apify.com/rowfeed/keyword-search-volume) | Monthly Google search volume, CPC, competition and 12-month trend for a keyword list, or keyword ideas from seed words | $3 per 1,000 keywords + $0.04 per lookup of up to 100 ($0.16 for a batch of up to 1,000) |
| [Competitor Keywords](https://apify.com/rowfeed/competitor-keywords) | Every Google keyword a domain ranks for: position, URL, volume, CPC, difficulty, intent, estimated traffic, plus a domain summary | $2 per 1,000 keywords + $0.02 per domain lookup |
| [Google Trends Explorer](https://apify.com/rowfeed/google-trends-explorer) | Google Trends interest over time for up to 5 compared keywords, with average, peak, latest value and trend | $0.001 per keyword + $0.02 per lookup of up to 5 |

Failed lookups are never charged. Each run also costs $0.001 to start.

## Connect (remote MCP, streamable HTTP)

Server URL:

```
https://mcp.apify.com?tools=rowfeed/google-serp-api,rowfeed/ai-search-visibility-tracker,rowfeed/google-news-monitor,rowfeed/amazon-product-tracker,rowfeed/google-shopping-prices,rowfeed/apple-app-store-scraper,rowfeed/career-site-jobs-scraper,rowfeed/keyword-search-volume,rowfeed/competitor-keywords,rowfeed/google-trends-explorer
```

Authenticate with your own Apify API token (free account at [apify.com](https://apify.com)), either via OAuth in clients that support it, or as a header:

```json
{
  "mcpServers": {
    "rowfeed-data": {
      "url": "https://mcp.apify.com?tools=rowfeed/google-serp-api,rowfeed/ai-search-visibility-tracker,rowfeed/google-news-monitor,rowfeed/amazon-product-tracker,rowfeed/google-shopping-prices,rowfeed/apple-app-store-scraper,rowfeed/career-site-jobs-scraper,rowfeed/keyword-search-volume,rowfeed/competitor-keywords,rowfeed/google-trends-explorer",
      "headers": { "Authorization": "Bearer <YOUR_APIFY_TOKEN>" }
    }
  }
}
```

Works in Claude Desktop, Claude Code, Cursor, VS Code and any client that speaks remote MCP. Usage is billed per event to your Apify account; you can cap the cost of every run. Live lookups on the paid-data tools need a paid Apify plan (any plan).

## Example questions for your agent

- "Search Google for 'best crm for startups' in the UK and tell me where hubspot.com ranks."
- "Any news about Nvidia in the last hour? Give me the article links."
- "What are the top 20 Amazon results for 'standing desk' and their prices?"
- "Which engineering jobs did Stripe and OpenAI post this week?"
- "What is the monthly search volume and CPC of these 200 keywords in Germany?"
- "Which Google keywords bring the most traffic to competitor.com, first page only?"
- "Compare Google Trends interest in iphone, samsung galaxy and google pixel over the last 12 months."

## About

Built and maintained by [Rowfeed](https://apify.com/rowfeed). Not affiliated with Google, Semrush or Ahrefs.
