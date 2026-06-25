# Bilbasen Scraper

Extract structured car listings from [bilbasen.dk](https://www.bilbasen.dk) — Denmark's largest used car marketplace with 50,000+ active listings.

Get clean JSON with price, specs, images, seller info, geo coordinates, and full descriptions. Search by make, model, year range, and price range — or provide any bilbasen.dk search URL.

Built for car market analytics, price monitoring, dealership intelligence, and automotive data pipelines.

**[Bilbasen Scraper - Denmark’s Car Marketplace on Apify →](https://apify.com/blackfalcondata/bilbasen-scraper?fpr=1h3gvi)**


## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.



## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.



## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.



## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.


---

## Key features










**Incremental mode** — Only get new or changed listings since your last run. Content hash per listing — no duplicates, no re-processing.

**Change classification** — Track expired across runs. Build audit trails of how listings evolve over time.

**Compact output** — Emit core fields only (AI-agent / MCP-friendly). Keeps response size small for LLM workflows.

**Description truncation** — Cap description length per listing to control output size and cost.

**Result cap** — Stop after N listings. Set to 0 for the full catalog.

**Proxy support** — Route traffic through Apify Proxy or your own proxy group to avoid regional blocks and rate limits.

**Export anywhere** — Download as JSON, CSV, or Excel. Stream via Apify API, webhooks, or integrations with Make, Zapier, Airbyte, Keboola.

**Structured data** — Every listing returns the same schema with consistent field naming. All fields always present — `null` when unavailable, never omitted.

---

## Use cases










**Data pipeline automation**
Integrate with your ETL pipeline to collect structured listings from bilbasen.dk on a schedule. Export to CSV, JSON, or directly to your database. Use compact mode to control output size.

**Market research**
Monitor listings, track trends, and analyze market dynamics with structured, deduplicated data from bilbasen.dk.

**Change monitoring**
Run daily or hourly in incremental mode to capture only new, updated, or expired listings. Perfect for price-tracking, churn analysis, and alerting pipelines.

**Lead generation**
Extract employer contact details alongside listings to build outreach lists for recruiters, staffing agencies, or B2B sales teams.

**AI / LLM training data**
Structured JSON per listing is ready for RAG pipelines, embeddings, and agent workflows. Compact mode trims tokens for LLM context windows.

---

## Example output

```json
{
    "url": "https://www.bilbasen.dk/brugt/bil/audi/a4/35-tdi-prestige-avant-s-tr-5d/6794104",
    "portalUrl": "https://www.bilbasen.dk/brugt/bil/audi/a4/35-tdi-prestige-avant-s-tr-5d/6794104",
    "title": "Audi A4 35 TDi Prestige Avant S-tr. 5d",
    "price": 329800,
    "priceAmount": 329800,
    "priceText": "329.800 kr.",
    "make": "Audi",
    "model": "A4",
    "variant": "35 TDi Prestige Avant S-tr. 5d",
    "year": 2021,
    "firstRegistrationDate": "2021-02",
    "mileage": "78.000 km",
    "fuelType": "Diesel",
    "gearType": "Automatisk",
    "locationLat": 55.744602,
    "locationLon": 9.584339,
    "locationCity": "Tønder",
    "locationRegion": "Syd- og Sønderjylland",
    "sellerName": "KJ Biler",
    "sellerType": "Dealer",
    "sellerCity": "Tønder",
    "sellerZipCode": 6270,
    "images": ["https://billeder.bilbasen.dk/..."],
    "imagesCount": 24,
    "scrapedAt": "2026-03-21T00:56:00.000Z"
}
```

---

## Try this example query

Paste this directly into the actor input and run:

```json
{
    "make": "BMW",
    "model": "3-Serien",
    "yearFrom": 2020,
    "priceTo": 400000,
    "maxResults": 50,
    "includeDetailPages": true
}
```

Returns recent BMW 3-series listings from 2020+ under 400,000 DKK — with full specs, seller info, and geo coordinates.

---

## Quick start

### Search by filters

```json
{
    "make": "Audi",
    "model": "A4",
    "yearFrom": 2020,
    "priceFrom": 100000,
    "priceTo": 400000,
    "maxResults": 50
}
```

### Search by URL

```json
{
    "startUrls": [{ "url": "https://www.bilbasen.dk/brugt/bil/bmw/3-serien?yearfrom=2019&pricetype=Retail" }],
    "maxResults": 100,
    "includeDetailPages": true
}
```

### Fast list-only mode

```json
{
    "make": "Toyota",
    "maxResults": 200,
    "includeDetailPages": false,
    "compact": true
}
```

---

## Incremental mode — track new and changed listings

Set up a scheduled run and receive only listings that are new or have changed since your last run. No duplicates, no re-processing.

```json
{
    "make": "Tesla",
    "model": "Model 3",
    "maxResults": 0,
    "includeDetailPages": true,
    "incremental": true
}
```

State is stored in a named Apify KV store and persists across runs. First run outputs everything — subsequent runs output only changes.

---

## Input parameters

### Search

| Parameter | Type | Description |
|:----------|:-----|:------------|
| `startUrls` | array | One bilbasen.dk search URL per run. Optional if filter params are set. |
| `make` | string | Car make (e.g. "Audi", "BMW", "Toyota") |
| `model` | string | Car model (e.g. "A4", "3-Serien"). Requires `make`. |
| `yearFrom` | integer | Minimum model year |
| `yearTo` | integer | Maximum model year |
| `priceFrom` | integer | Minimum price in DKK |
| `priceTo` | integer | Maximum price in DKK |
| `maxResults` | integer | Maximum listings to return (0 = unlimited, default: 100) |

### Output control

| Parameter | Type | Description |
|:----------|:-----|:------------|
| `includeDetailPages` | boolean | Fetch full detail for each listing (default: true) |
| `compact` | boolean | Return only 10 core fields (default: false) |
| `descriptionMaxLength` | integer | Truncate description to N characters |
| `incremental` | boolean | Only output new/changed listings (default: false) |
| `imagesMode` | string | `"first3"` or `"all"` image URLs (default: "first3") |

### Proxy & performance

| Parameter | Type | Description |
|:----------|:-----|:------------|
| `proxyConfiguration` | object | Apify proxy config (strongly recommended) |
| `maxConcurrency` | integer | Max concurrent requests (default: 5) |
| `maxRequestRetries` | integer | Retries per request (default: 3) |
| `maxPages` | integer | Max search result pages (default: 200) |

---

## Output fields

### Vehicle

| Field | Type | Description |
|:------|:-----|:------------|
| `make` | string | Car make (e.g. "Audi") |
| `model` | string | Car model (e.g. "A4") |
| `variant` | string | Full variant name |
| `year` | number | Model year |
| `firstRegistrationDate` | string | First registration in ISO format (e.g. "2021-02") |
| `mileage` | string | Mileage as displayed (e.g. "78.000 km") |
| `fuelType` | string | Fuel type (e.g. "Diesel", "Benzin", "El") |
| `gearType` | string | Gear type (e.g. "Automatisk", "Manuel") |
| `horsepower` | string | Engine output (e.g. "190 hk/400 nm") |
| `color` | string | Color |
| `doors` | number | Number of doors |

### Pricing

| Field | Type | Description |
|:------|:-----|:------------|
| `price` | number | Price from search page (numeric) |
| `priceAmount` | number | Price parsed from detail page |
| `priceText` | string | Price as displayed (e.g. "329.800 kr.") |

### Location

| Field | Type | Description |
|:------|:-----|:------------|
| `locationLat` | number | Latitude |
| `locationLon` | number | Longitude |
| `locationCity` | string | City |
| `locationZipCode` | number | Zip code |
| `locationRegion` | string | Region (e.g. "Østjylland") |

### Seller

| Field | Type | Description |
|:------|:-----|:------------|
| `sellerName` | string | Dealer or private seller name |
| `sellerType` | string | "Dealer" or "Private" |
| `sellerAddress` | string | Full address |
| `sellerCity` | string | City |
| `sellerZipCode` | number | Zip code |
| `sellerPhone` | string | Phone (when available) |

### Content & metadata

| Field | Type | Description |
|:------|:-----|:------------|
| `url` | string | Listing URL |
| `portalUrl` | string | Portal listing URL |
| `title` | string | Listing title |
| `description` | string | Full listing description |
| `features` | string[] | Feature highlights parsed from description |
| `images` | string[] | Image URLs |
| `imagesCount` | number | Total images available |
| `externalId` | number | Bilbasen listing ID |
| `scrapedAt` | string | ISO 8601 timestamp |

---

## Bilbasen car data & scraping

This actor provides structured access to bilbasen.dk car listing data. Common use cases include:

- **Bilbasen API** — query car listings programmatically without a browser
- **Bilbasen car data extraction** — download make, model, price, specs, and seller data at scale
- **Danish used car market dataset** — build datasets for research, analytics, or automotive platforms
- **Bilbasen price monitoring** — track price changes on specific models with incremental mode
- **Car dealership scraper** — collect dealer inventory and pricing across Denmark
- **Bilbasen dataset** — create reusable datasets for analytics, research, or data lake ingestion

---

## Frequently asked questions

**Is this a Bilbasen API?**
Bilbasen does not offer a structured data export. This actor provides programmatic access to bilbasen.dk listings and returns structured JSON — effectively acting as a Bilbasen API for your application.

**How many listings can I scrape?**
Bilbasen has 50,000+ active listings. Set `maxResults: 0` for unlimited. The actor handles pagination automatically across all search result pages.

**Does it return geo coordinates?**
Yes. Every listing includes latitude, longitude, city, zip code, and region — ready for map visualizations and geographic analysis.

**How does smart input resolution work?**
Type "VW" and the actor automatically resolves it to "Volkswagen" for the correct bilbasen URL. Same for "Mercedes" → "Mercedes-Benz", "Alfa" → "Alfa Romeo", and other common aliases.

**Can I use it for price monitoring?**
Yes. Enable `incremental: true` and schedule the actor to run daily or hourly. Each run returns only new or changed listings — ideal for detecting price drops.

**Does it work without proxy?**
It can, but bilbasen.dk uses WAF protection. Apify Proxy is strongly recommended for reliable operation.

---

## Known limitations

- Proxy strongly recommended — bilbasen.dk uses WAF/CDN protection
- One search per run — use one URL or one set of filter parameters per run
- No email data — bilbasen does not expose seller email addresses
- Geo data is from search page — detail pages do not include coordinates
- Sponsored/promoted listings may appear first in results regardless of search filters


## Sample output

One object per listing. Here is a real example from a production run:

```json
{
  "url": "https://www.bilbasen.dk/brugt/bil/vw/idbuzz/77-pro-swb-5d/6846117",
  "portalUrl": "https://www.bilbasen.dk/brugt/bil/vw/idbuzz/77-pro-swb-5d/6846117",
  "title": "VW ID.Buzz 77 Pro SWB 5d",
  "price": 329900,
  "make": "VW",
  "model": "ID.Buzz",
  "variant": "77 Pro SWB 5d",
  "year": 2023,
  "mileage": "15.500 km",
  "fuelType": "El",
  "sellerType": "Dealer",
  "locationCity": "Køge"
}
```

*Truncated — full records contain 52 fields. See Output fields for the complete schema.*


**[Try Bilbasen Scraper - Denmark’s Car Marketplace now — $5 free credit, no credit card →](https://apify.com/blackfalcondata/bilbasen-scraper?fpr=1h3gvi)**


## Pricing

Pay only for what you extract. No subscription required — Apify's free $5 credit covers thousands of results.

| Event | Price (USD) |
| --- | --- |
| Actor Start | $0.01 |
| Result | $0.002 |

See the [actor on Apify](https://apify.com/blackfalcondata/bilbasen-scraper?fpr=1h3gvi) for current pricing.

---

## Related products by Black Falcon Data










- [mobile.de Scraper](https://apify.com/blackfalcondata/mobile-de-scraper?fpr=1h3gvi) — Germany's largest car marketplace
- [StepStone Scraper](https://apify.com/blackfalcondata/stepstone-scraper?fpr=1h3gvi) — Job listings from 18 European portals
- [Indeed Job Scraper](https://apify.com/blackfalcondata/indeed-job-scraper?fpr=1h3gvi) — Indeed job listings with salary data
- [LinkedIn Jobs Scraper](https://apify.com/blackfalcondata/linkedin-jobs-scraper?fpr=1h3gvi) — World's largest professional network — global job listings, no login required
- [Glassdoor Job Scraper](https://apify.com/blackfalcondata/glassdoor-job-scraper?fpr=1h3gvi) — Glassdoor listings with company ratings
- [Arbeitsagentur Scraper](https://apify.com/blackfalcondata/arbeitsagentur-scraper?fpr=1h3gvi) — Germany's official job portal (1M+ listings)

---


## About Black Falcon Data

Black Falcon Data builds production-grade web scrapers for job boards and marketplace data. Browse our full actor catalog at [www.blackfalcondata.com](https://www.blackfalcondata.com).

---

## Getting started with Apify

New to Apify? [Create a free account with $5 credit](https://console.apify.com/sign-up?fpr=1h3gvi) — no credit card required.

1. [Sign up free](https://console.apify.com/sign-up?fpr=1h3gvi) — $5 credit included
2. Open the actor and paste your input
3. Click Start — results download as JSON, CSV, or Excel

Need more volume? [See pricing](https://apify.com/pricing?fpr=1h3gvi).

---

---

*Last updated: March 2026*
