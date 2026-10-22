# Rowfeed Search & Market Data – MCP tools for ChatGPT brand visibility, Google search, Google Ads, Google Maps rankings and business data, Google Hotels prices, website traffic and authority, backlinks, news, Amazon, App Store, company jobs, keyword volume and Google Trends

Seventeen pay-per-use data tools for AI agents, served as a remote MCP server through Apify.
Licensed data (DataForSEO's Google SERP, Amazon, Google Ads and ranking data) plus Google News' public feeds, Apple's public App Store feeds and companies' public job boards. No blocked runs.

| Tool | What it returns | Price |
|---|---|---|
| [AI Search Visibility Tracker](https://apify.com/rowfeed/ai-search-visibility-tracker) | Asks ChatGPT and Google AI Mode your prompts: is your brand mentioned, its position versus competitors, cited sources and the full answer | $0.04 per answer ($0.03 until 31 Oct 2026) |
| [Google Search Results API](https://apify.com/rowfeed/google-serp-api) | Google results for any query, country, language and device: organic, ads, featured snippet, People Also Ask, AI overview, local pack, and your domain's rank | $3 per 1,000 searches |
| [Google News Monitor](https://apify.com/rowfeed/google-news-monitor) | Google News articles for any query or topic in any edition: headline, source, time and publisher URL; monitor mode returns only new articles | $1 per 1,000 articles ($2 from 30 Oct 2026) |
| [Amazon Product Tracker](https://apify.com/rowfeed/amazon-product-tracker) | Amazon search results (rank, price, rating, ratings count, badges, sponsored) and product details per ASIN (price, discount, Best Sellers Rank) on any marketplace | $1 per 1,000 products + $0.005 per ASIN detail |
| [Google Shopping Prices](https://apify.com/rowfeed/google-shopping-prices) | Google Shopping results for any product search: price, old price and discount, seller, rating, delivery and rank, with seller tracking | $1 per 1,000 products + $0.002 per search |
| [Apple App Store Scraper](https://apify.com/rowfeed/apple-app-store-scraper) | App Store top charts (free, paid, grossing, iPad, new) for any country and category, App Store search and app details: rank, developer, price, rating, ratings count, version | $1 per 1,000 apps |
| [Google Jobs Scraper](https://apify.com/rowfeed/google-jobs-api) | Google Jobs listings for any search and location: title, employer, location, salary, job type, posted date and apply link, with date and job-type filters and a monitor mode | $2 per 1,000 jobs + $0.002 per 10 jobs requested |
| [Google Ads Transparency & Ad Library](https://apify.com/rowfeed/google-ads-transparency) | Every ad a domain or advertiser runs on Google Search, YouTube, Play, Maps and Shopping from the Google Ads Transparency Center: advertiser, format, preview image, first and last shown; advertiser search by name and a monitor mode for new ads | $1 per 1,000 ads + $0.001 per 40 ads requested |
| [Local Rank Tracker](https://apify.com/rowfeed/google-maps-rank-tracker) | Google Maps rank of a business at every point of a geo-grid around it (3x3 to 9x9): rank per point, the top 3 there, average rank, top-3 share and the competitors that beat it | $0.004 per grid point |
| [Google Maps Scraper](https://apify.com/rowfeed/google-maps-scraper) | Every business Google Maps shows for a search in any city or around coordinates: name, category, address, phone, website, rating, reviews, opening hours and place id, up to 700 per search, with rating, reviews, website and phone filters | $2 per 1,000 places + $0.001 per search per 100 places asked for |
| [Google Hotels API](https://apify.com/rowfeed/google-hotels-api) | Google Hotels prices for any city and dates: price per night, stars, rating, reviews and discounts, plus each hotel's prices on every booking site (Booking.com, Expedia, the official site) | $2 per 1,000 hotels + $0.004 per hotel for booking-site prices |
| [Website Traffic Checker](https://apify.com/rowfeed/website-traffic-checker) | Bulk website traffic and domain authority for up to 10,000 domains: Google organic and paid traffic estimate, ranking keywords, domain rank, referring domains and backlinks | $4 per 1,000 domains + $0.12 per batch of up to 1,000 |
| [Backlinks Checker](https://apify.com/rowfeed/backlink-checker) | Backlinks of any site or page: referring domains, linking pages, anchor text, dofollow, domain and page strength, spam score, first and last seen; strongest first, up to 10,000 per site | $1 per 1,000 backlinks + $0.04 per lookup of up to 1,000 |
| [Career Site Jobs Scraper](https://apify.com/rowfeed/career-site-jobs-scraper) | Open jobs from company career sites on Greenhouse, Lever, Ashby, Workday and SmartRecruiters, with filters and a monitor mode for new jobs | $1 per 1,000 jobs |
| [Keyword Search Volume](https://apify.com/rowfeed/keyword-search-volume) | Monthly Google search volume, CPC, competition and 12-month trend for a keyword list, or keyword ideas from seed words | $3 per 1,000 keywords + $0.04 per lookup of up to 100 ($0.16 for a batch of up to 1,000) |
| [Competitor Keywords](https://apify.com/rowfeed/competitor-keywords) | Every Google keyword a domain ranks for: position, URL, volume, CPC, difficulty, intent, estimated traffic, plus a domain summary | $2 per 1,000 keywords + $0.02 per domain lookup |
| [Google Trends Explorer](https://apify.com/rowfeed/google-trends-explorer) | Google Trends interest over time for up to 5 compared keywords, with average, peak, latest value and trend | $0.001 per keyword + $0.02 per lookup of up to 5 |

Failed lookups are never charged. Each run also costs $0.001 to start.

## Connect (remote MCP, streamable HTTP)

Server URL:

```
https://mcp.apify.com?tools=rowfeed/google-serp-api,rowfeed/ai-search-visibility-tracker,rowfeed/google-news-monitor,rowfeed/amazon-product-tracker,rowfeed/google-shopping-prices,rowfeed/apple-app-store-scraper,rowfeed/google-jobs-api,rowfeed/google-ads-transparency,rowfeed/google-maps-rank-tracker,rowfeed/google-maps-scraper,rowfeed/google-hotels-api,rowfeed/website-traffic-checker,rowfeed/backlink-checker,rowfeed/career-site-jobs-scraper,rowfeed/keyword-search-volume,rowfeed/competitor-keywords,rowfeed/google-trends-explorer
```

Authenticate with your own Apify API token (free account at [apify.com](https://apify.com)), either via OAuth in clients that support it, or as a header:

```json
{
  "mcpServers": {
    "rowfeed-data": {
      "url": "https://mcp.apify.com?tools=rowfeed/google-serp-api,rowfeed/ai-search-visibility-tracker,rowfeed/google-news-monitor,rowfeed/amazon-product-tracker,rowfeed/google-shopping-prices,rowfeed/apple-app-store-scraper,rowfeed/google-jobs-api,rowfeed/google-ads-transparency,rowfeed/google-maps-rank-tracker,rowfeed/google-maps-scraper,rowfeed/google-hotels-api,rowfeed/website-traffic-checker,rowfeed/backlink-checker,rowfeed/career-site-jobs-scraper,rowfeed/keyword-search-volume,rowfeed/competitor-keywords,rowfeed/google-trends-explorer",
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
