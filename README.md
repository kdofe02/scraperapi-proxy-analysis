# ScraperAPI Proxy API Complete Guide: How Does It Work, Which Plan Should You Choose, Are the Credits Worth It — Plus Full Pricing Breakdown, Discount Tips, and Honest Comparison With Competitors

If you've ever built a web scraper and watched it get blocked after 50 requests, you already know the drill. Proxy rotation, CAPTCHA solving, user-agent rotation, JavaScript rendering — managing all of that yourself is basically a second full-time job on top of whatever you actually wanted to scrape. That's the exact problem a **proxy API** is designed to solve. And among the tools in this space, ScraperAPI is one of the most talked-about options for developers who want a clean, single-endpoint solution that handles all of the messy infrastructure for them.

This guide covers everything you need to know before signing up: how the ScraperAPI proxy API actually works under the hood, the full plan and pricing breakdown (including the credit multiplier system that most reviews gloss over), a comparison with competing services, and honest notes on where it shines versus where it struggles.

---

## **What Is a Proxy API — And Why Do Developers Use One?**

Before diving into ScraperAPI specifically, it helps to understand what a **proxy API** is and why someone would pay for one instead of managing proxies themselves.

When you scrape a website at scale, websites see repeated requests from the same IP and block you. The traditional fix is to buy a pool of proxy IPs, rotate them, handle failures, detect blocks, and retry automatically. That infrastructure is annoying to build and expensive to maintain — especially when the sites you're targeting keep updating their anti-bot detection.

A proxy API wraps all of that into a single HTTP endpoint. You send it a URL, it routes the request through a managed proxy pool, handles retries, bypasses CAPTCHAs if needed, and returns either raw HTML or structured JSON. From your code's perspective, it's one API call. What happens behind the scenes is someone else's problem.

ScraperAPI specifically routes requests through a pool of **40 million+ IPs across 50+ countries**, handles CAPTCHA solving automatically, supports JavaScript rendering via headless browsers, and offers structured data endpoints for popular sites like Amazon, Google, Walmart, and eBay. It's been around since 2018 and processes over 36 billion API requests per month, serving companies including Deloitte, Sony, and Alibaba.

