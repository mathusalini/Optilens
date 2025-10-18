# Optilens

# 🛒 Web Scraping Amazon Pendant Light Data using Oxylabs

## 🔍 Why Oxylabs Was Chosen

Amazon’s product pages are **dynamic, heavily protected, and legally restricted** for direct scraping.  
Traditional scraping tools like `BeautifulSoup` or `Selenium` often fail because of:

- Frequent **CAPTCHAs** and **IP blocking**
- **Dynamic JavaScript-rendered** content
- **Anti-bot protection** systems (Akamai / Cloudflare)
- **Legal restrictions** against direct scraping

To overcome these limitations, we chose **Oxylabs E-commerce Scraper API**, a **compliant and enterprise-grade** data collection platform.

### ✅ Advantages of Using Oxylabs

1. **High Success Rate**
   - Handles Amazon’s anti-bot protection automatically.
   - Rotates millions of IPs via residential and datacenter proxies.

2. **Structured JSON Output**
   - Returns clean, machine-readable data (no HTML parsing needed).

3. **JavaScript Rendering**
   - Automatically loads dynamic elements such as prices, ratings, and images.

4. **Scalable & Cloud-Based**
   - No need to manage browsers, proxies, or headless servers.
   - Supports concurrent scraping of multiple pages.

5. **Legally Compliant**
   - Oxylabs provides scraping as a service under data aggregation compliance standards.

---

## 🧠 What Data (Features) Are Extracted

Using Oxylabs’ **Amazon Search Source**, we can collect key product attributes from the *“Pendant Light”* category.

| Feature | Description |
|----------|-------------|
| **Title** | Product name or title |
| **ASIN** | Amazon Standard Identification Number (unique product ID) |
| **Price** | Product price (numeric value) |
| **Currency** | Currency code (USD, GBP, etc.) |
| **Rating** | Average customer rating (e.g., 4.7 / 5) |
| **Reviews** | Number of customer reviews |
| **Image** | URL of the main product image |
| **URL** | Direct link to the product page |
| **Page Number** | Indicates the source search page |
| **Category / Domain** | The Amazon domain (e.g., amazon.com, amazon.co.uk) |

These fields are returned as **structured JSON** and then converted into a **CSV** or **DataFrame** for analysis.

---

## ⚙️ Example Workflow

1. **Send a POST request** to Oxylabs’ API with:
   ```json
   {
     "source": "amazon_search",
     "domain": "com",
     "query": "pendant light",
     "start_page": 1,
     "pages": 2
   }

**Why Supabase?**
- Provides a cloud SQL database (PostgreSQL)
- Keeps your scraped Amazon data organized and persistent
- Enables realtime access for dashboards and apps
- No manual backend coding required
- Integrates easily with Python and React

**In this project:**
We use Supabase to store pendant light product data (titles, prices, ratings, reviews, image URLs, and product links) fetched via Oxylabs.  
This allows long-term market analysis, visualization, and future mobile app integration.
