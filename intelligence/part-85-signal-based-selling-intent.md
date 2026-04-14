# Part 85: Signal-Based Selling & B2B Intent Data

> **Section 11: Marketing Intelligence & Decision Systems**

---

## Learning Objectives

- Understand intent data sources and how they reveal purchase readiness signals
- Build a signal-based marketing and sales workflow that prioritizes the right accounts at the right time
- Identify the data quality, privacy, and attribution research gaps in intent data use

---

## The Old Model vs. Signal-Based Marketing

Traditional B2B marketing operates on a time-based cadence: send emails on Tuesday, run ads continuously, contact accounts quarterly based on ICP (Ideal Customer Profile) segmentation. The implicit assumption: buying readiness is distributed uniformly across the account universe, and consistent outreach will capture whichever accounts happen to be in-market at each touchpoint.

Signal-based marketing rejects this assumption. Buying readiness is not evenly distributed — at any given time, a specific fraction of your addressable market is actively researching solutions like yours, experiencing the trigger conditions that create buying urgency, or showing behavioral patterns that precede purchases. Identifying those accounts and prioritizing engagement toward them — rather than distributing outreach uniformly — is the core signal-based proposition.

---

## The Intent Signal Ecosystem

**1. First-Party Behavioral Signals**
Your own data: website visits (especially high-intent pages like pricing, case studies, and competitive comparison), form fills, content downloads, product trial activity, email engagement. These are the highest-confidence signals because they represent direct interaction with your brand.

**2. Third-Party Intent Data**
Data providers (Bombora, G2 Buyer Intent, TechTarget, 6sense, Demandbase) aggregate behavioral data across networks of B2B content publishers. When accounts research topics relevant to your product category across these networks, buying stage signals are generated — without those accounts having visited your website. This is "dark web" intent in the B2B sense: your prospect is researching but hasn't made themselves visible to you yet.

**3. Hiring Signals**
LinkedIn job postings reveal organizational priorities. A company hiring 10 data engineers and a Chief Data Officer signals an upcoming data infrastructure investment. A company adding a VP of Revenue Operations signals CRM and RevOps tooling evaluation. Many ABM platforms (Clay, Keyplay, Common Room) now automate hiring signal monitoring and scoring.

**4. Technographic Signals**
The technology stack a company uses (detected through job postings, web scraping, and provider data from BuiltWith and Datanyze) reveals integration requirements, displacement opportunities, and budget indicators.

**5. Trigger Events**
Funding announcements (new budget allocation), executive changes (new VP often re-evaluates vendor stack), M&A activity (consolidation creates tool overlap), and expansion signals (new office openings, hiring surges) are high-confidence buying trigger indicators.

**6. Product Usage Signals (PQL — Product Qualified Leads)**
For products with free tiers or trials, usage signals within the product itself are the highest-fidelity intent data available. An account that hits usage limits, adds team members, or explores enterprise features is signaling readiness for a paid conversation.

---

## Building a Signal-Scoring System

Signal-based marketing requires synthesizing multiple signal types into actionable account scores. The framework:

```
ACCOUNT SCORE = 
  (Fit Score × w₁) + (Intent Score × w₂) + (Engagement Score × w₃)

Where:
  Fit Score    = ICP match (firmographic/technographic alignment)
  Intent Score = Research signals (third-party intent + trigger events)
  Engagement Score = First-party behavioral signals

Weights (w₁, w₂, w₃) calibrated to historical conversion data
```

High-fit + high-intent + low-engagement = top priority for outbound outreach (in-market but not yet engaged)
High-fit + low-intent + high-engagement = nurture for conversion trigger
Low-fit + high-intent = may signal ICP expansion opportunity to investigate

---

## Real-World Example: 6sense and Account Engagement Prediction

6sense's "Dark Funnel" platform aggregates intent signals to predict which accounts are in-market before they raise their hand. Early adopters report significant improvements in sales development efficiency: less time cold-calling accounts with no buying intent, more time engaging accounts showing research activity. Some customers report 2–3x improvements in opportunity creation rates when sales teams prioritize signal-based accounts over territory-based lists.

---

## Research Gaps

**Gap 1: Third-party intent data accuracy**
Third-party intent data aggregators claim to identify in-market accounts based on research behavior across publisher networks. But the accuracy of these signals — how reliably they predict actual purchase timelines — is largely vendor-reported. Independent validation studies comparing third-party intent signal accuracy to actual conversion outcomes are extremely limited.

**Gap 2: Signal decay rates**
How long after a positive intent signal does buying urgency persist? A company researching cybersecurity solutions this week may have completely different priorities in eight weeks. Research on intent signal half-lives — the optimal engagement window after different signal types — is underdeveloped.

**Gap 3: Privacy implications of B2B intent data**
Third-party B2B intent data is collected from business activity, but individuals within companies have privacy interests. GDPR's applicability to B2B behavioral data collected across publisher networks is actively contested. The legal landscape for third-party intent data use in different jurisdictions is unstable.

---

## Key Takeaways

- Signal-based marketing identifies in-market accounts through intent signals rather than distributing outreach uniformly
- Signal types: first-party behavioral, third-party intent, hiring signals, technographics, trigger events, and product usage (PQL)
- Synthesize signals into account scores combining Fit, Intent, and Engagement dimensions
- The highest-value use case: identifying high-fit accounts in active research mode before they engage with any vendor
- Research gaps: third-party data accuracy validation, signal decay rates, and GDPR implications of B2B intent data

---

## Related Parts

- [Part 33: Lead Generation](../acquisition/part-33-lead-generation.md)
- [Part 34: Lead Nurturing](../acquisition/part-34-lead-nurturing.md)
- [Part 52: Predictive Analytics & Machine Learning](../futuristic/part-52-predictive-analytics-ml.md)
- [Part 81: Marketing Intelligence Systems](./part-81-marketing-intelligence-systems.md)
- [Part 94: Account-Based Marketing at Enterprise Scale](./part-94-account-based-marketing.md)
