# Part 31: Marketing Analytics

## Learning Objectives
- Understand the marketing analytics ecosystem and what to measure at each stage
- Learn how to set up a reliable measurement foundation
- Use data to make better marketing decisions and communicate value to stakeholders

---

## Why Marketing Analytics Matters

Marketing without measurement is guessing. You might be spending 80% of your budget on channels that produce 20% of your results — and not know it. Analytics reveals what's actually working, enables confident optimization, and justifies marketing investment to leadership.

But analytics is routinely done poorly. Common failures:
- Tracking too many metrics without a hierarchy of importance
- Optimizing for proxy metrics (clicks, impressions) instead of business outcomes (revenue, customers)
- Ignoring attribution complexity and crediting all results to the last click
- Data collection without analysis — reports that nobody acts on

The goal of marketing analytics is not to produce dashboards. The goal is to make better decisions.

---

## The Analytics Foundation: Tracking Setup

Before analysis, you need reliable data collection. The analytics stack typically includes:

### Website Analytics
**Google Analytics 4 (GA4):** The standard for tracking website traffic, user behavior, and conversions.

Key setup steps:
- Install GA4 tracking code on every page
- Configure conversion events (form submissions, purchases, signups, key page visits)
- Link to Google Search Console (organic search data)
- Link to Google Ads (paid search performance)
- Set up filters to exclude internal traffic
- Configure goals and funnels

### Conversion Tracking
Track the specific actions that matter:
- **Form submissions** (lead generation)
- **Account signups** (product adoption)
- **Purchases** (revenue)
- **Calls** (phone conversions)

Every conversion should fire a tracking event. If you can't track a conversion, you can't optimize for it.

### UTM Parameters
UTM (Urchin Tracking Module) parameters are URL tags that tell analytics where traffic came from:
- `utm_source`: Where traffic originated (google, facebook, newsletter)
- `utm_medium`: The channel type (cpc, email, organic, social)
- `utm_campaign`: The specific campaign name
- `utm_content`: The specific ad or link (for A/B testing)

**Example:** `yoursite.com/pricing?utm_source=linkedin&utm_medium=paid-social&utm_campaign=q1-awareness&utm_content=video-ad`

Use UTMs consistently on all paid, email, and social links.

### CRM and Revenue Data
Connect marketing data to actual revenue. What matters is not just which channel drives the most traffic, but which channel drives customers with the highest lifetime value.

---

## The Analytics Hierarchy

Not all metrics are equal. Organize by type:

**Business outcome metrics** (most important):
- Revenue attributed to marketing
- New customers acquired
- Customer lifetime value (LTV)
- LTV:CAC ratio

**Leading indicators** (predict business outcomes):
- Marketing Qualified Leads (MQLs)
- Sales Qualified Leads (SQLs)
- Trial signups
- Free-to-paid conversion rate

**Channel performance metrics**:
- Organic traffic and keyword rankings
- Email open and click rates
- Ad CTR, CPC, conversion rate
- Social reach and engagement

**Vanity metrics** (informative but not decision-driving):
- Total page views
- Social followers
- Email list size

The hierarchy: optimize toward business outcomes; use channel metrics to guide tactical decisions; be skeptical of vanity metrics.

---

## Key Measurement Frameworks

### The Marketing Funnel Metrics

Map metrics to funnel stages:

| Funnel Stage | Key Metrics |
|--------------|------------|
| Awareness | Organic reach, ad impressions, brand search volume, new visitor sessions |
| Consideration | Time on site, content downloads, email subscriptions, return visits |
| Conversion | Lead form submissions, trial signups, purchase conversion rate, CAC |
| Retention | Churn rate, LTV, NPS, product engagement, repeat purchase rate |
| Advocacy | Referral rate, NPS, user-generated content, review volume |

### Cohort Analysis
Group customers by acquisition date and track their behavior over time. Reveals:
- Which acquisition cohorts have the best retention?
- Which channels produce customers with the highest LTV?
- How has onboarding changes affected activation rate over time?

---

## Attribution: Connecting Touchpoints to Results

Attribution is the practice of assigning credit to the marketing touchpoints that contributed to a conversion. It's one of the hardest problems in marketing analytics.

**Common attribution models:**

| Model | How Credit Is Assigned | When to Use |
|-------|----------------------|-------------|
| Last-click | 100% to final touchpoint before conversion | Simple, common default |
| First-click | 100% to first touchpoint | Understanding awareness drivers |
| Linear | Equal credit to all touchpoints | General view of multi-touch impact |
| Time-decay | More credit to recent touchpoints | Short sales cycles |
| Data-driven | Algorithm distributes credit based on patterns | When you have enough data |

No model is perfect. Use multi-touch attribution to understand the full picture; use last-click for optimization decisions within specific channels.

---

## Building a Measurement Cadence

**Daily:** Monitor for anomalies — traffic spikes or drops, conversion rate changes, ad budget issues

**Weekly:** Channel performance review — what worked this week? What needs adjustment?

**Monthly:** Performance vs. goals — are we on track? Where are the gaps? What needs strategic adjustment?

**Quarterly:** Deep-dive analysis — cohort performance, attribution review, channel efficiency, recommendations for next quarter strategy

---

## Analytics Tools

| Purpose | Tools |
|---------|-------|
| Web analytics | Google Analytics 4, Plausible, Mixpanel |
| SEO analytics | Google Search Console, SEMrush, Ahrefs |
| Paid advertising | Google Ads Manager, Meta Ads Manager |
| Email analytics | HubSpot, Klaviyo, Mailchimp |
| Social analytics | Native platform analytics, Sprout Social, Buffer |
| Business intelligence | Looker, Tableau, Google Looker Studio |
| Product analytics | Mixpanel, Amplitude, Heap |

---

## Key Takeaways

- Analytics should drive better decisions, not just produce reports
- Build your tracking foundation before campaigns: conversion events, UTMs, GA4 setup
- Organize metrics in a hierarchy: business outcomes → leading indicators → channel metrics
- Attribution is complex; use multiple models to build a full picture
- Establish a regular measurement cadence: daily monitoring, weekly review, monthly analysis, quarterly strategy

---

## Related Parts

- [Part 10: Setting SMART Goals](../strategy/part-10-smart-goals.md)
- [Part 41: Marketing Metrics & KPIs](../measurement/part-41-marketing-metrics-kpis.md)
- [Part 42: Attribution Modeling](../measurement/part-42-attribution-modeling.md)
- [Part 45: Marketing Dashboards](../measurement/part-45-marketing-dashboards.md)
- [Part 46: ROI Calculation](../measurement/part-46-roi-calculation.md)
