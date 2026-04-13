# Part 44: Churn Prevention Operations

## Learning Objectives
- Distinguish between churn types and understand their distinct prevention strategies
- Build a churn prediction model using leading behavioral signals
- Implement a proactive churn prevention program anchored in customer health scoring
- Design win-back campaigns for different churn segments
- Establish operational rhythms (QBRs, check-ins, dunning) to systematically reduce churn

---

## Understanding Churn: Types and Dimensions

Not all churn is the same. Treating it as a monolith leads to misdiagnosed solutions.

### Voluntary vs Involuntary Churn

| Type | Definition | Root Cause | Prevention Strategy |
|---|---|---|---|
| **Voluntary** | Customer actively cancels | Lack of value, better alternative, budget cut | Value realization, engagement, positioning |
| **Involuntary** | Subscription lapses due to payment failure | Credit card expired, bank decline | Dunning management, payment retry logic |

**Important:** In many SaaS businesses, **involuntary churn accounts for 20–40% of total churn**—and it is entirely recoverable with proper payment operations. This is often the fastest-wins bucket.

### Early vs Late Churn

| Type | Timing | Cause | Response |
|---|---|---|---|
| **Early churn** | First 30–90 days | Failed onboarding, product-market fit miss | Onboarding fix, ICP tightening |
| **Mid-lifecycle churn** | 3–12 months | Engagement decay, feature gaps, competition | Re-engagement, success programs |
| **Late churn** | 12+ months | Strategic shift, budget restructuring, acquisition | Executive relationship, contract renegotiation |

---

## Churn Prediction Models and Signals

The goal of churn prediction is to identify **at-risk customers before they decide to leave**, not after. Leading signals always outperform lagging signals.

### Behavioral Leading Signals

**High churn risk indicators:**
- Login frequency dropping by 50%+ over 30 days
- Key feature usage declining week-over-week
- Number of active users on a B2B account declining
- Support tickets with negative sentiment or unresolved escalations
- Pricing page or cancellation flow visits
- Non-response to CSM outreach
- NPS score of 6 or below (detractor)

**Low churn risk indicators:**
- Expanding usage (new users added, more data processed)
- Integration connections growing
- Regular QBR engagement
- High NPS or positive support interactions
- Usage growing toward plan limits

### Building a Churn Score

A simple, effective churn score for B2B SaaS:

```
Health Score = (Engagement Score × 0.4) + 
               (Adoption Score × 0.3) + 
               (Relationship Score × 0.2) + 
               (Commercial Score × 0.1)
```

| Component | What to Measure |
|---|---|
| **Engagement** | Login frequency, session depth, feature breadth |
| **Adoption** | % of purchased features actively used |
| **Relationship** | NPS, QBR attendance, CSM responsiveness |
| **Commercial** | Payment history, contract age, renewal proximity |

Assign **Red / Yellow / Green** tiers and trigger different interventions for each.

---

## Proactive Churn Prevention Tactics

### For Red Accounts (High Risk)
- **Immediate CSM outreach:** Phone or video call within 24 hours of entering Red status
- **Executive sponsor engagement:** Pull in an executive to signal commitment
- **Emergency success plan:** Written 30-day plan with named milestones and accountability
- **Feature gap review:** Understand specifically what value is missing
- **Concession if warranted:** Discount, extended term, or added services—but only after understanding the root cause

### For Yellow Accounts (At-Risk)
- **Scheduled check-in call:** Structured conversation around goals and progress
- **Usage report with recommendations:** Show the customer their data + personalized tips
- **Feature adoption campaign:** Target the specific features they haven't used
- **Peer success story:** Send a relevant case study showing comparable companies' results

### For Green Accounts (Healthy)
- **Expansion conversation:** Strong health is the best time to introduce upsell
- **Advocacy invitation:** Ask for a case study, referral, or review
- **Executive alignment:** Deepen the relationship beyond the day-to-day user

---

## Customer Health Scoring in Practice

**Tooling options:**
- **Native CSM platforms:** Gainsight, ChurnZero, Totango, Catalyst—purpose-built with health scoring, playbooks, and workflow automation
- **CRM-based:** HubSpot or Salesforce with custom health score fields fed by product data via Segment or API
- **Lightweight:** Spreadsheet-based scoring for early-stage companies, with Zapier automation for alert triggers

**Operational cadence:**
- Health scores should update **daily or in real-time** based on product usage signals
- CSMs should review their entire book of business **weekly** sorted by health score
- Red account escalations should trigger **same-day** notifications to CS leadership

---

## QBR and Success Check-In Programs

