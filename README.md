[Kijiji Scraper](https://apify.com/fayoussef/kijiji-scraper?fpr=data)

# Kijiji.ca Scraper — Extract Vehicles, Real Estate & Classifieds from Kijiji Canada

Scrape Kijiji.ca listings at scale — vehicles, real estate, and general classifieds — with this actor that handles both search result pages and individual ad URLs. It extracts 35+ structured fields per listing including GPS coordinates, vehicle specs (VIN, Carfax link, trim), and seller contact details. Built for automotive dealers, real estate analysts, market researchers, and lead generation teams operating in the Canadian market.

## What you get

**Listing info**

- `id` — Kijiji listing ID
- `title`, `description`
- `kijiji_url` — direct link to the ad
- `ad_source` — Top Ad, Showcase, or standard
- `activation_date`, `sorting_date`

**Pricing**

- `price_type` — Fixed, Please Contact, Free, etc.
- `price_surcharges` — e.g., PLUS_GST

**Location**

- `location_name`, `location_address`
- `latitude`, `longitude` — GPS coordinates

**Seller**

- `Phone Number`
- `poster_id`
- `for_sale_by` — Dealer or Private
- `is_top_ad`, `is_showcase`, `is_highlighted`

**Vehicle-specific fields**

- `make`, `model`, `year`
- `mileage_km`
- `transmission`, `fuel_type`, `drivetrain`
- `body_type`, `color`, `condition`
- `trim`, `vin`
- `carfax_link`
- `seats`, `doors`
- `features` — A/C, alloy wheels, Bluetooth, sunroof, and 20+ more boolean flags

**Media**

- `image_urls` — array of photo URLs

**Meta**

- `source_search_url` — the search that surfaced this listing

## Sample output

```
{
  "id": "m10661116",
  "title": "2024 BMW M4",
  "description": "Presenting the 2024 BMW M4 Competition M xDrive, sold by St. Albert Exotics...",
  "phone_number":"+1-833-870-0000"
  "kijiji_url": "https://kijiji.ca/v-cars-trucks/edmonton/2024-bmw-m4/m10661116",
  "ad_source": "TOP_AD",
  "activation_date": "2025-04-15T23:45:28.000Z",
  "location_name": "Edmonton",
  "location_address": "Saint Albert Trail Northwest, Edmonton, AB, T5L 4H5",
  "latitude": 53.5910375,
  "longitude": -113.5649788,
  "price_type": "FIXED",
  "price_surcharges": "PLUS_GST",
  "make": "bmw",
  "model": "m4",
  "year": 2024,
  "mileage_km": 30160,
  "fuel_type": "Gas",
  "drivetrain": "AWD",
  "body_type": "coup",
  "color": "Black",
  "condition": "Used",
  "for_sale_by": "Dealer",
  "vin": "WBS43AZ04RCP39930",
  "trim": "Competition M xDrive",
  "carfax_link": "https://vhr.carfax.ca/?id=rx6WB4G84rojC55NbLR4s1",
  "seats": 4,
  "doors": 2,
  "features/airconditioning": true,
  "features/sunroof": true,
  "image_urls": [
    "https://media.kijiji.ca/api/v1/autos-prod-ads/images/35/351e0ce4.jpg"
  ],
  "source_search_url": "https://www.kijiji.ca/b-cars-vehicles/edmonton/bmw/k0c27l1700203"
}
```

## Use cases

- Used car dealerships monitoring Kijiji for private seller pricing and competitor dealer inventory across Canadian provinces
- Real estate analysts tracking rental and sale listing activity by neighborhood with GPS precision
- Lead generation agencies building targeted lists of private sellers by vehicle type, city, or price range
- Market research firms studying classified ad volumes and pricing trends across categories
- Insurance companies cross-referencing VINs from Kijiji listings against their own databases
- Automotive wholesalers sourcing inventory leads from both private and dealer ads

## Pricing

| Fee | Amount |
| --- | --- |
| Monthly base | $10.00 |
| Usage | Pay-per-result (see Apify platform for per-event rate) |

**Real example:** Scraping 5,000 Kijiji vehicle listings in the GTA costs the $10 monthly base plus usage.

First results are free — test before subscribing.

## How it works

- Input one or more Kijiji.ca URLs — either search result pages or direct ad URLs
- Set `type_url` to `"listing page"` for search results (with pagination) or `"product page"` for specific ads
- `max_depth` controls how many result pages to process per search URL
- Proxy rotation using Canadian residential IPs is enabled by default
- Up to 3 automatic retries per request with increasing delays
- Export results as JSON, CSV, or Excel from the Apify dataset

## Why this scraper

- Returns GPS coordinates per listing, enabling geospatial analysis out of the box
- Includes VIN and Carfax link for vehicle ads — most Kijiji scrapers omit these
- Boolean feature flags (A/C, alloy wheels, Bluetooth, sunroof, etc.) come as separate columns, ready for filtering
- Handles both search-result pagination and direct ad URLs in one actor
- Uses Canadian residential proxies by default for better success rates on geo-restricted content

## Input example

```
{
  "start_urls": [
    { "url": "https://www.kijiji.ca/b-cars-trucks/gta-greater-toronto-area/c174l1700272" }
  ],
  "type_url": "listing page",
  "max_depth": 5,
  "max_concurrency": 20
}
```

## FAQ

**Can I scrape both vehicles and real estate with the same actor?**
Yes. Provide any Kijiji.ca search URL for any category — vehicles, real estate, jobs, or general classifieds.

**Does it extract vehicle features like A/C or Bluetooth?**
Yes. Each feature is a separate boolean column (e.g., `features/airconditioning`, `features/sunroof`) for easy filtering.

**What proxy setup is used?**
Apify's Canadian residential proxy pool by default. You can supply a custom proxy URL if needed.

**What output formats are available?**
JSON, CSV, Excel, XML, and JSONL — downloadable from the Apify platform.

**Does it support scheduling?**
Yes. Use Apify's scheduler to run daily or on any cron schedule.

**Can I use this via API or MCP?**
Yes. Callable via the Apify REST API and available as an MCP server for AI agents.

**Can I scrape a specific ad page directly?**
Yes. Set `type_url` to `"product page"` and provide direct ad URLs — the actor will extract details without pagination.

## Use via API or MCP

Call this actor via the Apify REST API or as an MCP server for AI agents (Claude, ChatGPT, Cursor):

```
https://mcp.apify.com/actors/fayoussef/kijiji-scraper
```

Full API docs: [https://docs.apify.com/api/v2](https://docs.apify.com/api/v2)

## Need a custom scraper?

Need Kijiji data delivered on a schedule, integrated with a CRM, or combined with other Canadian sources? Visit [automationbyexperts.com](https://automationbyexperts.com) for custom builds, retainers, and data-as-a-service.