# Part 47: KPI Command Center

## Learning Objectives
- Build a rigorous marketing KPI framework tied to business outcomes
- Understand top-level, channel-level, and funnel metrics
- Design dashboards that drive action, not just reporting
- Establish reporting rhythms that create accountability
- Foster a data-driven decision culture across marketing teams

---

## Why a KPI Command Center Matters

Marketing without measurement is guesswork. Yet most teams suffer from the opposite problem: **metric overload**. They track dozens of numbers, run weekly reports nobody reads, and still make decisions based on gut feel. A KPI Command Center solves this by creating a single source of truth—organized by decision-making level, updated at the right cadence, and connected directly to business outcomes.

---

## The KPI Hierarchy

Structure your metrics in three tiers:

| Tier | Who Uses It | Cadence | Examples |
|------|-------------|---------|---------|
| **Business** | C-Suite, Board | Monthly/Quarterly | Revenue, CAC, LTV, Payback Period |
| **Channel** | Marketing Directors | Weekly | CPL, ROAS, CTR, Pipeline Sourced |
| **Execution** | Campaign Managers | Daily | Impressions, CPC, Open Rate |

---

## Top-Level Business Metrics

### Revenue
- **New MRR/ARR**: revenue added from new customers
- **Expansion MRR**: revenue from upsells and cross-sells
- **Churned MRR**: revenue lost; marketing influences retention through lifecycle programs

### Customer Acquisition Cost (CAC)
**Formula**: Total Sales & Marketing Spend ÷ New Customers Acquired

- Segment by channel: paid CAC vs organic CAC vs product-led CAC
- Benchmark: SaaS B2B median CAC payback is 15–18 months; best-in-class is under 12
- **Blended CAC** hides channel-level waste—always break it down

### Lifetime Value (LTV)
**Formula**: ARPU × Gross Margin % ÷ Churn Rate

- LTV:CAC ratio of 3:1 or higher signals healthy unit economics
- Below 2:1 means you're likely over-investing in acquisition

### Payback Period
**Formula**: CAC ÷ (ARPU × Gross Margin %)

- Target under 12 months for SaaS; under 6 months for high-velocity SMB
- Longer payback periods require more capital efficiency discipline

### Churn Rate
- **Logo churn**: percentage of customers lost
- **Revenue churn (net)**: accounts for expansion; negative net churn means expansion outpaces losses
- Marketing's role: influence onboarding content, nurture sequences, and loyalty programs

---

## Channel-Level KPIs

### Paid Search
- Cost Per Click (CPC), Click-Through Rate (CTR), Quality Score, Conversion Rate, ROAS

### Paid Social
- CPM, CTR, Cost Per Lead (CPL), Cost Per Acquisition (CPA), Frequency

### SEO / Organic
- Organic sessions, keyword rankings, Domain Rating, Pages Per Session, Organic-Sourced Pipeline

### Email
- Open Rate, Click Rate, Reply Rate, Unsubscribe Rate, Revenue Per Email

### Content / Inbound
- Blog sessions, Time on Page, Lead Capture Rate, Content-Assisted Pipeline

---

## Funnel Conversion Benchmarks by Industry

| Stage | B2B SaaS | eCommerce | Agency | Marketplace |
|-------|----------|-----------|--------|-------------|
| Visitor → Lead | 2–5% | 2–4% | 3–7% | 1–3% |
| Lead → MQL | 20–40% | N/A | 30–50% | N/A |
| MQL → SQL | 30–50% | N/A | 40–60% | N/A |
| SQL → Close | 20–30% | N/A | 25–40% | N/A |
| Cart → Purchase | N/A | 2–4% | N/A | 5–10% |

Use these as starting benchmarks; build your own internal cohorts over 6–12 months.

---

## Designing a Marketing Dashboard

### Tool Selection

