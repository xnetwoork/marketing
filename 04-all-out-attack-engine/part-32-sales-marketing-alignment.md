# Part 32: Sales + Marketing Strike Alignment

## Learning Objectives
- Understand why sales-marketing misalignment is a primary growth killer
- Build a service-level agreement (SLA) framework between sales and marketing
- Align on lead definitions: MQL, SQL, and SAL
- Design seamless handoff processes that prevent lead leakage
- Create shared reporting and dashboards that unify accountability
- Implement a RevOps model that scales alignment as the company grows

---

## Why Sales-Marketing Misalignment Kills Growth

Sales and marketing misalignment is one of the most costly and underestimated problems in B2B growth. Research from Aberdeen Group found that companies with strong sales-marketing alignment achieve **20% annual revenue growth**, while companies with poor alignment see **4% revenue decline** in the same period.

**The misalignment tax:**
- **Sales wastes time on bad leads:** Marketing sends volume, sales chases unqualified prospects, conversion rates collapse
- **Marketing doesn't learn from closed-lost deals:** Without feedback loops, marketing optimizes for metrics that don't drive revenue
- **Attribution warfare:** Sales says marketing generates bad leads; marketing says sales doesn't follow up
- **Duplicated effort:** Both teams create similar content and assets independently
- **Customer experience fragmentation:** Prospects receive inconsistent messaging from pre- to post-sale

> **Real-World Example:** HubSpot documented their own sales-marketing alignment journey in building their $1B ARR business. Their "Smarketing" approach (an internal alignment program) reduced CAC by 30% and improved close rates by 25% within 18 months of implementation.

**The root cause of misalignment is almost never people — it's missing systems, definitions, and processes.**

---

## SLA Framework Between Sales and Marketing

A **Service Level Agreement (SLA)** makes the sales-marketing relationship contractual, not aspirational. It defines what each team commits to delivering, removes ambiguity, and creates shared accountability.

### Marketing SLAs to Sales

Marketing commits to:
- **Lead volume:** Deliver X MQLs per month by segment/territory
- **Lead quality:** Minimum X% MQL-to-SQL conversion rate (typical target: 20–30%)
- **Response enablement:** All MQLs have complete firmographic and behavioral data for sales context
- **Handoff speed:** MQLs entered in CRM within [X] hours of qualifying action
- **Content support:** Sales has X pieces of relevant content per buying stage per persona

### Sales SLAs to Marketing

Sales commits to:
- **Speed to lead:** Contact every MQL within [X] hours (best practice: <5 hours; top-performing teams: <1 hour)
- **Attempt volume:** Minimum X contact attempts before marking lead as unresponsive
- **Disposition accuracy:** Every lead is dispositioned (qualified, disqualified, nurture) within X business days
- **Feedback quality:** Provide closed-lost reasons with sufficient detail for marketing optimization
- **Content usage:** Use marketing-approved materials in a defined percentage of outreach sequences

### SLA Review Cadence

| Frequency | Activity |
|---|---|
| Weekly | Lead volume and conversion rate pulse check |
| Monthly | Full SLA performance review, identify gaps |
| Quarterly | SLA renegotiation and adjustment based on business changes |

---

## Lead Definition Alignment

The most common source of misalignment is undefined or inconsistently applied lead definitions. Every revenue team must agree on:

### Marketing Qualified Lead (MQL)

**Definition:** A prospect who has demonstrated sufficient interest and fits the ICP profile to warrant sales engagement.

**MQL criteria framework (lead scoring):**
| Attribute | Points |
|---|---|
| Fits ICP job title | 15 |
| Fits target company size | 10 |
| Fits target industry | 10 |
| Downloaded bottom-funnel content | 20 |
| Visited pricing page | 25 |
| Attended webinar | 15 |
| Opened 3+ emails in sequence | 10 |
| **MQL threshold** | **≥50 points** |

Revisit MQL thresholds quarterly based on MQL-to-SQL conversion data.

### Sales Accepted Lead (SAL)

**Definition:** An MQL that sales has reviewed and confirmed meets minimum qualification criteria before investing contact effort.

SAL is the quality gate between marketing handing off and sales actively working. If SAL rates are <80% of MQLs, marketing's ICP targeting needs adjustment. If SAL rates are >95%, the MQL threshold may be too high (losing good leads).

### Sales Qualified Lead (SQL)

**Definition:** A lead that sales has contacted, confirmed budget/authority/need/timeline (BANT or equivalent), and has entered into an active sales cycle.

**SQL conversion benchmarks by source:**

| Lead Source | MQL-to-SQL Benchmark |
|---|---|
| Inbound organic/SEO | 25–35% |
| Paid search (non-brand) | 20–30% |
| Paid social | 15–25% |
| Outbound SDR | 30–50% (self-sourced) |
| Events and webinars | 20–35% |
| Referral | 40–60% |

---

## Handoff Processes

A broken handoff is where most leads die. The handoff process must be fast, complete, and tracked.

### Handoff Checklist

Before a lead is handed to sales, marketing must ensure the CRM record contains:
- [ ] First/last name, company, title, email, phone (if available)
- [ ] Lead source and specific campaign/ad that generated the lead
- [ ] Behavioral data: pages visited, content downloaded, forms submitted
- [ ] Lead score at time of handoff
- [ ] Account context: company size, industry, existing relationship notes
- [ ] Suggested first message based on engagement signals

### Handoff Workflow

