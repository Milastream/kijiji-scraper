[Kijiji Scraper](https://apify.com/automation-lab/kijiji-scraper?fpr=data)

## What does Kijiji Canada Scraper do?

**Kijiji Canada Scraper** extracts classified listings from [Kijiji.ca](https://www.kijiji.ca), Canada's largest online classifieds marketplace. Scrape **real estate rentals, cars and trucks, buy & sell items, jobs, services, and pets** from any city or province in Canada.

The scraper uses **pure HTTP requests** (no browser), making it fast and cost-effective. It parses Kijiji's structured data directly, extracting **titles, prices, descriptions, images, seller info, location coordinates, and category-specific attributes** (bedrooms, mileage, condition, etc.).

Try it now — click **Start** with the prefilled input to scrape Toronto apartment listings.

## Who is Kijiji Canada Scraper for?

🏠 **Real estate investors and property managers**

- Monitor rental prices across Canadian cities
- Track new apartment and condo listings in real time
- Analyze rental market trends by neighbourhood

🚗 **Car dealers and buyers**

- Track used car prices by make, model, and location
- Find underpriced vehicles before competitors
- Build a database of dealer inventory across provinces

📊 **Market researchers and data analysts**

- Analyze pricing trends for consumer goods across Canada
- Study regional demand patterns for different product categories
- Build datasets for machine learning or reporting

🛍️ **Resellers and deal hunters**

- Find deals on electronics, furniture, and collectibles
- Set up automated monitoring for specific keywords
- Compare prices across different Canadian cities

💼 **Recruiters and HR teams**

- Monitor job postings across industries in Canada
- Track salary ranges and hiring trends by location
- Analyze competitor job listings

## Why use Kijiji Canada Scraper?

- ⚡ **Fast and affordable** — pure HTTP scraper, no browser overhead. Scrape 100 listings for ~$0.30
- 🔄 **Schedule and automate** — run on a daily/weekly schedule to monitor new listings
- 📋 **Rich structured data** — prices, coordinates, seller info, and all category-specific attributes
- 🌍 **All of Canada** — any city, province, or category on Kijiji.ca
- 🔗 **API access** — integrate with Google Sheets, Slack, Zapier, Make, and 5,000+ apps
- 📦 **Multiple export formats** — JSON, CSV, Excel, XML, HTML
- 🔑 **No login or API key needed** — scrapes public listing data only
- 🖼️ **Full-size images** — automatically upgrades thumbnail URLs to high-resolution versions

## What data can you extract from Kijiji?

Each listing includes these fields:

| Field | Type | Description |
| --- | --- | --- |
| `adId` | string | Unique Kijiji listing ID |
| `title` | string | Listing title |
| `description` | string | Full listing description |
| `price` | string | Display price ("$1,200.00", "Free", "Please Contact") |
| `priceAmount` | number | Numeric price in CAD (null if not applicable) |
| `currency` | string | Always "CAD" |
| `category` | string | Listing category (e.g., "Cars & Trucks", "Apartments & Condos") |
| `location` | string | City or area name |
| `address` | string | Street address (when available) |
| `latitude` | number | GPS latitude |
| `longitude` | number | GPS longitude |
| `postedDate` | string | Date the listing was posted (ISO format) |
| `url` | string | Direct link to the listing |
| `imageUrls` | array | High-resolution image URLs |
| `sellerName` | string | Seller display name |
| `sellerType` | string | Seller type (Owner, Dealer) |
| `adType` | string | Ad type (ORGANIC, TOP_AD) |
| `attributes` | object | Category-specific attributes (bedrooms, mileage, year, etc.) |
| `scrapedAt` | string | Timestamp when the data was extracted |

### Category-specific attributes examples

🏠 **Real estate**: bedrooms, bathrooms, unit type, parking, pet-friendly, laundry, air conditioning, move-in date

🚗 **Cars**: year, make, model, mileage, transmission, drivetrain, fuel type, body type, colour, number of seats

🛍️ **Buy & Sell**: condition, brand, model

## How much does it cost to scrape Kijiji?

This actor uses **pay-per-event** pricing — you only pay for what you scrape. No monthly subscription. All platform costs are **included**.

|  | Free | Starter ($29/mo) | Scale ($199/mo) | Business ($999/mo) |
| --- | --- | --- | --- | --- |
| **Per listing** | $0.00345 | $0.003 | $0.00234 | $0.0018 |
| **100 listings** | $0.35 | $0.30 | $0.23 | $0.18 |
| **1,000 listings** | $3.45 | $3.00 | $2.34 | $1.80 |

Higher-tier plans get additional volume discounts.

**Real-world cost examples:**

| Query | Listings | Duration | Cost (Free tier) |
| --- | --- | --- | --- |
| Toronto apartments (20 listings with details) | 20 | ~30s | ~$0.07 |
| Honda Civic search across Canada (50 listings) | 50 | ~15s | ~$0.18 |
| Buy & sell electronics Ottawa (100 listings) | 100 | ~25s | ~$0.35 |

On the free plan ($5 credits), you can scrape approximately **1,400 listings**.

## How to scrape Kijiji listings

1. Go to the [Kijiji Canada Scraper](https://apify.com/automation-lab/kijiji-scraper) page on Apify Store
2. Click **Start** to try with prefilled Toronto apartment listings
3. Or customize your search:

- Paste a Kijiji URL directly into **Kijiji URLs**
- Or use **Search keywords**, **Category**, and **Location** to build a query
4. Set **Max listings** to control how many results to scrape
5. Enable **Include full details** for complete descriptions and attributes
6. Click **Start** and wait for results
7. Download your data as JSON, CSV, Excel, or connect via API

### Example: Scrape Toronto car listings

```
{
    "category": "cars-vehicles",
    "location": "city-of-toronto",
    "maxListings": 50,
    "includeDetails": true
}
```

### Example: Search for specific items

```
{
    "searchQuery": "macbook pro",
    "category": "buy-sell",
    "location": "vancouver",
    "maxListings": 30,
    "includeDetails": false
}
```

### Example: Scrape from a direct URL

```
{
    "startUrls": [
        { "url": "https://www.kijiji.ca/b-jobs/city-of-toronto/c45l1700273" }
    ],
    "maxListings": 100,
    "includeDetails": true
}
```

## Input parameters

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| `startUrls` | array | — | Direct Kijiji search or category page URLs |
| `searchQuery` | string | — | Keywords to search for |
| `category` | string | All | Category filter (buy-sell, cars-vehicles, real-estate, jobs, services, pets, community, vacation-rentals) |
| `location` | string | — | Location slug from Kijiji URLs (e.g., city-of-toronto, vancouver, alberta) |
| `maxListings` | integer | 100 | Maximum number of listings to extract (1-5000) |
| `includeDetails` | boolean | true | Fetch detail pages for full descriptions and attributes |

## Output example

```
{
    "adId": "1734239942",
    "title": "1, 2 AND 3 BEDROOM APARTMENTS AVAILABLE",
    "description": "ONE MONTH FREE RENT PROMO! Welcome to Royal Palace Apartments...",
    "price": "$1,700.00",
    "priceAmount": 1700,
    "currency": "CAD",
    "category": "Apartments & Condos",
    "location": "Toronto",
    "address": "3827 Lawrence Ave E, Scarborough, ON",
    "latitude": 43.76837,
    "longitude": -79.29991,
    "postedDate": "2026-03-10T14:40:15.000Z",
    "url": "https://www.kijiji.ca/v-apartments-condos/city-of-toronto/1-2-and-3-bedroom-apartments-available/1734239942",
    "imageUrls": [
        "https://media.kijiji.ca/api/v1/ca-prod-fsbo-ads/images/39/391a8292-a3aa-4e3c-ba29-2c1fe7090ed0?rule=kijijica-960-jpg"
    ],
    "sellerName": null,
    "sellerType": null,
    "adType": "TOP_AD",
    "attributes": {
        "Unit Type": "Apartment",
        "Bedrooms": "1",
        "Bathrooms": "1",
        "Pet Friendly": "Yes",
        "Parking Included": "Yes",
        "Agreement Type": "1 Year"
    },
    "scrapedAt": "2026-03-30T05:30:00.000Z"
}
```

## Tips for best results

- 🎯 **Start small** — use the prefilled input (20 listings) to test before running large jobs
- 📍 **Use specific locations** — narrow by city for more relevant results. Find location slugs in Kijiji URLs
- 🔍 **Combine search + category** — search within a category for more targeted results
- ⏱️ **Skip details for speed** — disable "Include full details" when you only need titles and prices. This is ~3x faster
- 📅 **Schedule daily runs** — set up a recurring schedule to monitor new listings automatically
- 💰 **Optimize costs** — without detail pages, scraping is cheaper and faster. Use detail pages only when you need full descriptions
- 🔗 **Use direct URLs** — paste Kijiji search URLs with filters (price range, sort order) already applied for precise results

## Integrations

🔄 **Kijiji to Google Sheets** — export rental listings to a spreadsheet for market analysis. Set up a daily schedule to track new apartments in your target neighbourhood.

📱 **Kijiji to Slack/Discord** — get instant alerts when new listings matching your criteria appear. Perfect for deal hunting or competitive monitoring.

⚡ **Kijiji to Zapier/Make** — build automated workflows: new car listing appears → check price against your budget → send notification → add to database.

📊 **Scheduled monitoring** — run the scraper on a daily schedule and compare datasets to identify new listings, price changes, and removed ads.

🔗 **Webhooks** — trigger your own API endpoint when scraping completes for real-time data processing.

## Using the Apify API

### Node.js

```
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: 'YOUR_API_TOKEN' });

const run = await client.actor('automation-lab/kijiji-scraper').call({
    category: 'real-estate',
    location: 'city-of-toronto',
    maxListings: 100,
    includeDetails: true,
});

const { items } = await client.dataset(run.defaultDatasetId).listItems();
console.log(items);
```

### Python

```
from apify_client import ApifyClient

client = ApifyClient('YOUR_API_TOKEN')

run = client.actor('automation-lab/kijiji-scraper').call(run_input={
    'category': 'real-estate',
    'location': 'city-of-toronto',
    'maxListings': 100,
    'includeDetails': True,
})

items = client.dataset(run['defaultDatasetId']).list_items().items
print(items)
```

### cURL

```
curl -X POST "https://api.apify.com/v2/acts/automation-lab~kijiji-scraper/runs?token=YOUR_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "category": "cars-vehicles",
    "location": "vancouver",
    "maxListings": 50,
    "includeDetails": true
  }'
```

## Use with AI agents via MCP

Kijiji Canada Scraper is available as a tool for AI assistants that support the [Model Context Protocol (MCP)](https://docs.apify.com/platform/integrations/mcp).

Add the Apify MCP server to your AI client — this gives you access to all Apify actors, including this one:

### Setup for Claude Code

```
$claude mcp add --transport http apify "https://mcp.apify.com?tools=automation-lab/kijiji-scraper"
```

### Setup for Claude Desktop, Cursor, or VS Code

Add this to your MCP config file:

```
{
    "mcpServers": {
        "apify": {
            "url": "https://mcp.apify.com?tools=automation-lab/kijiji-scraper"
        }
    }
}
```

Your AI assistant will use OAuth to authenticate with your Apify account on first use.

### Example prompts

Once connected, try asking your AI assistant:

- "Use automation-lab/kijiji-scraper to find 2-bedroom apartments under $2,000/month in downtown Toronto"
- "Search Kijiji for used Honda Civic listings in Vancouver and compare prices"
- "Monitor Kijiji Ottawa for new MacBook Pro listings under $1,500"

Learn more in the [Apify MCP documentation](https://docs.apify.com/platform/integrations/mcp).

## Is it legal to scrape Kijiji?

This actor scrapes only **publicly available data** from Kijiji.ca — the same information any visitor can see without logging in. It does not access private accounts, bypass authentication, or collect personal data beyond what sellers publicly display.

Web scraping of public data is generally legal, as confirmed by the US Ninth Circuit Court ruling in *HiQ Labs v. LinkedIn*. However, always comply with applicable laws in your jurisdiction and use the data responsibly.

For more information, see Apify's [guide to ethical web scraping](https://blog.apify.com/is-web-scraping-legal/).

## FAQ

**How fast is Kijiji Canada Scraper?**

Without detail pages, the scraper processes approximately 40 listings per second (one page fetch). With detail pages enabled, it processes about 3-5 listings per second due to individual page fetches. A typical run of 100 listings with details takes about 30-45 seconds.

**How much does it cost to monitor Kijiji daily?**

A daily run scraping 50 new listings with details costs about $0.17 on the Free plan. That's roughly $5/month — well within the free plan's $5 monthly credit.

**Does it work for all Canadian cities?**

Yes. The scraper works with any location on Kijiji.ca. Use the location slug from any Kijiji URL (e.g., "city-of-toronto", "calgary", "montreal", "vancouver", "edmonton", "winnipeg", "halifax", "alberta", "british-columbia").

**Why are some description fields short?**

If you disable "Include full details", descriptions are truncated (~200 characters) as they appear on the search page. Enable full details to get complete descriptions from each listing's detail page.

**Why do some listings show "Please Contact" instead of a price?**

Some Kijiji sellers choose not to display a price. The `price` field shows the display text, and `priceAmount` will be `null` for these listings. You can filter these out in post-processing.

**Why are results from outside my chosen location appearing?**

Kijiji shows promoted/featured ads from across Canada at the top of search results. These are marked with `adType: "TOP_AD"`. Filter by the `location` field in your results to get only local listings.

## Other classifieds and marketplace scrapers

- 🛒 [Poshmark Scraper](https://apify.com/automation-lab/poshmark-scraper) — scrape Poshmark fashion listings
- 🛍️ [Newegg Scraper](https://apify.com/automation-lab/newegg-scraper) — extract electronics and computer products
- 🏠 [Greenhouse Jobs Scraper](https://apify.com/automation-lab/greenhouse-jobs-scraper) — scrape job listings from Greenhouse