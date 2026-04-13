# Part 45: Marketing Dashboards

## Learning Objectives
- Understand the principles of effective dashboard design
- Learn how to build dashboards that drive decisions, not just display data
- Create the right dashboards for different audiences and cadences

---

## Why Most Dashboards Fail

Most marketing dashboards are built backward: collect all available data, display it in charts, call it a dashboard. The result: dense screens of numbers and graphs that nobody uses to make decisions.

An effective dashboard is designed from the audience and decisions backward:
1. Who will use this dashboard?
2. What decisions do they need to make?
3. What data would inform those decisions?
4. How should it be displayed to make the right action obvious?

The goal of a dashboard is not to show what happened — it's to show what to do next.

---

## The Three Dashboard Types

### Strategic Dashboard
**Audience:** Senior leadership (VP Marketing, CMO, CEO)
**Cadence:** Monthly/quarterly
**Purpose:** Track progress toward strategic marketing goals; connect marketing activity to business outcomes

**Key metrics:**
- Marketing's contribution to revenue
- Customer acquisition (new customers, CAC)
- Retention and LTV trends
- Marketing ROI
- Progress against quarterly/annual OKRs

**Design principle:** High-level summary. A senior leader should be able to understand the state of marketing in 60 seconds.

### Operational Dashboard
**Audience:** Marketing team leads
**Cadence:** Weekly
**Purpose:** Track performance of active programs; identify what needs attention

**Key metrics:**
- MQLs generated vs. goal
- Channel performance vs. benchmarks (SEO traffic, email engagement, paid CPL)
- Active campaign performance
- Content pipeline health
- Budget paced vs. spent

**Design principle:** Show trend vs. goal for each metric. Make it easy to spot what's red (behind) and what's green (on track).

### Tactical Dashboard
**Audience:** Channel specialists (SEO manager, email manager, paid search manager)
**Cadence:** Daily/weekly
**Purpose:** Optimize specific channel performance in real-time

**Example for paid search:**
- Impressions, clicks, CTR, CPC, conversions, CPA
- Campaign budget pacing
- Ad group performance breakdown
- Keyword performance
- Quality score trends

**Design principle:** Detailed enough to identify specific optimization actions. The specialist should be able to log in and immediately know what to improve.

---

## Dashboard Design Principles

### 1. Start With One Question Per Dashboard

Each dashboard should primarily answer one question:
- "Is marketing on track to hit its goals this quarter?" (Strategic)
- "Which channels need attention this week?" (Operational)
- "Which campaigns should I scale or pause?" (Tactical)

When a dashboard tries to answer too many questions, it answers none well.

### 2. Hierarchy of Visual Attention

Place the most important metric first, in the most prominent position. Hierarchy guides the viewer's eye:
- Top-left: Highest priority metric
- Large chart: The most important trend
- Color: Red/yellow/green status indicators draw immediate attention

### 3. Context Is Everything

A metric without context is meaningless:
- Show trend: Is this metric improving or declining over time?
- Show comparison: Is this above or below goal? Better or worse than last period?
- Show benchmark: How does this compare to industry average?

"Email open rate: 24.3%" means nothing without context. "Email open rate: 24.3% (↑3% MoM; +4% vs. industry benchmark)" tells a story.

### 4. Minimize Metrics

More is less in dashboard design. The optimal number of metrics per dashboard is typically 5-10 for strategic and operational dashboards. Tactical dashboards can go deeper.

If a metric doesn't drive a decision, it doesn't belong on the dashboard.

### 5. Automate Data Refresh

A dashboard that requires manual updating won't get updated. Connect to live data sources so numbers refresh automatically.

---

## Building Your Marketing Dashboard Stack

### Tool Options

| Tool | Best For |
|------|---------|
| **Google Looker Studio** | Free; connects natively to GA4, Google Ads, Search Console; good for most teams |
| **Tableau** | Advanced visualization; enterprise; expensive |
| **Power BI** | Microsoft ecosystem; strong for complex data models |
| **Klipfolio** | Marketing-specific; lots of pre-built templates |
| **HubSpot Reporting** | Best when HubSpot is your CRM; all-in-one |
| **Databox** | Easy to set up; mobile-friendly |

### Data Sources to Connect

Most marketing dashboards pull from:
- **Google Analytics 4:** Website traffic and conversion data
- **Google Search Console:** SEO and keyword performance
- **Google Ads / Meta Ads / LinkedIn Ads:** Paid campaign performance
- **Email platform (HubSpot, Klaviyo, Mailchimp):** Email metrics
- **CRM (Salesforce, HubSpot):** Pipeline and revenue data
- **Social platforms:** Native analytics or connected through Buffer/Sprout Social

---

## The Marketing Dashboard Template

**Recommended sections for an operational marketing dashboard:**

**Section 1: Goal Progress**
- MQL target vs. actual (YTD and current month)
- Revenue contribution vs. target
- Key leading indicators (traffic, email list growth)

**Section 2: Channel Performance**
- Organic search traffic (trend, vs. last month)
- Paid search CPA (trend, vs. target)
- Email click-through rate (trend, by segment)
- Social referral traffic (trend)

**Section 3: Campaign Highlights**
- Active campaigns and their KPIs
- Budget pacing (% spent vs. % through campaign period)

**Section 4: Alerts**
- Metrics significantly below target (auto-flagged red)
- Unusual data anomalies

---

## Dashboard Review Cadence

**Daily:** Automated alert emails for critical metrics out of range (e.g., "conversion rate dropped 30% vs. yesterday")

**Weekly:** Operational dashboard review in team meeting; identify what needs attention this week

**Monthly:** Strategic dashboard review with leadership; compare vs. goals; adjust plans

**Quarterly:** Full strategic review; update dashboard metrics and goals if strategy has shifted

---

## Key Takeaways

- Effective dashboards are designed from audience and decisions backward, not from available data forward
- Three dashboard types serve different needs: strategic (leadership), operational (team), tactical (specialist)
- Every metric needs context: trend, comparison to goal, benchmark
- Automate data refresh; manual dashboards don't get maintained
- 5-10 metrics per strategic dashboard; more is noise

---

## Related Parts

- [Part 41: Marketing Metrics & KPIs](./part-41-marketing-metrics-kpis.md)
- [Part 44: Data Analysis for Marketers](./part-44-data-analysis.md)
- [Part 47: Performance Reporting](./part-47-performance-reporting.md)
- [Part 31: Marketing Analytics](../digital/part-31-marketing-analytics.md)