> 👉 [Start your free ScraperAPI trial — 5,000 credits, no credit card required](https://www.scraperapi.com/?fp_ref=coupons)

---

## **How ScraperAPI's Credit System Really Works (The Part Everyone Gets Wrong)**

This is the section most reviews skip, and it's the single most important thing to understand before you pick a plan.

ScraperAPI bills on a **credit system**. Every plan gives you a monthly bucket of API credits. When you make a request, you spend credits. Simple enough — until you look at how many credits a single request actually costs.

### **Domain-Based Credit Multipliers**

Not every request costs 1 credit. The cost depends on the target domain:

| **Domain / Type** | **Credits per Request** |
|---|---|
| Normal HTML pages (blogs, news, etc.) | 1 |
| E-commerce — Amazon | 5 |
| Search engines — Google, Bing (all subdomains) | 25 |
| Social media — LinkedIn | 30 |

These multipliers are **automatic** — you don't opt in. The moment ScraperAPI detects the domain, it applies the multiplier. Anti-bot bypass (Cloudflare, DataDome, PerimeterX) adds another **+10 credits per request** on top, also automatically detected.

### **Feature Flag Credit Costs**

You can also add parameters to your requests. Here's what they cost:

| **Parameter** | **Extra Credits** |
|---|---|
| `render=true` (JavaScript rendering) | +10 |
| `screenshot=true` | +10 |
| `premium=true` (premium proxy pool) | +10 |
| `ultra_premium=true` | +30 |
| `premium=true` + `render=true` combined | **+25** (not +20) |
| `ultra_premium=true` + `render=true` combined | **+75** (not +40) |

Note those last two rows. Combined parameter costs are **non-linear** — they cost more than the sum of the individual parts. This is documented but not prominently so, and it's the primary reason users report credits disappearing faster than expected.

### **What Your Plan Credits Actually Buy**

On the Business plan ($299/month, 3 million credits), here's what those credits realistically get you depending on use case:

| **Scraping Scenario** | **Credits/Request** | **Requests from 3M Credits** | **Effective Cost per 1K** |
|---|---|---|---|
| Simple HTML, no JS | 1 | 3,000,000 | $0.10 |
| Amazon product pages | 5 | 600,000 | $0.50 |
| Google SERP results | 25 | 120,000 | $2.49 |
| Amazon + JS rendering | 15 | 200,000 | $1.50 |
| Protected site, ultra-premium + JS | 75 | 40,000 | $7.48 |

The headline "3,000,000 credits" on the Business plan can translate to as few as 40,000 actual requests if you're working with the toughest targets. Run these numbers against your specific use case before picking a plan.

**Important gotchas:**
- Credits do **not** roll over month to month — unused credits expire at renewal
- ScraperAPI only charges for successful requests (HTTP 200 and 404 responses) — failed requests don't cost credits
- 404 responses **do** consume credits, even though the page wasn't found
- Requests cancelled before the 70-second processing window completes are also charged

---

## **Full ScraperAPI Pricing & Plan Comparison**

Here's the complete current plan lineup. All paid plans include JS rendering, rotating proxy pools, CAPTCHA/anti-bot bypass, custom headers, session persistence, automatic retries, unlimited bandwidth, and a 99.9% uptime guarantee. The differences come down to volume, concurrency, geotargeting scope, and access to advanced features like Pay-As-You-Go overflow.

| **Plan** | **Monthly Price** | **Annual Price (per mo)** | **API Credits/Month** | **Concurrent Threads** | **Geotargeting** | **PAYG Overflow** | **Get Started** |
|---|---|---|---|---|---|---|---|
| **Free Trial** | $0 (7 days) | — | 5,000 (trial) + 1,000/mo free | 5 | Limited | No |  [Start Free Trial](https://www.scraperapi.com/?fp_ref=coupons) |
| **Hobby** | $49/mo | $44.10/mo | 100,000 | 20 | US & EU only | No |  [Get Hobby Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Startup** | $149/mo | $134.10/mo | 1,000,000 | 50 | US & EU only | No |  [Get Startup Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Business** | $299/mo | $269.10/mo | 3,000,000 | 100 | Global (50+ countries) | No |  [Get Business Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Scaling** | $475/mo | $427.50/mo | 5,000,000 | 200 | Global | ✅ Yes |  [Get Scaling Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Professional** | $975/mo | $877.50/mo | 10,500,000 | 300 | Global | ✅ Yes |  [Get Professional Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Advanced** | $1,975/mo | $1,777.50/mo | 21,500,000 | 500 | Global | ✅ Yes |  [Get Advanced Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Enterprise** | Custom | Custom | 22M+ | 500+ | Global | ✅ Yes |  [Contact Sales](https://www.scraperapi.com/?fp_ref=coupons) |

**Key things to note:**

- **Geotargeting is plan-gated.** Hobby and Startup only support US and EU proxy locations. If your project requires scraping geo-restricted content from other regions — say, Japanese Amazon listings or Brazilian e-commerce sites — you need at least the Business plan.
- **Pay-As-You-Go is only available from Scaling ($475/mo) upward.** On Hobby, Startup, and Business, running out of credits mid-cycle means you're cut off until renewal or you upgrade. There's no overflow billing on lower tiers.
- **Unlimited analytics history** starts at the Business plan. Hobby and Startup are capped at 30 days of dashboard history.
- **Annual billing gets you 10% off** automatically — no promo code needed, just select annual at checkout.

### **Which Plan Should You Actually Pick?**

**Hobby ($49/mo)** is the right call if you're running a personal project, testing an idea, or doing small-scale monitoring — checking competitor prices on a handful of products, scraping a few dozen pages a day. For plain HTML pages, 100,000 credits goes a long way. For Amazon or Google, do the credit math first.

**Startup ($149/mo)** suits small SaaS products, solo developers building real scraping workflows, or agencies running jobs for a handful of clients. The jump to 1 million credits and 50 concurrent threads is meaningful. Still US/EU geo only.

**Business ($299/mo)** is the first tier that opens global geotargeting, which is often the actual deciding factor. If you need to scrape from specific countries outside the US and EU, this is your entry point. Also adds unlimited dashboard history and 100 concurrent threads.

**Scaling ($475/mo) and above** is where Pay-As-You-Go overflow kicks in, meaning you never get hard-capped mid-month. If your project depends on scraping as infrastructure (other systems rely on it), being cut off at the end of the billing cycle is unacceptable — the Scaling plan removes that risk.

---

## **Are There ScraperAPI Discount Codes?**

The most reliably verified discount method right now is **annual billing**, which automatically takes 10% off every plan — no code entry required. The annual prices are already reflected in the table above.

For new users on monthly billing, the promo code **START10** gives 10% off your first month on any paid subscription plan. This is the most consistently verified code across multiple sources as of mid-2026, applicable to new accounts only.

There are lots of third-party coupon sites claiming 25–70% off codes, but independent verification suggests these are largely inaccurate or expired. The 10% annual discount and the START10 first-month code are the current confirmed offers.

> 👉 [Sign up with this link to access the current free trial offer](https://www.scraperapi.com/?fp_ref=coupons)

---

## **What ScraperAPI Is Actually Good At**

Not every proxy API is equally good across all scraping targets. ScraperAPI is genuinely strong in some areas and noticeably weaker in others.

### **Where It Performs Well**

Independent benchmarks from Scrapeway (2026) show ScraperAPI performing strongly on mainstream e-commerce and real estate:

| **Target Site** | **Success Rate** | **Average Speed** |
|---|---|---|
| Zillow | 100% | ~10.5s |
| Etsy | 99% | ~4.8s |
| Amazon | 98% | ~6.5s |
| LinkedIn | 95% | ~17.8s |
| Walmart | 93% | ~11.4s |
| Indeed | 90% | ~15.8s |

The **Structured Data Endpoints (SDEs)** are a genuine strength. ScraperAPI offers 18 structured data endpoints across Amazon (product details, search, competitor offers), Google (SERP, Shopping, Maps, News, Jobs), Walmart (product, search, category, reviews), eBay, and Redfin. Instead of returning raw HTML that you have to parse yourself, these endpoints return clean, structured JSON. The Amazon SDE in particular returns 18+ fields including pricing, ratings, BSR, images, and seller info, supporting 21 regional marketplaces.

**Geotargeting** (on Business and above) lets you set a `country_code` parameter on any request to route it through a proxy in that specific country — no extra credit cost, it's included.

### **Where It Falls Short**

| **Target** | **Success Rate** | **Notes** |
|---|---|---|
| Instagram | 0% | Complete failure |
| Twitter/X | 0% | Complete failure |
| Booking.com | 0% | Complete failure |
| Realtor.com | 12% | Unreliable |

Social media is effectively a dead zone for ScraperAPI. Instagram, Twitter/X, and Booking.com show 0% success rates in independent testing. If social data is your primary use case, this is the wrong tool.

ScraperAPI also **explicitly forbids scraping content behind login walls** — it doesn't support form-filling, two-factor authentication, or complex auth flows. Session persistence via `session_number` is supported, but that's for maintaining the same IP across sequential requests, not for authenticated scraping.

There's also a **10-minute forced cache** applied to difficult targets, meaning you may receive results up to 10 minutes old on heavily protected sites. For time-sensitive data like live pricing or stock levels, this is worth knowing upfront.

---

## **ScraperAPI vs. Competitors: A Fair Comparison**

At the ~$300/month price point, here's how effective cost-per-request stacks up across common scenarios:

### **Basic HTML Scraping (No JS, No Premium Proxy)**

| **Provider** | **Plan** | **Price** | **Requests from Plan** | **Cost per 1K** |
|---|---|---|---|---|
| ScrapingBee | Business | $249 | 3,000,000 | $0.08 |
| **ScraperAPI** | **Business** | **$299** | **3,000,000** | **$0.10** |
| Scrapfly | Startup | $250 | 2,500,000 | $0.10 |
| ZenRows | Business | $300 | ~1,071,000 | $0.28 |
| Bright Data | PAYG | ~$300 | ~200,000 | $1.50 |

### **JavaScript Rendering Required**

| **Provider** | **Plan** | **Price** | **Requests from Plan** | **Cost per 1K** |
|---|---|---|---|---|
| ScrapingBee | Business | $249 | 600,000 | $0.42 |
| Scrapfly | Startup | $250 | 416,667 | $0.60 |
| **ScraperAPI** | **Business** | **$299** | **300,000** | **$1.00** |
| ZenRows | Business | $300 | ~214,000 | $1.40 |
| Bright Data | PAYG | ~$300 | ~200,000 | $1.50 |

### **Premium Proxy + JS Rendering (Protected Sites)**

| **Provider** | **Plan** | **Price** | **Requests from Plan** | **Cost per 1K** |
|---|---|---|---|---|
| Bright Data | PAYG | ~$300 | ~200,000 | $1.50 |
| ScrapingBee | Business | $249 | 120,000 | $2.08 |
| **ScraperAPI** | **Business** | **$299** | **120,000** | **$2.49** |
| Scrapfly | Startup | $250 | 80,645 | $3.10 |
| ZenRows | Business | $300 | ~42,857 | $7.00 |

**Takeaway:** For basic HTML scraping, ScraperAPI is competitive but slightly pricier than ScrapingBee. For JavaScript-rendered pages, ScrapingBee and Scrapfly beat it on cost. For protected sites with premium proxies and JS rendering, ScraperAPI sits in the middle — better than ZenRows, behind Bright Data. The "right" choice depends almost entirely on your specific target mix.

---

## **Getting Started with the ScraperAPI Proxy API: The Basics**

Integration is genuinely simple. The quickest way is to use ScraperAPI as a proxy replacement — pass your target URL as a parameter to ScraperAPI's endpoint along with your API key:

python
import requests

api_key = "YOUR_API_KEY"
url = "https://www.amazon.com/dp/B08N5WRWNW"

response = requests.get(
    "http://api.scraperapi.com",
    params={
        "api_key": api_key,
        "url": url,
        "autoparse": "true"
    }
)

print(response.json())


For JavaScript-rendered pages, add `render=true`. For premium proxies, add `premium=true`. For country-specific requests, add `country_code=de` (or whatever country code you need).

**Free Trial Process:**
1. Sign up at ScraperAPI — no credit card required
2. You get 1,000 free credits permanently, plus 5,000 credits for your first 7 days
3. Use the API Playground in the dashboard to test your specific URLs and check their credit cost before running at scale
4. Use the Domain Multiplier tool in the dashboard to look up credit costs for any URL you plan to scrape

> 👉 [Create your free ScraperAPI account and start with 5,000 trial credits](https://www.scraperapi.com/?fp_ref=coupons)

---

## **Beyond the Core API: Async Scraping and DataPipeline**

ScraperAPI isn't just a synchronous proxy endpoint. There are two additional product layers worth knowing about.

### **Async Scraper Service**

For high-volume jobs where you're sending millions of requests, the **Async API** lets you submit URL batches and collect results asynchronously. Instead of waiting for each request to complete before sending the next one, you fire off thousands of requests and retrieve results when they're ready. This is the recommended approach for large-scale, recurring data collection jobs.

### **DataPipeline (No-Code)**

DataPipeline is ScraperAPI's no-code scheduled scraping tool. You configure a data collection job — URLs, schedule, output format, webhook destination — without writing any code. It handles execution, retries, and delivery automatically.

One important catch: DataPipeline uses a **different, higher credit schedule** than the standard API. A basic normal request costs **6 credits** in DataPipeline versus **1 credit** via the standard API. If you set up a no-code pipeline expecting standard credit costs, you'll burn through credits six times faster than you might expect. This is documented, but it's buried in the technical docs rather than prominently featured on the pricing page.

---

## **What Real Users Say**

ScraperAPI sits at **4.5/5 on Trustpilot** (42 reviews), **4.4/5 on G2** (16 reviews), and **4.6/5 on Capterra** (62 reviews), with the Capterra Ease of Use sub-rating hitting an impressive **4.9/5**. That last number tracks — the integration experience really is that smooth for most developers. You can drop ScraperAPI into an existing scraping workflow in under 30 minutes.

The praise clusters around ease of setup, clean documentation, and reliability on well-supported targets. The criticism clusters around two things: the credit multiplier system being less transparent than it should be, and reliability on harder or less common targets. A notable Reddit thread described a user being quoted one price for an Amazon scraping plan, only to discover the 5x credit multiplier hadn't been explained upfront — their 60 million credit plan effectively became 12 million Amazon requests. That kind of surprise is entirely avoidable if you run the math beforehand, but it's also on ScraperAPI to make this more prominent.

---

## **Is ScraperAPI Right for You?**

Here's the short version:

**ScraperAPI is a strong fit if:**
- You're a developer building data pipelines in Python, Node.js, or similar
- Your primary targets are Amazon, Google, Walmart, Zillow, or mainstream e-commerce sites
- You want clean, structured JSON without building your own parsers
- You need high-volume scraping (100K+ requests/month) with reliable infrastructure

**ScraperAPI is probably not the right fit if:**
- Your primary targets are Instagram, Twitter/X, Booking.com, or social media generally
- You need to scrape content behind login walls
- You want predictable, multiplier-free per-request pricing
- You need real-time data where a 10-minute cache on difficult targets would be a problem

And before you commit: use the free trial. The 7-day trial with 5,000 credits is genuinely enough to test your real target sites, check the credit costs in the dashboard, and decide whether the numbers work for your use case. No credit card required, no guessing.

> 👉 [Try ScraperAPI free — 5,000 credits, 7-day trial, no card needed](https://www.scraperapi.com/?fp_ref=coupons)

---

## **Quick FAQ**

**Does every request cost 1 credit?**
No. Standard pages cost 1 credit, but Amazon costs 5, Google and Bing cost 25, LinkedIn costs 30. Add JavaScript rendering (+10), premium proxies (+10), or ultra-premium proxy + JS (+75 combined), and costs multiply further. Check the Domain Multiplier in your dashboard before running at scale.

**What happens if I run out of credits mid-month?**
On Hobby, Startup, and Business plans, you either upgrade to the next tier or wait for renewal. Pay-As-You-Go overflow only activates on Scaling ($475/mo) and above.

**Do credits roll over?**
No. Unused credits expire at each billing cycle reset.

**Is there a free trial?**
Yes — 5,000 credits for the first 7 days after signup, plus 1,000 free credits per month on the permanent free tier. No credit card required for either.

**Is there a money-back guarantee?**
ScraperAPI offers a 7-day no-questions-asked refund policy on paid plans.

**Can I cancel anytime?**
Yes, from the dashboard or by contacting support. No cancellation fees.

**Is there a discount code?**
Annual billing gives you an automatic 10% discount. New users on monthly plans can use **START10** for 10% off the first month (new accounts only, subscription plans).
