# Tudor Lane business data tools (via Apify)

[![Listed on mcpservers.org](https://mcpservers.org/badge.svg)](https://mcpservers.org/servers/tudorlane/tudorlane-mcp)

Pay-per-event tools built on official and public data, for AI agents and people. The caller uses their own [Apify](https://apify.com) account (OAuth or API token). Tudor Lane does not see that token. There is no subscription: each tool charges a small amount per result on Apify.

This repository is a **catalogue**, not a server we host. Each bundle below is a configured view of Apify's hosted MCP server at `https://mcp.apify.com`.

## How to connect

In your MCP client, add a server with:

- **Transport:** Streamable HTTP
- **URL:** one of the bundle URLs below, or `https://mcp.apify.com?tools=search-actors,fetch-actor-details,call-actor` to search the whole Store
- **Auth:** Apify OAuth, or a Bearer token (`Authorization: Bearer <APIFY_TOKEN>`)

Example Cursor / Claude config for the KYB bundle:

```json
{
  "mcpServers": {
    "tudorlane-kyb": {
      "url": "https://mcp.apify.com/?tools=tudorlane/uk-company-check,tudorlane/sanctions-screening,tudorlane/business-id-check,tudorlane/supplier-check,tudorlane/us-company-filings,tudorlane/lei-lookup,tudorlane/website-due-diligence,tudorlane/actor-trust-check,tudorlane/website-safety-check,tudorlane/signup-check,tudorlane/sanctions-watchlist,tudorlane/latam-id-check,tudorlane/adverse-media-watch"
    }
  }
}
```

Replace the URL with another bundle if you need a different job.

## Bundles

### KYB and compliance

`https://mcp.apify.com/?tools=tudorlane/uk-company-check,tudorlane/sanctions-screening,tudorlane/business-id-check,tudorlane/supplier-check,tudorlane/us-company-filings,tudorlane/lei-lookup,tudorlane/website-due-diligence,tudorlane/actor-trust-check,tudorlane/website-safety-check,tudorlane/signup-check,tudorlane/sanctions-watchlist,tudorlane/latam-id-check,tudorlane/adverse-media-watch`

Registry metadata: `kyb/server.json`

- [Companies House API: UK Company Check & KYB Risk](https://apify.com/tudorlane/uk-company-check) — `tudorlane/uk-company-check`
- [OFAC Sanctions Screening: SDN, UK, EU and UN Lists](https://apify.com/tudorlane/sanctions-screening) — `tudorlane/sanctions-screening`
- [VAT Number Validation: EU VIES, IBAN, LEI & EORI Check](https://apify.com/tudorlane/business-id-check) — `tudorlane/business-id-check`
- [Supplier Check API: UK KYB, Sanctions & Website Risk](https://apify.com/tudorlane/supplier-check) — `tudorlane/supplier-check`
- [SEC EDGAR API: US Company Filings, Financials & Insiders](https://apify.com/tudorlane/us-company-filings) — `tudorlane/us-company-filings`
- [LEI Lookup API: GLEIF Search by Name, BIC, ISIN + Parents](https://apify.com/tudorlane/lei-lookup) — `tudorlane/lei-lookup`
- [Website Due Diligence: Domain Age, SSL, Company & Risk Check](https://apify.com/tudorlane/website-due-diligence) — `tudorlane/website-due-diligence`
- [Actor Trust Check: Score Any Apify Actor Before You Call It](https://apify.com/tudorlane/actor-trust-check) — `tudorlane/actor-trust-check`
- [Website Safety & Domain Age Checker API (Scam Signals)](https://apify.com/tudorlane/website-safety-check) — `tudorlane/website-safety-check`
- [Sign-up Fraud Check: Email, Phone & IP Risk Score](https://apify.com/tudorlane/signup-check) — `tudorlane/signup-check`
- [Sanctions Watchlist Monitor: OFAC, UK, EU & UN Alerts](https://apify.com/tudorlane/sanctions-watchlist) — `tudorlane/sanctions-watchlist`
- [LatAm Tax ID Validator: CPF, CNPJ, RFC, CURP, CUIT, RUT](https://apify.com/tudorlane/latam-id-check) — `tudorlane/latam-id-check`
- [Adverse Media Screening: Negative News Monitor for KYC & AML](https://apify.com/tudorlane/adverse-media-watch) — `tudorlane/adverse-media-watch`

### UK everyday business

`https://mcp.apify.com/?tools=tudorlane/uk-pay-calendar-calculator,tudorlane/uk-property-sold-prices,tudorlane/fx-vat-rates,tudorlane/world-holidays-working-days,tudorlane/world-postcode-lookup,tudorlane/hs-tariff-code,tudorlane/gov-tender-watch,tudorlane/uk-company-watch,tudorlane/uk-new-companies-watch,tudorlane/regulation-lookup,tudorlane/regulation-change-watch`

Registry metadata: `uk-business/server.json`

- [UK Pay & Calendar Calculator 2026/27](https://apify.com/tudorlane/uk-pay-calendar-calculator) — `tudorlane/uk-pay-calendar-calculator`
- [UK Property Sold Prices: Land Registry Price Paid Data API](https://apify.com/tudorlane/uk-property-sold-prices) — `tudorlane/uk-property-sold-prices`
- [Currency Converter & VAT Rates by Country API (ECB, EU)](https://apify.com/tudorlane/fx-vat-rates) — `tudorlane/fx-vat-rates`
- [Public Holidays and Working Days API: 150+ Countries](https://apify.com/tudorlane/world-holidays-working-days) — `tudorlane/world-holidays-working-days`
- [Postcode & ZIP Code Lookup API Worldwide (Geocode, Reverse)](https://apify.com/tudorlane/world-postcode-lookup) — `tudorlane/world-postcode-lookup`
- [HS Code & Import Duty API: UK Tariff and US HTS Rates](https://apify.com/tudorlane/hs-tariff-code) — `tudorlane/hs-tariff-code`
- [UK Government Tender Watch: New Public Contract Alerts](https://apify.com/tudorlane/gov-tender-watch) — `tudorlane/gov-tender-watch`
- [UK Company Watch: Companies House Change Monitor](https://apify.com/tudorlane/uk-company-watch) — `tudorlane/uk-company-watch`
- [UK New Companies Watch: Fresh Incorporation Leads](https://apify.com/tudorlane/uk-new-companies-watch) — `tudorlane/uk-new-companies-watch`
- [Regulation & Legislation Search API: UK, US, EU Law](https://apify.com/tudorlane/regulation-lookup) — `tudorlane/regulation-lookup`
- [Regulatory Change Monitor: UK Legislation & US Federal Register](https://apify.com/tudorlane/regulation-change-watch) — `tudorlane/regulation-change-watch`

### Travel and places

`https://mcp.apify.com/?tools=tudorlane/travel-advisories,tudorlane/visa-requirements,tudorlane/airport-airline-lookup,tudorlane/world-weather-forecast,tudorlane/world-postcode-lookup,tudorlane/sun-moon-times,tudorlane/travel-advisory-watch,tudorlane/air-quality,tudorlane/earthquake-disaster-alerts,tudorlane/world-holidays-working-days,tudorlane/timezone-meeting-planner`

Registry metadata: `travel/server.json`

- [Travel Advisory API: UK FCDO & US State Dept by Country](https://apify.com/tudorlane/travel-advisories) — `tudorlane/travel-advisories`
- [Visa Requirements API: Passport to Destination Rules](https://apify.com/tudorlane/visa-requirements) — `tudorlane/visa-requirements`
- [Airport & Airline Code API: IATA, ICAO, Distance](https://apify.com/tudorlane/airport-airline-lookup) — `tudorlane/airport-airline-lookup`
- [Weather Forecast API: Any City or Coordinates Worldwide](https://apify.com/tudorlane/world-weather-forecast) — `tudorlane/world-weather-forecast`
- [Postcode & ZIP Code Lookup API Worldwide (Geocode, Reverse)](https://apify.com/tudorlane/world-postcode-lookup) — `tudorlane/world-postcode-lookup`
- [Sunrise, Sunset & Moon Phase API: Any Place, Any Date](https://apify.com/tudorlane/sun-moon-times) — `tudorlane/sun-moon-times`
- [Travel Advisory Watch: UK FCDO & US State Dept Alerts](https://apify.com/tudorlane/travel-advisory-watch) — `tudorlane/travel-advisory-watch`
- [Air Quality API: Live PM2.5, AQI & Health Advice by City](https://apify.com/tudorlane/air-quality) — `tudorlane/air-quality`
- [Earthquake & Disaster Alerts API: Quakes, Storms, Floods](https://apify.com/tudorlane/earthquake-disaster-alerts) — `tudorlane/earthquake-disaster-alerts`
- [Public Holidays and Working Days API: 150+ Countries](https://apify.com/tudorlane/world-holidays-working-days) — `tudorlane/world-holidays-working-days`
- [Time Zone Converter & Meeting Planner API (DST-aware)](https://apify.com/tudorlane/timezone-meeting-planner) — `tudorlane/timezone-meeting-planner`

### Web and documents

`https://mcp.apify.com/?tools=tudorlane/page-to-markdown,tudorlane/html-markdown-to-pdf,tudorlane/invoice-receipt-parse,tudorlane/seo-page-audit,tudorlane/website-contact-details,tudorlane/sitemap-url-lister,tudorlane/page-metadata-extract,tudorlane/page-change-watch,tudorlane/site-up-link-check,tudorlane/tech-stack-detect,tudorlane/domain-availability,tudorlane/domain-watch`

Registry metadata: `web-docs/server.json`

- [Website to Markdown: Web Page and PDF to LLM-ready Text](https://apify.com/tudorlane/page-to-markdown) — `tudorlane/page-to-markdown`
- [Markdown to PDF: HTML to PDF and Word (DOCX)](https://apify.com/tudorlane/html-markdown-to-pdf) — `tudorlane/html-markdown-to-pdf`
- [Invoice Parser API: Receipts & PDF Invoices to JSON (OCR)](https://apify.com/tudorlane/invoice-receipt-parse) — `tudorlane/invoice-receipt-parse`
- [SEO Audit: On-Page Checks, Score and Fixes](https://apify.com/tudorlane/seo-page-audit) — `tudorlane/seo-page-audit`
- [Contact Details Scraper - Emails, Phones & Socials](https://apify.com/tudorlane/website-contact-details) — `tudorlane/website-contact-details`
- [Sitemap URL Extractor: All Pages of a Website](https://apify.com/tudorlane/sitemap-url-lister) — `tudorlane/sitemap-url-lister`
- [Page Metadata Extractor API: OpenGraph, JSON-LD, Feeds](https://apify.com/tudorlane/page-metadata-extract) — `tudorlane/page-metadata-extract`
- [Website Change Monitor: Page Change Detection & Diff Alerts](https://apify.com/tudorlane/page-change-watch) — `tudorlane/page-change-watch`
- [Bulk URL Status Checker: HTTP Codes, Redirects, 404s](https://apify.com/tudorlane/site-up-link-check) — `tudorlane/site-up-link-check`
- [Tech Stack Detector: BuiltWith & Wappalyzer Alternative](https://apify.com/tudorlane/tech-stack-detect) — `tudorlane/tech-stack-detect`
- [Domain Availability Checker API: Bulk RDAP Lookup](https://apify.com/tudorlane/domain-availability) — `tudorlane/domain-availability`
- [Domain WHOIS & Website Watch: SSL, DNS, Expiry, Uptime](https://apify.com/tudorlane/domain-watch) — `tudorlane/domain-watch`

### Markets and filings

`https://mcp.apify.com/?tools=tudorlane/us-company-filings,tudorlane/stock-price,tudorlane/interest-rates-yields,tudorlane/macro-indicators,tudorlane/market-hours,tudorlane/funding-round-watch,tudorlane/fx-rate-alert,tudorlane/fx-vat-rates,tudorlane/card-and-id-checksums,tudorlane/lei-lookup`

Registry metadata: `markets/server.json`

- [SEC EDGAR API: US Company Filings, Financials & Insiders](https://apify.com/tudorlane/us-company-filings) — `tudorlane/us-company-filings`
- [Stock Price & Fundamentals API: Quotes, History, SEC Financials](https://apify.com/tudorlane/stock-price) — `tudorlane/stock-price`
- [Interest Rates & Bond Yields API: Fed, BoE, ECB](https://apify.com/tudorlane/interest-rates-yields) — `tudorlane/interest-rates-yields`
- [Macroeconomic Data API: Inflation, GDP, Unemployment by Country](https://apify.com/tudorlane/macro-indicators) — `tudorlane/macro-indicators`
- [Stock Market Hours API: Is the Exchange Open Now?](https://apify.com/tudorlane/market-hours) — `tudorlane/market-hours`
- [Startup Funding Rounds Tracker: SEC Form D & UK Allotments](https://apify.com/tudorlane/funding-round-watch) — `tudorlane/funding-round-watch`
- [FX Rate Alert: Currency Move Monitor (ECB Rates)](https://apify.com/tudorlane/fx-rate-alert) — `tudorlane/fx-rate-alert`
- [Currency Converter & VAT Rates by Country API (ECB, EU)](https://apify.com/tudorlane/fx-vat-rates) — `tudorlane/fx-vat-rates`
- [Check Digit Validator: Card Luhn, ISBN, EAN, ISIN, CUSIP, SEDOL](https://apify.com/tudorlane/card-and-id-checksums) — `tudorlane/card-and-id-checksums`
- [LEI Lookup API: GLEIF Search by Name, BIC, ISIN + Parents](https://apify.com/tudorlane/lei-lookup) — `tudorlane/lei-lookup`

### Security and dev

`https://mcp.apify.com/?tools=tudorlane/actor-trust-check,tudorlane/cve-lookup,tudorlane/package-health,tudorlane/package-vuln-watch,tudorlane/website-safety-check,tudorlane/signup-check,tudorlane/domain-availability,tudorlane/tech-stack-detect,tudorlane/site-up-link-check,tudorlane/website-due-diligence,tudorlane/domain-watch,tudorlane/ip-geolocation`

Registry metadata: `security-dev/server.json`

- [Actor Trust Check: Score Any Apify Actor Before You Call It](https://apify.com/tudorlane/actor-trust-check) — `tudorlane/actor-trust-check`
- [CVE Lookup API: Severity, Fixed Versions & Exploited](https://apify.com/tudorlane/cve-lookup) — `tudorlane/cve-lookup`
- [Package Health API: Version, Licence & Vulnerabilities](https://apify.com/tudorlane/package-health) — `tudorlane/package-health`
- [Package Vulnerability Watch: New CVEs & Releases Monitor](https://apify.com/tudorlane/package-vuln-watch) — `tudorlane/package-vuln-watch`
- [Website Safety & Domain Age Checker API (Scam Signals)](https://apify.com/tudorlane/website-safety-check) — `tudorlane/website-safety-check`
- [Sign-up Fraud Check: Email, Phone & IP Risk Score](https://apify.com/tudorlane/signup-check) — `tudorlane/signup-check`
- [Domain Availability Checker API: Bulk RDAP Lookup](https://apify.com/tudorlane/domain-availability) — `tudorlane/domain-availability`
- [Tech Stack Detector: BuiltWith & Wappalyzer Alternative](https://apify.com/tudorlane/tech-stack-detect) — `tudorlane/tech-stack-detect`
- [Bulk URL Status Checker: HTTP Codes, Redirects, 404s](https://apify.com/tudorlane/site-up-link-check) — `tudorlane/site-up-link-check`
- [Website Due Diligence: Domain Age, SSL, Company & Risk Check](https://apify.com/tudorlane/website-due-diligence) — `tudorlane/website-due-diligence`
- [Domain WHOIS & Website Watch: SSL, DNS, Expiry, Uptime](https://apify.com/tudorlane/domain-watch) — `tudorlane/domain-watch`
- [IP Geolocation API: Country, City, ASN & Time Zone](https://apify.com/tudorlane/ip-geolocation) — `tudorlane/ip-geolocation`

### Monitors and watches

`https://mcp.apify.com/?tools=tudorlane/page-change-watch,tudorlane/domain-watch,tudorlane/rss-feed-watch,tudorlane/sanctions-watchlist,tudorlane/uk-company-watch,tudorlane/uk-new-companies-watch,tudorlane/fx-rate-alert,tudorlane/regulation-change-watch,tudorlane/travel-advisory-watch,tudorlane/package-vuln-watch,tudorlane/price-stock-watch,tudorlane/adverse-media-watch`

Registry metadata: `monitors-watches/server.json`

- [Website Change Monitor: Page Change Detection & Diff Alerts](https://apify.com/tudorlane/page-change-watch) — `tudorlane/page-change-watch`
- [Domain WHOIS & Website Watch: SSL, DNS, Expiry, Uptime](https://apify.com/tudorlane/domain-watch) — `tudorlane/domain-watch`
- [RSS Feed Reader & Monitor: New Items, Atom, Feed Finder](https://apify.com/tudorlane/rss-feed-watch) — `tudorlane/rss-feed-watch`
- [Sanctions Watchlist Monitor: OFAC, UK, EU & UN Alerts](https://apify.com/tudorlane/sanctions-watchlist) — `tudorlane/sanctions-watchlist`
- [UK Company Watch: Companies House Change Monitor](https://apify.com/tudorlane/uk-company-watch) — `tudorlane/uk-company-watch`
- [UK New Companies Watch: Fresh Incorporation Leads](https://apify.com/tudorlane/uk-new-companies-watch) — `tudorlane/uk-new-companies-watch`
- [FX Rate Alert: Currency Move Monitor (ECB Rates)](https://apify.com/tudorlane/fx-rate-alert) — `tudorlane/fx-rate-alert`
- [Regulatory Change Monitor: UK Legislation & US Federal Register](https://apify.com/tudorlane/regulation-change-watch) — `tudorlane/regulation-change-watch`
- [Travel Advisory Watch: UK FCDO & US State Dept Alerts](https://apify.com/tudorlane/travel-advisory-watch) — `tudorlane/travel-advisory-watch`
- [Package Vulnerability Watch: New CVEs & Releases Monitor](https://apify.com/tudorlane/package-vuln-watch) — `tudorlane/package-vuln-watch`
- [Price Tracker: Product Price Drop & Back-in-Stock Alerts](https://apify.com/tudorlane/price-stock-watch) — `tudorlane/price-stock-watch`
- [Adverse Media Screening: Negative News Monitor for KYC & AML](https://apify.com/tudorlane/adverse-media-watch) — `tudorlane/adverse-media-watch`

### Leads and news

`https://mcp.apify.com/?tools=tudorlane/company-from-domain,tudorlane/lead-enrichment,tudorlane/email-verify,tudorlane/phone-validate,tudorlane/company-hiring-watch,tudorlane/job-title-salary,tudorlane/news-feed-search,tudorlane/adverse-media-watch,tudorlane/topic-trends,tudorlane/website-contact-details,tudorlane/rss-feed-watch,tudorlane/uk-new-companies-watch`

Registry metadata: `leads-news/server.json`

- [Company Enrichment API: Domain to Company Profile](https://apify.com/tudorlane/company-from-domain) — `tudorlane/company-from-domain`
- [Lead Enrichment & Company Enrichment by Domain](https://apify.com/tudorlane/lead-enrichment) — `tudorlane/lead-enrichment`
- [Email Verifier & Email Validation - Bulk Email Checker](https://apify.com/tudorlane/email-verify) — `tudorlane/email-verify`
- [Phone Number Validator API: Format, Type & Country](https://apify.com/tudorlane/phone-validate) — `tudorlane/phone-validate`
- [Job Postings Scraper & Hiring Watch: Greenhouse, Lever, Ashby](https://apify.com/tudorlane/company-hiring-watch) — `tudorlane/company-hiring-watch`
- [Job Title to Salary API: SOC Codes & US Pay by State](https://apify.com/tudorlane/job-title-salary) — `tudorlane/job-title-salary`
- [News Scraper - Latest News Articles & Headlines API](https://apify.com/tudorlane/news-feed-search) — `tudorlane/news-feed-search`
- [Adverse Media Screening: Negative News Monitor for KYC & AML](https://apify.com/tudorlane/adverse-media-watch) — `tudorlane/adverse-media-watch`
- [Topic Trends API: Daily Interest from Wikipedia Views](https://apify.com/tudorlane/topic-trends) — `tudorlane/topic-trends`
- [Contact Details Scraper - Emails, Phones & Socials](https://apify.com/tudorlane/website-contact-details) — `tudorlane/website-contact-details`
- [RSS Feed Reader & Monitor: New Items, Atom, Feed Finder](https://apify.com/tudorlane/rss-feed-watch) — `tudorlane/rss-feed-watch`
- [UK New Companies Watch: Fresh Incorporation Leads](https://apify.com/tudorlane/uk-new-companies-watch) — `tudorlane/uk-new-companies-watch`

### Ecommerce and products

`https://mcp.apify.com/?tools=tudorlane/barcode-product-lookup,tudorlane/price-stock-watch,tudorlane/qr-barcode-tools,tudorlane/vin-decoder,tudorlane/hs-tariff-code,tudorlane/invoice-receipt-parse,tudorlane/tech-stack-detect,tudorlane/card-and-id-checksums,tudorlane/fx-vat-rates`

Registry metadata: `ecommerce-products/server.json`

- [Barcode Lookup API: EAN/UPC to Product & Nutrition](https://apify.com/tudorlane/barcode-product-lookup) — `tudorlane/barcode-product-lookup`
- [Price Tracker: Product Price Drop & Back-in-Stock Alerts](https://apify.com/tudorlane/price-stock-watch) — `tudorlane/price-stock-watch`
- [QR Code & Barcode API: Generate PNG/SVG and Decode Images](https://apify.com/tudorlane/qr-barcode-tools) — `tudorlane/qr-barcode-tools`
- [VIN Decoder API: Make, Model, Year, Specs & Recalls](https://apify.com/tudorlane/vin-decoder) — `tudorlane/vin-decoder`
- [HS Code & Import Duty API: UK Tariff and US HTS Rates](https://apify.com/tudorlane/hs-tariff-code) — `tudorlane/hs-tariff-code`
- [Invoice Parser API: Receipts & PDF Invoices to JSON (OCR)](https://apify.com/tudorlane/invoice-receipt-parse) — `tudorlane/invoice-receipt-parse`
- [Tech Stack Detector: BuiltWith & Wappalyzer Alternative](https://apify.com/tudorlane/tech-stack-detect) — `tudorlane/tech-stack-detect`
- [Check Digit Validator: Card Luhn, ISBN, EAN, ISIN, CUSIP, SEDOL](https://apify.com/tudorlane/card-and-id-checksums) — `tudorlane/card-and-id-checksums`
- [Currency Converter & VAT Rates by Country API (ECB, EU)](https://apify.com/tudorlane/fx-vat-rates) — `tudorlane/fx-vat-rates`

### Health and regulation

`https://mcp.apify.com/?tools=tudorlane/medical-codes-providers,tudorlane/regulation-lookup,tudorlane/regulation-change-watch,tudorlane/air-quality,tudorlane/earthquake-disaster-alerts`

Registry metadata: `health-regulation/server.json`

- [ICD-10 & NPI Lookup API: HCPCS, LOINC, Drug Labels](https://apify.com/tudorlane/medical-codes-providers) — `tudorlane/medical-codes-providers`
- [Regulation & Legislation Search API: UK, US, EU Law](https://apify.com/tudorlane/regulation-lookup) — `tudorlane/regulation-lookup`
- [Regulatory Change Monitor: UK Legislation & US Federal Register](https://apify.com/tudorlane/regulation-change-watch) — `tudorlane/regulation-change-watch`
- [Air Quality API: Live PM2.5, AQI & Health Advice by City](https://apify.com/tudorlane/air-quality) — `tudorlane/air-quality`
- [Earthquake & Disaster Alerts API: Quakes, Storms, Floods](https://apify.com/tudorlane/earthquake-disaster-alerts) — `tudorlane/earthquake-disaster-alerts`

### Data lookups

`https://mcp.apify.com/?tools=tudorlane/wiki-facts,tudorlane/academic-paper-search,tudorlane/iso-codes-lookup,tudorlane/ip-geolocation,tudorlane/latam-id-check,tudorlane/card-and-id-checksums,tudorlane/unit-converter,tudorlane/vin-decoder,tudorlane/barcode-product-lookup,tudorlane/lei-lookup,tudorlane/medical-codes-providers,tudorlane/world-postcode-lookup`

Registry metadata: `data-lookups/server.json`

- [Wikipedia & Wikidata Facts API: Summary + Key Facts](https://apify.com/tudorlane/wiki-facts) — `tudorlane/wiki-facts`
- [Academic Paper Search API: Crossref, arXiv & DOI Lookup](https://apify.com/tudorlane/academic-paper-search) — `tudorlane/academic-paper-search`
- [Country, Currency & Language Codes API: ISO Lookup](https://apify.com/tudorlane/iso-codes-lookup) — `tudorlane/iso-codes-lookup`
- [IP Geolocation API: Country, City, ASN & Time Zone](https://apify.com/tudorlane/ip-geolocation) — `tudorlane/ip-geolocation`
- [LatAm Tax ID Validator: CPF, CNPJ, RFC, CURP, CUIT, RUT](https://apify.com/tudorlane/latam-id-check) — `tudorlane/latam-id-check`
- [Check Digit Validator: Card Luhn, ISBN, EAN, ISIN, CUSIP, SEDOL](https://apify.com/tudorlane/card-and-id-checksums) — `tudorlane/card-and-id-checksums`
- [Unit Converter API: Length, Weight, Temperature & Cooking](https://apify.com/tudorlane/unit-converter) — `tudorlane/unit-converter`
- [VIN Decoder API: Make, Model, Year, Specs & Recalls](https://apify.com/tudorlane/vin-decoder) — `tudorlane/vin-decoder`
- [Barcode Lookup API: EAN/UPC to Product & Nutrition](https://apify.com/tudorlane/barcode-product-lookup) — `tudorlane/barcode-product-lookup`
- [LEI Lookup API: GLEIF Search by Name, BIC, ISIN + Parents](https://apify.com/tudorlane/lei-lookup) — `tudorlane/lei-lookup`
- [ICD-10 & NPI Lookup API: HCPCS, LOINC, Drug Labels](https://apify.com/tudorlane/medical-codes-providers) — `tudorlane/medical-codes-providers`
- [Postcode & ZIP Code Lookup API Worldwide (Geocode, Reverse)](https://apify.com/tudorlane/world-postcode-lookup) — `tudorlane/world-postcode-lookup`

### Text, files and utilities

`https://mcp.apify.com/?tools=tudorlane/text-toolkit,tudorlane/file-convert-profile,tudorlane/json-schema-validate,tudorlane/exact-calc,tudorlane/date-parse-cron,tudorlane/timezone-meeting-planner,tudorlane/ics-calendar-tools,tudorlane/image-exif-metadata,tudorlane/page-metadata-extract,tudorlane/provable-random,tudorlane/html-markdown-to-pdf,tudorlane/unit-converter`

Registry metadata: `text-files/server.json`

- [Token Counter & Text Stats API: Tokens, Language, Readability](https://apify.com/tudorlane/text-toolkit) — `tudorlane/text-toolkit`
- [CSV to JSON Converter: Excel, Parquet & Data Profiler](https://apify.com/tudorlane/file-convert-profile) — `tudorlane/file-convert-profile`
- [JSON Schema Validator API: Validate & Infer Schemas](https://apify.com/tudorlane/json-schema-validate) — `tudorlane/json-schema-validate`
- [Exact Calculator API: Decimal Maths, Percent, Loans, Rounding](https://apify.com/tudorlane/exact-calc) — `tudorlane/exact-calc`
- [Date Parser & Cron API: Natural Language to ISO Dates](https://apify.com/tudorlane/date-parse-cron) — `tudorlane/date-parse-cron`
- [Time Zone Converter & Meeting Planner API (DST-aware)](https://apify.com/tudorlane/timezone-meeting-planner) — `tudorlane/timezone-meeting-planner`
- [Calendar ICS API: Create Invites, Parse Feeds, Free Slots](https://apify.com/tudorlane/ics-calendar-tools) — `tudorlane/ics-calendar-tools`
- [Photo EXIF Metadata Reader & Stripper: GPS, Camera, Date](https://apify.com/tudorlane/image-exif-metadata) — `tudorlane/image-exif-metadata`
- [Page Metadata Extractor API: OpenGraph, JSON-LD, Feeds](https://apify.com/tudorlane/page-metadata-extract) — `tudorlane/page-metadata-extract`
- [Provably Fair Random Picker: Raffles, Draws, Shuffles & IDs](https://apify.com/tudorlane/provable-random) — `tudorlane/provable-random`
- [Markdown to PDF: HTML to PDF and Word (DOCX)](https://apify.com/tudorlane/html-markdown-to-pdf) — `tudorlane/html-markdown-to-pdf`
- [Unit Converter API: Length, Weight, Temperature & Cooking](https://apify.com/tudorlane/unit-converter) — `tudorlane/unit-converter`
## Tools by job

The bundles above are short lists (5–12 tools) so they fit in an agent's context window. A tool can appear in more than one bundle when it genuinely fits both jobs.

### KYB and compliance

- [Companies House API: UK Company Check & KYB Risk](https://apify.com/tudorlane/uk-company-check) — `tudorlane/uk-company-check`
- [OFAC Sanctions Screening: SDN, UK, EU and UN Lists](https://apify.com/tudorlane/sanctions-screening) — `tudorlane/sanctions-screening`
- [VAT Number Validation: EU VIES, IBAN, LEI & EORI Check](https://apify.com/tudorlane/business-id-check) — `tudorlane/business-id-check`
- [Supplier Check API: UK KYB, Sanctions & Website Risk](https://apify.com/tudorlane/supplier-check) — `tudorlane/supplier-check`
- [SEC EDGAR API: US Company Filings, Financials & Insiders](https://apify.com/tudorlane/us-company-filings) — `tudorlane/us-company-filings`
- [LEI Lookup API: GLEIF Search by Name, BIC, ISIN + Parents](https://apify.com/tudorlane/lei-lookup) — `tudorlane/lei-lookup`
- [Website Due Diligence: Domain Age, SSL, Company & Risk Check](https://apify.com/tudorlane/website-due-diligence) — `tudorlane/website-due-diligence`
- [Actor Trust Check: Score Any Apify Actor Before You Call It](https://apify.com/tudorlane/actor-trust-check) — `tudorlane/actor-trust-check`
- [Website Safety & Domain Age Checker API (Scam Signals)](https://apify.com/tudorlane/website-safety-check) — `tudorlane/website-safety-check`
- [Sign-up Fraud Check: Email, Phone & IP Risk Score](https://apify.com/tudorlane/signup-check) — `tudorlane/signup-check`
- [Sanctions Watchlist Monitor: OFAC, UK, EU & UN Alerts](https://apify.com/tudorlane/sanctions-watchlist) — `tudorlane/sanctions-watchlist`
- [LatAm Tax ID Validator: CPF, CNPJ, RFC, CURP, CUIT, RUT](https://apify.com/tudorlane/latam-id-check) — `tudorlane/latam-id-check`
- [Adverse Media Screening: Negative News Monitor for KYC & AML](https://apify.com/tudorlane/adverse-media-watch) — `tudorlane/adverse-media-watch`

### UK everyday business

- [UK Pay & Calendar Calculator 2026/27](https://apify.com/tudorlane/uk-pay-calendar-calculator) — `tudorlane/uk-pay-calendar-calculator`
- [UK Property Sold Prices: Land Registry Price Paid Data API](https://apify.com/tudorlane/uk-property-sold-prices) — `tudorlane/uk-property-sold-prices`
- [Currency Converter & VAT Rates by Country API (ECB, EU)](https://apify.com/tudorlane/fx-vat-rates) — `tudorlane/fx-vat-rates`
- [Public Holidays and Working Days API: 150+ Countries](https://apify.com/tudorlane/world-holidays-working-days) — `tudorlane/world-holidays-working-days`
- [Postcode & ZIP Code Lookup API Worldwide (Geocode, Reverse)](https://apify.com/tudorlane/world-postcode-lookup) — `tudorlane/world-postcode-lookup`
- [HS Code & Import Duty API: UK Tariff and US HTS Rates](https://apify.com/tudorlane/hs-tariff-code) — `tudorlane/hs-tariff-code`
- [UK Government Tender Watch: New Public Contract Alerts](https://apify.com/tudorlane/gov-tender-watch) — `tudorlane/gov-tender-watch`
- [UK Company Watch: Companies House Change Monitor](https://apify.com/tudorlane/uk-company-watch) — `tudorlane/uk-company-watch`
- [UK New Companies Watch: Fresh Incorporation Leads](https://apify.com/tudorlane/uk-new-companies-watch) — `tudorlane/uk-new-companies-watch`
- [Regulation & Legislation Search API: UK, US, EU Law](https://apify.com/tudorlane/regulation-lookup) — `tudorlane/regulation-lookup`
- [Regulatory Change Monitor: UK Legislation & US Federal Register](https://apify.com/tudorlane/regulation-change-watch) — `tudorlane/regulation-change-watch`

### Travel and places

- [Travel Advisory API: UK FCDO & US State Dept by Country](https://apify.com/tudorlane/travel-advisories) — `tudorlane/travel-advisories`
- [Visa Requirements API: Passport to Destination Rules](https://apify.com/tudorlane/visa-requirements) — `tudorlane/visa-requirements`
- [Airport & Airline Code API: IATA, ICAO, Distance](https://apify.com/tudorlane/airport-airline-lookup) — `tudorlane/airport-airline-lookup`
- [Weather Forecast API: Any City or Coordinates Worldwide](https://apify.com/tudorlane/world-weather-forecast) — `tudorlane/world-weather-forecast`
- [Postcode & ZIP Code Lookup API Worldwide (Geocode, Reverse)](https://apify.com/tudorlane/world-postcode-lookup) — `tudorlane/world-postcode-lookup`
- [Sunrise, Sunset & Moon Phase API: Any Place, Any Date](https://apify.com/tudorlane/sun-moon-times) — `tudorlane/sun-moon-times`
- [Travel Advisory Watch: UK FCDO & US State Dept Alerts](https://apify.com/tudorlane/travel-advisory-watch) — `tudorlane/travel-advisory-watch`
- [Air Quality API: Live PM2.5, AQI & Health Advice by City](https://apify.com/tudorlane/air-quality) — `tudorlane/air-quality`
- [Earthquake & Disaster Alerts API: Quakes, Storms, Floods](https://apify.com/tudorlane/earthquake-disaster-alerts) — `tudorlane/earthquake-disaster-alerts`
- [Public Holidays and Working Days API: 150+ Countries](https://apify.com/tudorlane/world-holidays-working-days) — `tudorlane/world-holidays-working-days`
- [Time Zone Converter & Meeting Planner API (DST-aware)](https://apify.com/tudorlane/timezone-meeting-planner) — `tudorlane/timezone-meeting-planner`

### Web and documents

- [Website to Markdown: Web Page and PDF to LLM-ready Text](https://apify.com/tudorlane/page-to-markdown) — `tudorlane/page-to-markdown`
- [Markdown to PDF: HTML to PDF and Word (DOCX)](https://apify.com/tudorlane/html-markdown-to-pdf) — `tudorlane/html-markdown-to-pdf`
- [Invoice Parser API: Receipts & PDF Invoices to JSON (OCR)](https://apify.com/tudorlane/invoice-receipt-parse) — `tudorlane/invoice-receipt-parse`
- [SEO Audit: On-Page Checks, Score and Fixes](https://apify.com/tudorlane/seo-page-audit) — `tudorlane/seo-page-audit`
- [Contact Details Scraper - Emails, Phones & Socials](https://apify.com/tudorlane/website-contact-details) — `tudorlane/website-contact-details`
- [Sitemap URL Extractor: All Pages of a Website](https://apify.com/tudorlane/sitemap-url-lister) — `tudorlane/sitemap-url-lister`
- [Page Metadata Extractor API: OpenGraph, JSON-LD, Feeds](https://apify.com/tudorlane/page-metadata-extract) — `tudorlane/page-metadata-extract`
- [Website Change Monitor: Page Change Detection & Diff Alerts](https://apify.com/tudorlane/page-change-watch) — `tudorlane/page-change-watch`
- [Bulk URL Status Checker: HTTP Codes, Redirects, 404s](https://apify.com/tudorlane/site-up-link-check) — `tudorlane/site-up-link-check`
- [Tech Stack Detector: BuiltWith & Wappalyzer Alternative](https://apify.com/tudorlane/tech-stack-detect) — `tudorlane/tech-stack-detect`
- [Domain Availability Checker API: Bulk RDAP Lookup](https://apify.com/tudorlane/domain-availability) — `tudorlane/domain-availability`
- [Domain WHOIS & Website Watch: SSL, DNS, Expiry, Uptime](https://apify.com/tudorlane/domain-watch) — `tudorlane/domain-watch`

### Markets and filings

- [SEC EDGAR API: US Company Filings, Financials & Insiders](https://apify.com/tudorlane/us-company-filings) — `tudorlane/us-company-filings`
- [Stock Price & Fundamentals API: Quotes, History, SEC Financials](https://apify.com/tudorlane/stock-price) — `tudorlane/stock-price`
- [Interest Rates & Bond Yields API: Fed, BoE, ECB](https://apify.com/tudorlane/interest-rates-yields) — `tudorlane/interest-rates-yields`
- [Macroeconomic Data API: Inflation, GDP, Unemployment by Country](https://apify.com/tudorlane/macro-indicators) — `tudorlane/macro-indicators`
- [Stock Market Hours API: Is the Exchange Open Now?](https://apify.com/tudorlane/market-hours) — `tudorlane/market-hours`
- [Startup Funding Rounds Tracker: SEC Form D & UK Allotments](https://apify.com/tudorlane/funding-round-watch) — `tudorlane/funding-round-watch`
- [FX Rate Alert: Currency Move Monitor (ECB Rates)](https://apify.com/tudorlane/fx-rate-alert) — `tudorlane/fx-rate-alert`
- [Currency Converter & VAT Rates by Country API (ECB, EU)](https://apify.com/tudorlane/fx-vat-rates) — `tudorlane/fx-vat-rates`
- [Check Digit Validator: Card Luhn, ISBN, EAN, ISIN, CUSIP, SEDOL](https://apify.com/tudorlane/card-and-id-checksums) — `tudorlane/card-and-id-checksums`
- [LEI Lookup API: GLEIF Search by Name, BIC, ISIN + Parents](https://apify.com/tudorlane/lei-lookup) — `tudorlane/lei-lookup`

### Security and dev

- [Actor Trust Check: Score Any Apify Actor Before You Call It](https://apify.com/tudorlane/actor-trust-check) — `tudorlane/actor-trust-check`
- [CVE Lookup API: Severity, Fixed Versions & Exploited](https://apify.com/tudorlane/cve-lookup) — `tudorlane/cve-lookup`
- [Package Health API: Version, Licence & Vulnerabilities](https://apify.com/tudorlane/package-health) — `tudorlane/package-health`
- [Package Vulnerability Watch: New CVEs & Releases Monitor](https://apify.com/tudorlane/package-vuln-watch) — `tudorlane/package-vuln-watch`
- [Website Safety & Domain Age Checker API (Scam Signals)](https://apify.com/tudorlane/website-safety-check) — `tudorlane/website-safety-check`
- [Sign-up Fraud Check: Email, Phone & IP Risk Score](https://apify.com/tudorlane/signup-check) — `tudorlane/signup-check`
- [Domain Availability Checker API: Bulk RDAP Lookup](https://apify.com/tudorlane/domain-availability) — `tudorlane/domain-availability`
- [Tech Stack Detector: BuiltWith & Wappalyzer Alternative](https://apify.com/tudorlane/tech-stack-detect) — `tudorlane/tech-stack-detect`
- [Bulk URL Status Checker: HTTP Codes, Redirects, 404s](https://apify.com/tudorlane/site-up-link-check) — `tudorlane/site-up-link-check`
- [Website Due Diligence: Domain Age, SSL, Company & Risk Check](https://apify.com/tudorlane/website-due-diligence) — `tudorlane/website-due-diligence`
- [Domain WHOIS & Website Watch: SSL, DNS, Expiry, Uptime](https://apify.com/tudorlane/domain-watch) — `tudorlane/domain-watch`
- [IP Geolocation API: Country, City, ASN & Time Zone](https://apify.com/tudorlane/ip-geolocation) — `tudorlane/ip-geolocation`

### Monitors and watches

- [Website Change Monitor: Page Change Detection & Diff Alerts](https://apify.com/tudorlane/page-change-watch) — `tudorlane/page-change-watch`
- [Domain WHOIS & Website Watch: SSL, DNS, Expiry, Uptime](https://apify.com/tudorlane/domain-watch) — `tudorlane/domain-watch`
- [RSS Feed Reader & Monitor: New Items, Atom, Feed Finder](https://apify.com/tudorlane/rss-feed-watch) — `tudorlane/rss-feed-watch`
- [Sanctions Watchlist Monitor: OFAC, UK, EU & UN Alerts](https://apify.com/tudorlane/sanctions-watchlist) — `tudorlane/sanctions-watchlist`
- [UK Company Watch: Companies House Change Monitor](https://apify.com/tudorlane/uk-company-watch) — `tudorlane/uk-company-watch`
- [UK New Companies Watch: Fresh Incorporation Leads](https://apify.com/tudorlane/uk-new-companies-watch) — `tudorlane/uk-new-companies-watch`
- [FX Rate Alert: Currency Move Monitor (ECB Rates)](https://apify.com/tudorlane/fx-rate-alert) — `tudorlane/fx-rate-alert`
- [Regulatory Change Monitor: UK Legislation & US Federal Register](https://apify.com/tudorlane/regulation-change-watch) — `tudorlane/regulation-change-watch`
- [Travel Advisory Watch: UK FCDO & US State Dept Alerts](https://apify.com/tudorlane/travel-advisory-watch) — `tudorlane/travel-advisory-watch`
- [Package Vulnerability Watch: New CVEs & Releases Monitor](https://apify.com/tudorlane/package-vuln-watch) — `tudorlane/package-vuln-watch`
- [Price Tracker: Product Price Drop & Back-in-Stock Alerts](https://apify.com/tudorlane/price-stock-watch) — `tudorlane/price-stock-watch`
- [Adverse Media Screening: Negative News Monitor for KYC & AML](https://apify.com/tudorlane/adverse-media-watch) — `tudorlane/adverse-media-watch`

### Leads, news and hiring

- [Company Enrichment API: Domain to Company Profile](https://apify.com/tudorlane/company-from-domain) — `tudorlane/company-from-domain`
- [Lead Enrichment & Company Enrichment by Domain](https://apify.com/tudorlane/lead-enrichment) — `tudorlane/lead-enrichment`
- [Email Verifier & Email Validation - Bulk Email Checker](https://apify.com/tudorlane/email-verify) — `tudorlane/email-verify`
- [Phone Number Validator API: Format, Type & Country](https://apify.com/tudorlane/phone-validate) — `tudorlane/phone-validate`
- [Job Postings Scraper & Hiring Watch: Greenhouse, Lever, Ashby](https://apify.com/tudorlane/company-hiring-watch) — `tudorlane/company-hiring-watch`
- [Job Title to Salary API: SOC Codes & US Pay by State](https://apify.com/tudorlane/job-title-salary) — `tudorlane/job-title-salary`
- [News Scraper - Latest News Articles & Headlines API](https://apify.com/tudorlane/news-feed-search) — `tudorlane/news-feed-search`
- [Adverse Media Screening: Negative News Monitor for KYC & AML](https://apify.com/tudorlane/adverse-media-watch) — `tudorlane/adverse-media-watch`
- [Topic Trends API: Daily Interest from Wikipedia Views](https://apify.com/tudorlane/topic-trends) — `tudorlane/topic-trends`
- [Contact Details Scraper - Emails, Phones & Socials](https://apify.com/tudorlane/website-contact-details) — `tudorlane/website-contact-details`
- [RSS Feed Reader & Monitor: New Items, Atom, Feed Finder](https://apify.com/tudorlane/rss-feed-watch) — `tudorlane/rss-feed-watch`
- [UK New Companies Watch: Fresh Incorporation Leads](https://apify.com/tudorlane/uk-new-companies-watch) — `tudorlane/uk-new-companies-watch`

### Ecommerce and products

- [Barcode Lookup API: EAN/UPC to Product & Nutrition](https://apify.com/tudorlane/barcode-product-lookup) — `tudorlane/barcode-product-lookup`
- [Price Tracker: Product Price Drop & Back-in-Stock Alerts](https://apify.com/tudorlane/price-stock-watch) — `tudorlane/price-stock-watch`
- [QR Code & Barcode API: Generate PNG/SVG and Decode Images](https://apify.com/tudorlane/qr-barcode-tools) — `tudorlane/qr-barcode-tools`
- [VIN Decoder API: Make, Model, Year, Specs & Recalls](https://apify.com/tudorlane/vin-decoder) — `tudorlane/vin-decoder`
- [HS Code & Import Duty API: UK Tariff and US HTS Rates](https://apify.com/tudorlane/hs-tariff-code) — `tudorlane/hs-tariff-code`
- [Invoice Parser API: Receipts & PDF Invoices to JSON (OCR)](https://apify.com/tudorlane/invoice-receipt-parse) — `tudorlane/invoice-receipt-parse`
- [Tech Stack Detector: BuiltWith & Wappalyzer Alternative](https://apify.com/tudorlane/tech-stack-detect) — `tudorlane/tech-stack-detect`
- [Check Digit Validator: Card Luhn, ISBN, EAN, ISIN, CUSIP, SEDOL](https://apify.com/tudorlane/card-and-id-checksums) — `tudorlane/card-and-id-checksums`
- [Currency Converter & VAT Rates by Country API (ECB, EU)](https://apify.com/tudorlane/fx-vat-rates) — `tudorlane/fx-vat-rates`

### Health and regulation

- [ICD-10 & NPI Lookup API: HCPCS, LOINC, Drug Labels](https://apify.com/tudorlane/medical-codes-providers) — `tudorlane/medical-codes-providers`
- [Regulation & Legislation Search API: UK, US, EU Law](https://apify.com/tudorlane/regulation-lookup) — `tudorlane/regulation-lookup`
- [Regulatory Change Monitor: UK Legislation & US Federal Register](https://apify.com/tudorlane/regulation-change-watch) — `tudorlane/regulation-change-watch`
- [Air Quality API: Live PM2.5, AQI & Health Advice by City](https://apify.com/tudorlane/air-quality) — `tudorlane/air-quality`
- [Earthquake & Disaster Alerts API: Quakes, Storms, Floods](https://apify.com/tudorlane/earthquake-disaster-alerts) — `tudorlane/earthquake-disaster-alerts`

### Data lookups

- [Wikipedia & Wikidata Facts API: Summary + Key Facts](https://apify.com/tudorlane/wiki-facts) — `tudorlane/wiki-facts`
- [Academic Paper Search API: Crossref, arXiv & DOI Lookup](https://apify.com/tudorlane/academic-paper-search) — `tudorlane/academic-paper-search`
- [Country, Currency & Language Codes API: ISO Lookup](https://apify.com/tudorlane/iso-codes-lookup) — `tudorlane/iso-codes-lookup`
- [IP Geolocation API: Country, City, ASN & Time Zone](https://apify.com/tudorlane/ip-geolocation) — `tudorlane/ip-geolocation`
- [LatAm Tax ID Validator: CPF, CNPJ, RFC, CURP, CUIT, RUT](https://apify.com/tudorlane/latam-id-check) — `tudorlane/latam-id-check`
- [Check Digit Validator: Card Luhn, ISBN, EAN, ISIN, CUSIP, SEDOL](https://apify.com/tudorlane/card-and-id-checksums) — `tudorlane/card-and-id-checksums`
- [Unit Converter API: Length, Weight, Temperature & Cooking](https://apify.com/tudorlane/unit-converter) — `tudorlane/unit-converter`
- [VIN Decoder API: Make, Model, Year, Specs & Recalls](https://apify.com/tudorlane/vin-decoder) — `tudorlane/vin-decoder`
- [Barcode Lookup API: EAN/UPC to Product & Nutrition](https://apify.com/tudorlane/barcode-product-lookup) — `tudorlane/barcode-product-lookup`
- [LEI Lookup API: GLEIF Search by Name, BIC, ISIN + Parents](https://apify.com/tudorlane/lei-lookup) — `tudorlane/lei-lookup`
- [ICD-10 & NPI Lookup API: HCPCS, LOINC, Drug Labels](https://apify.com/tudorlane/medical-codes-providers) — `tudorlane/medical-codes-providers`
- [Postcode & ZIP Code Lookup API Worldwide (Geocode, Reverse)](https://apify.com/tudorlane/world-postcode-lookup) — `tudorlane/world-postcode-lookup`

### Text, files and utilities

- [Token Counter & Text Stats API: Tokens, Language, Readability](https://apify.com/tudorlane/text-toolkit) — `tudorlane/text-toolkit`
- [CSV to JSON Converter: Excel, Parquet & Data Profiler](https://apify.com/tudorlane/file-convert-profile) — `tudorlane/file-convert-profile`
- [JSON Schema Validator API: Validate & Infer Schemas](https://apify.com/tudorlane/json-schema-validate) — `tudorlane/json-schema-validate`
- [Exact Calculator API: Decimal Maths, Percent, Loans, Rounding](https://apify.com/tudorlane/exact-calc) — `tudorlane/exact-calc`
- [Date Parser & Cron API: Natural Language to ISO Dates](https://apify.com/tudorlane/date-parse-cron) — `tudorlane/date-parse-cron`
- [Time Zone Converter & Meeting Planner API (DST-aware)](https://apify.com/tudorlane/timezone-meeting-planner) — `tudorlane/timezone-meeting-planner`
- [Calendar ICS API: Create Invites, Parse Feeds, Free Slots](https://apify.com/tudorlane/ics-calendar-tools) — `tudorlane/ics-calendar-tools`
- [Photo EXIF Metadata Reader & Stripper: GPS, Camera, Date](https://apify.com/tudorlane/image-exif-metadata) — `tudorlane/image-exif-metadata`
- [Page Metadata Extractor API: OpenGraph, JSON-LD, Feeds](https://apify.com/tudorlane/page-metadata-extract) — `tudorlane/page-metadata-extract`
- [Provably Fair Random Picker: Raffles, Draws, Shuffles & IDs](https://apify.com/tudorlane/provable-random) — `tudorlane/provable-random`
- [Markdown to PDF: HTML to PDF and Word (DOCX)](https://apify.com/tudorlane/html-markdown-to-pdf) — `tudorlane/html-markdown-to-pdf`
- [Unit Converter API: Length, Weight, Temperature & Cooking](https://apify.com/tudorlane/unit-converter) — `tudorlane/unit-converter`

## A–Z index

- [`tudorlane/academic-paper-search`](https://apify.com/tudorlane/academic-paper-search) — Academic Paper Search API: Crossref, arXiv & DOI Lookup
- [`tudorlane/actor-trust-check`](https://apify.com/tudorlane/actor-trust-check) — Actor Trust Check: Score Any Apify Actor Before You Call It
- [`tudorlane/adverse-media-watch`](https://apify.com/tudorlane/adverse-media-watch) — Adverse Media Screening: Negative News Monitor for KYC & AML
- [`tudorlane/air-quality`](https://apify.com/tudorlane/air-quality) — Air Quality API: Live PM2.5, AQI & Health Advice by City
- [`tudorlane/airport-airline-lookup`](https://apify.com/tudorlane/airport-airline-lookup) — Airport & Airline Code API: IATA, ICAO, Distance
- [`tudorlane/barcode-product-lookup`](https://apify.com/tudorlane/barcode-product-lookup) — Barcode Lookup API: EAN/UPC to Product & Nutrition
- [`tudorlane/business-id-check`](https://apify.com/tudorlane/business-id-check) — VAT Number Validation: EU VIES, IBAN, LEI & EORI Check
- [`tudorlane/card-and-id-checksums`](https://apify.com/tudorlane/card-and-id-checksums) — Check Digit Validator: Card Luhn, ISBN, EAN, ISIN, CUSIP, SEDOL
- [`tudorlane/company-from-domain`](https://apify.com/tudorlane/company-from-domain) — Company Enrichment API: Domain to Company Profile
- [`tudorlane/company-hiring-watch`](https://apify.com/tudorlane/company-hiring-watch) — Job Postings Scraper & Hiring Watch: Greenhouse, Lever, Ashby
- [`tudorlane/cve-lookup`](https://apify.com/tudorlane/cve-lookup) — CVE Lookup API: Severity, Fixed Versions & Exploited
- [`tudorlane/date-parse-cron`](https://apify.com/tudorlane/date-parse-cron) — Date Parser & Cron API: Natural Language to ISO Dates
- [`tudorlane/domain-availability`](https://apify.com/tudorlane/domain-availability) — Domain Availability Checker API: Bulk RDAP Lookup
- [`tudorlane/domain-watch`](https://apify.com/tudorlane/domain-watch) — Domain WHOIS & Website Watch: SSL, DNS, Expiry, Uptime
- [`tudorlane/earthquake-disaster-alerts`](https://apify.com/tudorlane/earthquake-disaster-alerts) — Earthquake & Disaster Alerts API: Quakes, Storms, Floods
- [`tudorlane/email-verify`](https://apify.com/tudorlane/email-verify) — Email Verifier & Email Validation - Bulk Email Checker
- [`tudorlane/exact-calc`](https://apify.com/tudorlane/exact-calc) — Exact Calculator API: Decimal Maths, Percent, Loans, Rounding
- [`tudorlane/file-convert-profile`](https://apify.com/tudorlane/file-convert-profile) — CSV to JSON Converter: Excel, Parquet & Data Profiler
- [`tudorlane/funding-round-watch`](https://apify.com/tudorlane/funding-round-watch) — Startup Funding Rounds Tracker: SEC Form D & UK Allotments
- [`tudorlane/fx-rate-alert`](https://apify.com/tudorlane/fx-rate-alert) — FX Rate Alert: Currency Move Monitor (ECB Rates)
- [`tudorlane/fx-vat-rates`](https://apify.com/tudorlane/fx-vat-rates) — Currency Converter & VAT Rates by Country API (ECB, EU)
- [`tudorlane/gov-tender-watch`](https://apify.com/tudorlane/gov-tender-watch) — UK Government Tender Watch: New Public Contract Alerts
- [`tudorlane/hs-tariff-code`](https://apify.com/tudorlane/hs-tariff-code) — HS Code & Import Duty API: UK Tariff and US HTS Rates
- [`tudorlane/html-markdown-to-pdf`](https://apify.com/tudorlane/html-markdown-to-pdf) — Markdown to PDF: HTML to PDF and Word (DOCX)
- [`tudorlane/ics-calendar-tools`](https://apify.com/tudorlane/ics-calendar-tools) — Calendar ICS API: Create Invites, Parse Feeds, Free Slots
- [`tudorlane/image-exif-metadata`](https://apify.com/tudorlane/image-exif-metadata) — Photo EXIF Metadata Reader & Stripper: GPS, Camera, Date
- [`tudorlane/interest-rates-yields`](https://apify.com/tudorlane/interest-rates-yields) — Interest Rates & Bond Yields API: Fed, BoE, ECB
- [`tudorlane/invoice-receipt-parse`](https://apify.com/tudorlane/invoice-receipt-parse) — Invoice Parser API: Receipts & PDF Invoices to JSON (OCR)
- [`tudorlane/ip-geolocation`](https://apify.com/tudorlane/ip-geolocation) — IP Geolocation API: Country, City, ASN & Time Zone
- [`tudorlane/iso-codes-lookup`](https://apify.com/tudorlane/iso-codes-lookup) — Country, Currency & Language Codes API: ISO Lookup
- [`tudorlane/job-title-salary`](https://apify.com/tudorlane/job-title-salary) — Job Title to Salary API: SOC Codes & US Pay by State
- [`tudorlane/json-schema-validate`](https://apify.com/tudorlane/json-schema-validate) — JSON Schema Validator API: Validate & Infer Schemas
- [`tudorlane/latam-id-check`](https://apify.com/tudorlane/latam-id-check) — LatAm Tax ID Validator: CPF, CNPJ, RFC, CURP, CUIT, RUT
- [`tudorlane/lead-enrichment`](https://apify.com/tudorlane/lead-enrichment) — Lead Enrichment & Company Enrichment by Domain
- [`tudorlane/lei-lookup`](https://apify.com/tudorlane/lei-lookup) — LEI Lookup API: GLEIF Search by Name, BIC, ISIN + Parents
- [`tudorlane/macro-indicators`](https://apify.com/tudorlane/macro-indicators) — Macroeconomic Data API: Inflation, GDP, Unemployment by Country
- [`tudorlane/market-hours`](https://apify.com/tudorlane/market-hours) — Stock Market Hours API: Is the Exchange Open Now?
- [`tudorlane/medical-codes-providers`](https://apify.com/tudorlane/medical-codes-providers) — ICD-10 & NPI Lookup API: HCPCS, LOINC, Drug Labels
- [`tudorlane/news-feed-search`](https://apify.com/tudorlane/news-feed-search) — News Scraper - Latest News Articles & Headlines API
- [`tudorlane/package-health`](https://apify.com/tudorlane/package-health) — Package Health API: Version, Licence & Vulnerabilities
- [`tudorlane/package-vuln-watch`](https://apify.com/tudorlane/package-vuln-watch) — Package Vulnerability Watch: New CVEs & Releases Monitor
- [`tudorlane/page-change-watch`](https://apify.com/tudorlane/page-change-watch) — Website Change Monitor: Page Change Detection & Diff Alerts
- [`tudorlane/page-metadata-extract`](https://apify.com/tudorlane/page-metadata-extract) — Page Metadata Extractor API: OpenGraph, JSON-LD, Feeds
- [`tudorlane/page-to-markdown`](https://apify.com/tudorlane/page-to-markdown) — Website to Markdown: Web Page and PDF to LLM-ready Text
- [`tudorlane/phone-validate`](https://apify.com/tudorlane/phone-validate) — Phone Number Validator API: Format, Type & Country
- [`tudorlane/price-stock-watch`](https://apify.com/tudorlane/price-stock-watch) — Price Tracker: Product Price Drop & Back-in-Stock Alerts
- [`tudorlane/provable-random`](https://apify.com/tudorlane/provable-random) — Provably Fair Random Picker: Raffles, Draws, Shuffles & IDs
- [`tudorlane/qr-barcode-tools`](https://apify.com/tudorlane/qr-barcode-tools) — QR Code & Barcode API: Generate PNG/SVG and Decode Images
- [`tudorlane/regulation-change-watch`](https://apify.com/tudorlane/regulation-change-watch) — Regulatory Change Monitor: UK Legislation & US Federal Register
- [`tudorlane/regulation-lookup`](https://apify.com/tudorlane/regulation-lookup) — Regulation & Legislation Search API: UK, US, EU Law
- [`tudorlane/rss-feed-watch`](https://apify.com/tudorlane/rss-feed-watch) — RSS Feed Reader & Monitor: New Items, Atom, Feed Finder
- [`tudorlane/sanctions-screening`](https://apify.com/tudorlane/sanctions-screening) — OFAC Sanctions Screening: SDN, UK, EU and UN Lists
- [`tudorlane/sanctions-watchlist`](https://apify.com/tudorlane/sanctions-watchlist) — Sanctions Watchlist Monitor: OFAC, UK, EU & UN Alerts
- [`tudorlane/seo-page-audit`](https://apify.com/tudorlane/seo-page-audit) — SEO Audit: On-Page Checks, Score and Fixes
- [`tudorlane/signup-check`](https://apify.com/tudorlane/signup-check) — Sign-up Fraud Check: Email, Phone & IP Risk Score
- [`tudorlane/site-up-link-check`](https://apify.com/tudorlane/site-up-link-check) — Bulk URL Status Checker: HTTP Codes, Redirects, 404s
- [`tudorlane/sitemap-url-lister`](https://apify.com/tudorlane/sitemap-url-lister) — Sitemap URL Extractor: All Pages of a Website
- [`tudorlane/stock-price`](https://apify.com/tudorlane/stock-price) — Stock Price & Fundamentals API: Quotes, History, SEC Financials
- [`tudorlane/sun-moon-times`](https://apify.com/tudorlane/sun-moon-times) — Sunrise, Sunset & Moon Phase API: Any Place, Any Date
- [`tudorlane/supplier-check`](https://apify.com/tudorlane/supplier-check) — Supplier Check API: UK KYB, Sanctions & Website Risk
- [`tudorlane/tech-stack-detect`](https://apify.com/tudorlane/tech-stack-detect) — Tech Stack Detector: BuiltWith & Wappalyzer Alternative
- [`tudorlane/text-toolkit`](https://apify.com/tudorlane/text-toolkit) — Token Counter & Text Stats API: Tokens, Language, Readability
- [`tudorlane/timezone-meeting-planner`](https://apify.com/tudorlane/timezone-meeting-planner) — Time Zone Converter & Meeting Planner API (DST-aware)
- [`tudorlane/topic-trends`](https://apify.com/tudorlane/topic-trends) — Topic Trends API: Daily Interest from Wikipedia Views
- [`tudorlane/travel-advisories`](https://apify.com/tudorlane/travel-advisories) — Travel Advisory API: UK FCDO & US State Dept by Country
- [`tudorlane/travel-advisory-watch`](https://apify.com/tudorlane/travel-advisory-watch) — Travel Advisory Watch: UK FCDO & US State Dept Alerts
- [`tudorlane/uk-company-check`](https://apify.com/tudorlane/uk-company-check) — Companies House API: UK Company Check & KYB Risk
- [`tudorlane/uk-company-watch`](https://apify.com/tudorlane/uk-company-watch) — UK Company Watch: Companies House Change Monitor
- [`tudorlane/uk-new-companies-watch`](https://apify.com/tudorlane/uk-new-companies-watch) — UK New Companies Watch: Fresh Incorporation Leads
- [`tudorlane/uk-pay-calendar-calculator`](https://apify.com/tudorlane/uk-pay-calendar-calculator) — UK Pay & Calendar Calculator 2026/27
- [`tudorlane/uk-property-sold-prices`](https://apify.com/tudorlane/uk-property-sold-prices) — UK Property Sold Prices: Land Registry Price Paid Data API
- [`tudorlane/unit-converter`](https://apify.com/tudorlane/unit-converter) — Unit Converter API: Length, Weight, Temperature & Cooking
- [`tudorlane/us-company-filings`](https://apify.com/tudorlane/us-company-filings) — SEC EDGAR API: US Company Filings, Financials & Insiders
- [`tudorlane/vin-decoder`](https://apify.com/tudorlane/vin-decoder) — VIN Decoder API: Make, Model, Year, Specs & Recalls
- [`tudorlane/visa-requirements`](https://apify.com/tudorlane/visa-requirements) — Visa Requirements API: Passport to Destination Rules
- [`tudorlane/website-contact-details`](https://apify.com/tudorlane/website-contact-details) — Contact Details Scraper - Emails, Phones & Socials
- [`tudorlane/website-due-diligence`](https://apify.com/tudorlane/website-due-diligence) — Website Due Diligence: Domain Age, SSL, Company & Risk Check
- [`tudorlane/website-safety-check`](https://apify.com/tudorlane/website-safety-check) — Website Safety & Domain Age Checker API (Scam Signals)
- [`tudorlane/wiki-facts`](https://apify.com/tudorlane/wiki-facts) — Wikipedia & Wikidata Facts API: Summary + Key Facts
- [`tudorlane/world-holidays-working-days`](https://apify.com/tudorlane/world-holidays-working-days) — Public Holidays and Working Days API: 150+ Countries
- [`tudorlane/world-postcode-lookup`](https://apify.com/tudorlane/world-postcode-lookup) — Postcode & ZIP Code Lookup API Worldwide (Geocode, Reverse)
- [`tudorlane/world-weather-forecast`](https://apify.com/tudorlane/world-weather-forecast) — Weather Forecast API: Any City or Coordinates Worldwide


## Trust check

Before you call any Apify Actor (ours or someone else's), you can score it with [`tudorlane/actor-trust-check`](https://apify.com/tudorlane/actor-trust-check).

## Publishing these bundles to the official MCP Registry

This repo is ready to publish, but it has **not** been published yet. See [RICHARD_STEPS.md](RICHARD_STEPS.md) for the exact clicks. Before you publish, replace `TudorLane` in every `server.json` and in this README's repository URLs with your GitHub username.