### Quarterly Business Reviews (QBRs)
A QBR is not a product demo—it is a **strategic business conversation** that anchors your product in the customer's goals.

**QBR agenda structure (60 minutes):**
1. **Business goals review (10 min):** What were their goals last quarter? Did they achieve them?
2. **Product value recap (15 min):** Data-driven proof of value (usage stats, ROI metrics, outcomes)
3. **Roadmap preview (10 min):** Upcoming features relevant to their use case
4. **Success planning (15 min):** Goals for next quarter + named success milestones
5. **Expansion discussion (10 min):** Organic introduction of additional solutions if health is green

**QBR best practices:**
- Prepare a **customized deck** with their actual usage data—never a generic template
- Always have the customer's **executive sponsor** in the room
- Send the recap with action items within 24 hours
- Log all commitments in your CRM

### Mid-Quarter Check-Ins
For high-ACV accounts, supplement QBRs with monthly 30-minute check-in calls. Less formal, more operational—focused on blockers and short-term wins.

---

## Win-Back Campaign Strategy

Even after churn, recovery is possible. The key is **speed, relevance, and authenticity**.

### Segmentation by Churn Recency and Reason

| Segment | Timing | Approach |
|---|---|---|
| **Recent churners (< 30 days)** | Immediate | Personal outreach from CSM; acknowledge issue; offer resolution |
| **Mid-term churners (30–90 days)** | 2-email sequence | New features + resolved issues; social proof; limited offer |
| **Long-lapsed (90+ days)** | 3-touch campaign | Lead with new value prop, not old product; strong incentive |
| **Involuntary churners** | Immediate dunning flow | Payment recovery focus; no product sell needed |

**Win-back email framework:**
- Subject: Acknowledge their departure; signal change ("What's new at [Product] since you left")
- Body: 2–3 specific improvements directly relevant to their stated reason for leaving
- CTA: Offer a no-friction re-entry point (re-activate in one click, or book a 15-min catch-up)

---

## Failed Payment Recovery: Dunning Management

Dunning is the process of recovering revenue from failed payments. Done well, it recaptures 40–60% of involuntary churn.

### Payment Retry Logic
- **Immediately:** Retry 24 hours after first failure
- **Day 3:** Second retry with different card network routing if available
- **Day 7:** Final retry before grace period expiry

### Dunning Email Sequence
| Day | Message | Tone |
|---|---|---|
| 0 | "Payment failed—update your card" | Neutral, urgent |
| 2 | "Action required: your account" | Slightly urgent |
| 5 | "Your access is at risk" | High urgency |
| 7 | "Last chance before suspension" | Final warning |
| 10 | Post-suspension win-back | Empathetic, solution-oriented |

**Tactics:**
- Use **smart retries** (Stripe Radar or equivalent) that retry at statistically optimal times
- Offer **alternative payment methods** (ACH, wire, purchase order for enterprise)
- For annual contracts, consider proactive **credit card expiry outreach** 45 days before expiry

---

## Churn Analysis Framework

After churn occurs, systematic analysis turns individual losses into systemic improvements.

**Exit interview process:**
- Survey all churned customers within 7 days (automated, 3 questions max)
- Follow up with personal outreach for high-value churned accounts
- Code churn reasons into categories: product gap, price, competition, business closure, not enough value

**Churn categorization:**
| Category | % of Churn | Action Owner |
|---|---|---|
| Product gap | 30% | Product team |
| Poor onboarding | 20% | CS + Product |
| Price sensitivity | 15% | Pricing/Revenue |
| Competitive loss | 15% | Product + Marketing |
| Business closure | 10% | Unavoidable |
| Low engagement/no champion | 10% | CS + Sales (ICP review) |

Share monthly churn analysis reports with product, sales, and executive leadership—churn data is one of the most valuable product signals available.

---

## Key Takeaways

- **Separate voluntary from involuntary churn** in your analysis—they require completely different solutions
- Build a **health scoring system** that updates automatically and triggers intervention playbooks
- **Proactive prevention** outperforms reactive win-back by a wide margin—intervene at Yellow, not Red
- Dunning management alone can recover 20–40% of involuntary revenue loss with minimal effort
- Churn analysis is a **product intelligence function**—make it a regular input to your roadmap

---

## Actionable Next Steps

1. Audit last quarter's churned accounts and categorize churn reasons
2. Build a simple health score (even in a spreadsheet) using 3–5 behavioral signals
3. Implement a basic dunning sequence in your billing platform this week
4. Schedule QBRs for your top 20% of accounts by ARR
5. Create a Red/Yellow/Green escalation playbook with named response actions and owners
