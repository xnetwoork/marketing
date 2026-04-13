# Part 48: Attribution Framework — MMM + MTA Practical Stack

## Learning Objectives
- Understand why attribution is fundamentally difficult and imperfect
- Distinguish between single-touch, multi-touch, and statistical attribution models
- Know when to use Marketing Mix Modeling (MMM) vs Multi-Touch Attribution (MTA)
- Run incrementality tests to validate attribution claims
- Build a practical attribution stack for your company stage
- Navigate privacy-era attribution challenges post iOS 14

---

## The Attribution Problem

Every marketer faces the same question: **which touchpoints actually drove the sale?**

A B2B buyer may see a LinkedIn ad, read a blog post, attend a webinar, receive three nurture emails, and respond to a cold outreach before signing. Which channel gets credit?

Attribution answers this question—but every model makes trade-offs between simplicity, accuracy, and data requirements. The goal isn't perfect attribution (it doesn't exist). The goal is **good enough attribution to make better budget decisions than your competitors**.

---

## Single-Touch Attribution Models

### First-Click Attribution
- 100% credit goes to the first touchpoint
- **Strength**: identifies top-of-funnel awareness drivers
- **Weakness**: ignores everything that happened after initial discovery
- **Use when**: measuring brand awareness campaigns

### Last-Click Attribution
- 100% credit goes to the final touchpoint before conversion
- **Strength**: simple; favored by Google Ads by default
- **Weakness**: over-credits bottom-funnel channels (paid brand search, retargeting)
- **Use when**: evaluating direct response campaigns in isolation

### Last Non-Direct Click
- Ignores direct traffic; credits the last identifiable channel
- Common in GA4 default reports

> **Real-world problem**: A company runs awareness YouTube ads for 3 months. Last-click shows YouTube contributing zero conversions. The team cuts the budget. Six weeks later, leads drop 40%. Single-touch attribution created a false picture.

---

## Multi-Touch Attribution (MTA)

MTA distributes credit across multiple touchpoints in the conversion path.

### Linear Attribution
- Equal credit to every touchpoint
- **Strength**: acknowledges all interactions
- **Weakness**: treats a brand impression the same as a demo request click

### Time-Decay Attribution
- More credit to touchpoints closer to conversion
- **Strength**: reflects recency bias in purchase decisions
- **Best for**: short sales cycles (eCommerce, SMB SaaS)

### U-Shaped (Position-Based)
- 40% first touch, 40% last touch, 20% distributed to middle
- Favors acquisition and closing touchpoints
- **Best for**: B2B where first and last interactions are highest signal

### Data-Driven Attribution (DDA)
- Machine learning model trained on your actual conversion paths
- Assigns fractional credit based on incremental contribution
- **Requires**: minimum ~3,000 conversions/month for statistical validity
- Available in Google Ads and GA4

| Model | Complexity | Data Required | Best For |
|-------|-----------|---------------|---------|
| First/Last Click | Low | Minimal | Single-channel evaluation |
| Linear | Low | Low | Early-stage, simple funnels |
| Time-Decay | Medium | Medium | Short sales cycles |
| U-Shaped | Medium | Medium | B2B with defined sales stages |
| Data-Driven | High | High | Scaled eCommerce or PLG SaaS |

---

## Marketing Mix Modeling (MMM)

MMM is a **statistical regression model** that measures the impact of marketing spend on business outcomes using historical aggregate data—no cookies or user-level tracking required.

### How MMM Works
1. Collect time-series data: spend by channel, revenue/conversions, external factors (seasonality, competitor activity, pricing changes)
2. Run regression analysis to isolate contribution of each variable
3. Output: **response curves** showing diminishing returns per channel

### When to Use MMM
- Large brand budgets where individual user tracking is impractical
- Privacy-constrained environments (no cookies, walled gardens)
- Long sales cycles with complex, multi-week journeys
- Budgets over $1M/month where statistical significance is achievable