1. Lead reaches MQL threshold in CRM/MAP (HubSpot, Salesforce, Marketo)
2. Automated notification sent to assigned SDR/AE with full context
3. Lead appears in SDR's priority queue with engagement data surfaced
4. SDR reviews (SAL decision) within 2 business hours
5. If accepted: first contact attempt within 4 hours
6. If rejected: SDR provides rejection reason (routed to nurture or disqualified)
7. If no response to 5 attempts: lead returned to marketing nurture sequence

---

## Shared Reporting and Dashboards

Shared visibility creates shared accountability. Both teams should review the same data from the same source of truth.

**Recommended shared dashboard metrics:**

| Metric | Marketing View | Sales View |
|---|---|---|
| Leads by source | Volume, CPL, MQL rate | Lead quality by source |
| MQL-to-SQL conversion | Quality signal for targeting | Efficiency of qualification |
| SQL-to-Close rate | Downstream quality validation | Win rate by segment/source |
| Pipeline contribution by channel | ROI by marketing source | Where to prioritize follow-up |
| Revenue by lead source | Full-funnel ROI | Best sources to request more |
| Average deal cycle | Content gap identification | Pacing and forecast accuracy |
| Lead response time | SLA compliance | Speed-to-revenue correlation |

**Dashboard tools:** Salesforce Dashboards, HubSpot Revenue Reports, Tableau, Looker, or a unified data warehouse (BigQuery + Looker Studio).

---

## Joint Planning Sessions

Alignment is built in planning sessions, not just reporting sessions.

**Quarterly Joint Planning Agenda:**
1. Review prior quarter: What did marketing deliver vs. SLA? What did sales deliver vs. SLA?
2. Discuss closed-lost analysis: What patterns emerge? What objections keep surfacing?
3. Review top performing and worst performing campaigns/sources
4. Plan next quarter: Campaigns, content needs, target segments, headcount assumptions
5. Refresh ICP and persona definitions based on real closed-won data
6. Update lead scoring model with new conversion data

**Monthly check-in (30 minutes):**
- SLA performance vs. targets
- Pipeline health: are we on track?
- Top 3 feedback items from sales to marketing this month
- Content and campaign coordination for the month ahead

---

## Feedback Loops from Sales to Marketing

Sales is the closest team to the market. Their feedback is priceless for marketing optimization — but only if captured systematically.

**Structured feedback mechanisms:**

| Mechanism | Frequency | Output |
|---|---|---|
| Closed-lost interview (select deals) | Monthly | Objection themes, competitive intelligence |
| Win/loss survey in CRM | Every deal | Quantitative win/loss data by segment |
| "Voice of the customer" call recording review | Weekly | Exact language prospects use (for copy) |
| Sales rep feedback form | Weekly | Top 3 leads that were great; top 3 that wasted their time |
| Objection tracking log | Ongoing | Evolving objection map by persona and stage |

**Action protocol:** Marketing reviews all sales feedback weekly. Any pattern seen in 3+ deals in a month triggers a marketing response (new content, updated landing page copy, revised ICP criteria).

---

## Revenue Operations (RevOps) Model

RevOps is the organizational structure that makes sales-marketing alignment sustainable at scale by creating a unified operations function:

**RevOps owns:**
- CRM administration and data quality
- Lead routing and assignment rules
- Attribution modeling and reporting
- Sales and marketing technology stack
- Process documentation and training
- SLA monitoring and enforcement

**RevOps reporting structure:** Typically reports to the COO or CFO — neutral between sales and marketing, accountable to revenue outcomes.

**When to hire a RevOps function:**
- When you have both a dedicated marketing team and a dedicated sales team (5+ people combined)
- When lead volume exceeds 500 MQLs per month
- When your tech stack includes 3+ integrated tools (CRM + MAP + sales engagement)

---

## Alignment Playbook: SMB vs. Enterprise

| Dimension | SMB Alignment | Enterprise Alignment |
|---|---|---|
| Lead volume | High volume, low-touch | Lower volume, high-touch |
| Lead routing | Simple rules (geography, product) | Complex scoring + territory + account-based |
| Handoff speed | Hours | Same day |
| Sales cycle | Days to weeks | Months to quarters |
| Persona complexity | 1–2 buyers | 6–10 stakeholder committee |
| Content needed | Self-serve, educational | Multi-stakeholder, ROI-focused |
| Alignment cadence | Monthly | Weekly |
| Key shared metric | Lead-to-close rate, CAC | Pipeline contribution, ARR |

**ABM for enterprise:** Enterprise alignment requires Account-Based Marketing (ABM) — marketing and sales targeting the same named accounts in coordinated, personalized campaigns rather than running lead generation independently.

---

## Key Takeaways

- **Misalignment is a system problem, not a people problem** — fix the process before assigning blame
- The SLA framework makes accountability explicit and measurable for both teams
- Consistent lead definitions (MQL, SAL, SQL) are the foundation of shared understanding — revisit quarterly
- Speed to lead is the single highest-impact variable sales controls — every hour of delay reduces close rates materially
- Shared dashboards replace "my data vs. your data" with "our data" — a cultural and operational shift
- RevOps is not overhead — it's the operating system that scales alignment as the company grows

---

## Actionable Next Steps

1. **This week:** Schedule a 60-minute session with your sales counterpart to align on MQL definition. Document the agreed criteria in writing.
2. **Next 2 weeks:** Build a shared revenue dashboard that both sales and marketing review in the same meeting.
3. **Ongoing:** Implement a monthly closed-lost review. Every pattern identified should trigger a marketing action within 30 days.