| Tool | Best For | Notes |
|------|----------|-------|
| **Looker** | Enterprise BI, SQL-native | Requires data warehouse (BigQuery, Snowflake) |
| **Tableau** | Complex visualization, large datasets | Strong for finance/ops crossover |
| **GA4** | Web/app behavior, funnel analysis | Free; limited CRM integration |
| **HubSpot / Salesforce Reports** | CRM-native pipeline reporting | Easy setup; less flexible |
| **Custom (Metabase, Redash)** | Startups with raw data access | Free/low cost, SQL-driven |

### Dashboard Design Principles
- **One number per question**: don't make users interpret grids of data
- **Traffic light status**: red/yellow/green against targets
- **Trend lines over snapshots**: a number without context misleads
- **Drill-down capability**: summary → breakdown → raw events
- **Mobile-ready**: leadership views dashboards on phones

---

## Reporting Rhythms

### Daily
- Ad spend pacing vs budget
- Conversion volume alerts (significant drops/spikes)
- Website uptime and error rate
- Automated Slack/email digest

### Weekly
- Channel performance vs prior week and target
- Pipeline sourced by channel
- Lead volume and quality trends
- Team standup: wins, issues, experiments live

### Monthly
- CAC, LTV, payback vs targets
- Full funnel conversion review
- Content and SEO performance
- Budget vs actuals reconciliation
- Stakeholder report to leadership

### Quarterly
- Strategic KPI review (see Part 50)
- Channel mix reallocation
- Benchmark comparisons (industry data)
- Headcount and tooling ROI

---

## Data-Driven Decisions vs HiPPO Decisions

The **HiPPO problem** (Highest Paid Person's Opinion) is one of the most costly issues in marketing organizations. When senior leaders override data with intuition, teams stop measuring because "it doesn't matter anyway."

**Combat HiPPO decisions by:**
- Pre-agreeing on success metrics *before* campaigns launch
- Documenting decisions with data rationale in a decision log
- Running experiments instead of debates (see Part 49)
- Presenting data as stories with clear recommendations, not spreadsheets
- Building psychological safety so junior analysts can challenge senior opinions with evidence

> **Real-world example**: At Booking.com, any team member can launch an A/B test. Data wins over opinion—this culture contributed to running 1,000+ experiments per year and industry-leading conversion rates.

---

## Building a Data Culture in Marketing Teams

### Hire for Curiosity + Comfort with Ambiguity
- Marketing analysts who can write SQL and explain results to non-technical stakeholders are rare—invest in them

### Define "Done" to Include Measurement
- No campaign ships without a measurement plan: what success looks like, how it's tracked, when it's evaluated

### Weekly Data Reviews
- Not just reporting—active interpretation: "What does this mean? What do we do differently?"

### Celebrate Learning from Failure
- A test that fails teaches more than a campaign that "probably worked"
- Create a **test library** documenting hypotheses, results, and learnings

### Democratize Access
- Give every marketer access to dashboards and basic query tools
- Data gatekeeping slows velocity and creates bottlenecks

---

## Key Takeaways

- **Structure metrics in tiers**: business → channel → execution, each with the right owner and cadence
- **CAC, LTV, and payback period** are the north star metrics for marketing efficiency
- **Dashboard design is UX**: built for decisions, not data dumps
- **Reporting rhythms create accountability**—daily for operations, weekly for channels, monthly for strategy
- **Data culture beats data tools**: invest in processes and people, not just software
- **Kill HiPPO decisions** by pre-committing to metrics and running experiments instead of debates

---

## Actionable Next Steps

1. **This week**: Audit your current metrics—list every KPI you track and eliminate any that don't connect to a business decision
2. **This month**: Build a single executive dashboard with no more than 10 metrics, with red/yellow/green status
3. **This quarter**: Establish daily, weekly, and monthly reporting rhythms with assigned owners
4. **Ongoing**: Run a monthly "data culture" session where the team reviews what they learned, not just what happened