### MMM Limitations
- **Lags**: models reflect the past; market dynamics shift
- **Minimum data requirement**: 2+ years of weekly data preferred
- **Granularity**: channel-level, not campaign or creative level
- **Cost**: custom MMM builds cost $50K–$200K; tools like Meridian (Google) and Robyn (Meta) offer open-source alternatives

---

## Incrementality Testing

**The gold standard of attribution.** Incrementality testing asks: *would this conversion have happened anyway without this touchpoint?*

### Holdout Test Design
1. Randomly split audience into exposed group and holdout (control) group
2. Suppress ads (or emails, or content) for the holdout
3. Measure conversion rate difference
4. **Incremental lift** = (Exposed CVR − Holdout CVR) ÷ Holdout CVR

### Geo-Based Incrementality
- Run ads in test markets, pause in control markets
- Compare revenue outcomes controlling for baseline differences
- Used by Facebook, Google, and Northbeam as default

> **Real-world example**: Airbnb ran incrementality tests on brand search ads and found that 89% of conversions would have happened organically without the paid click. They cut brand bidding and reallocated millions to acquisition.

---

## Building a Practical Attribution Stack

### Stage 1: Seed/Early (<$50K/month spend)
- **UTM parameters** on every link (mandatory)
- GA4 with basic goals configured
- CRM (HubSpot) with source tracking
- **Self-reported attribution survey** on sign-up form: "How did you hear about us?"
- Cost: ~$0

### Stage 2: Growth ($50K–$500K/month)
- Multi-touch attribution tool: **Northbeam**, **Triple Whale**, or **Rockerbox**
- Paid media API integrations (Google, Meta, LinkedIn)
- Revenue attribution in CRM by source
- Quarterly geo holdout tests for top channels
- Cost: $2K–$10K/month

### Stage 3: Scale ($500K+/month)
- Full MTA platform + MMM (annual or quarterly model runs)
- Custom data warehouse (BigQuery/Snowflake) as single source of truth
- Dedicated marketing analytics team
- Monthly incrementality testing cadence
- Cost: $20K–$100K+/month

---

## Privacy-Era Attribution (Post iOS 14)

### The iOS 14+ Impact
Apple's App Tracking Transparency (ATT) framework eliminated IDFA for ~60–70% of iOS users who opt out. Facebook reported a $10B revenue impact in 2022 from measurement degradation.

**What broke:**
- Facebook pixel attribution windows shortened from 28-day to 7-day
- User-level cross-site tracking eliminated
- Retargeting audience sizes collapsed

### The Cookieless Future
Google's deprecation of third-party cookies in Chrome (delayed to 2025) will further erode MTA accuracy.

**Adaptations:**
- **First-party data**: capture email/phone at every touchpoint; build owned audiences
- **Server-side tracking**: bypass browser-level blocking via Conversions API (Meta CAPI), Google Enhanced Conversions
- **Modeled conversions**: platforms fill gaps with ML modeling
- **Contextual targeting**: replace behavioral with content-based ad targeting

### Self-Reported Attribution Surveys
Underrated but powerful. A simple post-sign-up question—*"How did you hear about us?"*—captures dark social, word of mouth, podcasts, and other invisible channels.

- Tools: Typeform, native form field, Segment
- Benchmark: 40–60% response rate on sign-up flow
- Insight: typically reveals podcasts, newsletters, and peer recommendations that UTMs miss entirely

---

## Key Takeaways

- **No attribution model is correct**; choose one that fits your data maturity and sales cycle
- **Single-touch models mislead**—they systematically over-credit or under-credit channels
- **MMM and incrementality testing** are the most reliable measures but require investment
- **Build your attribution stack in stages** matched to spend level and data capability
- **Privacy changes have permanently degraded MTA**—diversify measurement approaches
- **Self-reported surveys capture dark social** that no tool can measure

---

## Actionable Next Steps

1. **Immediately**: Audit UTM parameter consistency across all campaigns—broken UTMs are the #1 attribution failure point
2. **This month**: Add a "How did you hear about us?" field to sign-up/contact forms
3. **This quarter**: Select and implement an MTA tool appropriate for your spend level
4. **This year**: Run at least one geo-holdout incrementality test on your largest channel
