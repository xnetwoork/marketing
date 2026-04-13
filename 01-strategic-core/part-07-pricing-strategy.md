# Pricing Strategy by Value Density

## Learning Objectives

By the end of this section, you will be able to:
- Understand and apply the major pricing models used in modern businesses
- Use the value density concept to determine the right price point
- Apply price anchoring and framing to increase perceived value
- Design tiered packaging that drives upsells
- Conduct a rigorous price testing methodology
- Navigate the key differences between B2B and B2C pricing

---

## The Core Pricing Principle: Value Density

**Value density** is the ratio of perceived value delivered to the price charged. A high-value-density offer feels like a bargain even at a premium price. A low-value-density offer feels expensive at any price.

The goal of pricing strategy is not to charge as much as possible. It's to **maximize value density from the customer's perspective** — while capturing a sustainable share of the value you create.

> **Formula:** Value Density = (Customer's perceived value of outcome) ÷ (Price paid)

The higher this ratio, the easier the sale, the lower churn, and the stronger the word of mouth.

---

## The Major Pricing Models

### 1. Value-Based Pricing

Price is derived from the economic value delivered to the customer.

**How it works:**
- Quantify the outcome (cost saved, revenue generated, time freed)
- Determine buyer's willingness to pay (WTP) for that outcome
- Price at 10–25% of quantified value (your "share" of the value created)

**Best for:** B2B SaaS, professional services, high-stakes software
**Pros:** Highest margin potential; pricing justified by ROI
**Cons:** Requires deep customer insight; hard to scale without segmentation

---

### 2. Cost-Plus Pricing

Price = cost to produce + target margin.

**How it works:** Calculate COGS (or CAC + delivery cost), add the desired margin.

**Best for:** Physical goods, agencies, commoditized services
**Pros:** Simple; protects margins
**Cons:** Leaves money on the table if customers would pay more; ignores competitive dynamics

---

### 3. Competitive Pricing

Price is set relative to what competitors charge.

**Strategies:**
- **Parity pricing:** Match competitors; compete on non-price dimensions
- **Penetration pricing:** Price below competitors to capture market share quickly
- **Premium pricing:** Price above competitors; requires clear differentiation justification

**Best for:** Established categories with visible competitive pricing
**Pros:** Market-informed; easy to benchmark
**Cons:** You're anchored to others' pricing decisions, not your value creation

---

### 4. Freemium Pricing

A free tier drives adoption; a paid tier captures conversion.

**Freemium mechanics:**
- **Feature-gated:** Free = limited features; paid = full features (Notion, Slack)
- **Capacity-gated:** Free = limited usage; paid = more capacity (Spotify, Dropbox)
- **Time-gated:** Free = trial period; paid = ongoing access (Salesforce, HubSpot)

**Freemium benchmarks:**
- Median free-to-paid conversion: 2–5%
- Best-in-class: 10–15%
- Key variable: how much free value do you give before gating?

**Best for:** PLG products with viral or bottom-up adoption dynamics
**Pros:** Low acquisition cost; large top of funnel
**Cons:** High infrastructure cost per free user; can commoditize your offer

---

### 5. Usage-Based Pricing (UBP)

Price scales directly with how much the customer uses the product.

**UBP models:**
| Unit | Example |
|---|---|
| API calls | Twilio, OpenAI, Stripe |
| Data volume | Snowflake, BigQuery |
| Events / tasks | Zapier, HubSpot (contacts) |
| Compute time | AWS Lambda, Vercel |
| Messages sent | SendGrid, Mailgun |

**Pros:** Aligns cost with value; reduces friction to adoption; grows with customer success
**Cons:** Unpredictable revenue; high churn risk if usage drops; difficult to forecast

**Hybrid usage-based model:** Minimum committed spend + usage above threshold (best of both worlds — floor for the vendor, flexibility for the buyer).

---

## Price Anchoring and Framing

Price is not objective. It's interpreted in context. **Anchoring** and **framing** change how buyers perceive the same price.

### Anchoring Techniques

- **High anchor first:** Present your enterprise/high tier before the mid tier; mid tier looks reasonable by comparison
- **Comparison anchor:** "Replace 5 tools at $200/mo each" → your $300/mo product looks like a discount
- **Cost-of-inaction anchor:** "Your current process costs $X in labor per month" → your $Y price looks like savings

### Framing Techniques

| Reframe | Example |
|---|---|
| Per user per day | "$3/user/day" feels smaller than "$90/user/month" |
| Cost vs. investment | "This is not a cost — it's a $50K revenue investment" |
| Percentage of outcome | "Our fee is 10% of the revenue we generate for you" |
| Loss frame | "Every month without this costs you $X" (more powerful than gain frame) |

---

## Pricing Psychology

| Principle | Application |
|---|---|
| **Charm pricing** | $97 feels significantly cheaper than $100; applies to SMB, not enterprise |
| **Decoy pricing** | Add a "bad value" tier that makes your preferred tier look obvious |
| **Choice architecture** | Limit to 3 tiers maximum; more than 3 causes decision paralysis |
| **Middle option bias** | ~60% of buyers choose the middle tier — design your ideal tier to sit there |
| **Social proof on pricing pages** | "Most popular" label drives 20–35% more middle tier conversions |
| **Annual upfront discount** | Offer 2 months free (17% discount) for annual payment; improves cash flow and retention |

---

## Packaging & Tier Design

Tiers are not just price points — they're **value propositions** for different customer segments.

### Good tier design:
- Each tier solves for a distinct customer need (not just "more features")
- Clear good/better/best logic — each tier is obviously more valuable
- Feature gates are *meaningful* — buyers feel the difference between tiers
- Upgrade path is visible from lower tiers (in-app prompts, usage limits)

### Sample SaaS tier framework:

| Tier | Target | Price logic | Gate |
|---|---|---|---|
| **Starter** | Individual / small team | Low friction; get them in | Basic features; limited seats/volume |
| **Professional** | Growing team | Core product + scale | Advanced features; higher limits |
| **Enterprise** | Large org | Custom; high deal size | SSO, admin, security, SLAs, support |

**Common packaging mistakes:**
- Gating features customers need to get value (kills activation)
- Over-engineering tiers (10 plans creates paralysis and support burden)
- Not differentiating on outcome — tiers feel like arbitrary price points

---

## Price Testing Methodology

Pricing is a product. It should be tested, measured, and iterated.

**Step 1: Van Westendorp Price Sensitivity Meter**
Ask four questions to your ICP:
1. At what price would this be so expensive you would not consider it?
2. At what price would it be expensive but you'd still consider it?
3. At what price would it be a bargain — great value for money?
4. At what price would it be so cheap you'd question the quality?

The overlap of acceptable prices reveals your optimal price range.

**Step 2: Willingness-to-Pay Survey**
Present a single price to each respondent: "At $X/month, how likely are you to purchase?" Vary the price across respondents. Build a demand curve.

**Step 3: A/B Test Live Pricing**
Run different price points in live purchase flows. Measure not just conversion rate but **revenue per visitor** (a higher price with slightly lower conversion rate may win on revenue).

**Step 4: Cohort Analysis**
Track whether customers acquired at different price points have different churn rates, expansion rates, and LTV. Price affects customer quality, not just acquisition volume.

---

## B2B vs. B2C Pricing Differences

| Dimension | B2B | B2C |
|---|---|---|
| **Decision maker** | Committee (economic, technical, user) | Individual |
| **Price sensitivity** | Lower — ROI justification expected | Higher — personal spend, emotional |
| **Purchase process** | Procurement, contract, legal | Credit card, self-serve |
| **Price visibility** | Often hidden (custom quotes) | Typically public |
| **Discount dynamics** | Negotiated; multi-year deals | Promotional; seasonal |
| **Packaging** | Solution-based; outcomes-focused | Feature-based; tier simplicity |
| **Trial model** | POC, pilot, limited rollout | Free trial, freemium |
| **Annual vs. monthly** | Annual preferred (stability) | Monthly preferred (flexibility) |

---

## Key Takeaways

- **Price to value, not to cost.** The most defensible pricing is rooted in the economic outcome you deliver.
- **Value density is the true metric.** High-density offers generate loyalty, referrals, and expansion — not just revenue.
- **Framing changes price perception** — the same number feels different depending on context, comparison, and unit of measure.
- **Three tiers, maximum.** Choice architecture determines tier uptake more than the features in each tier.
- **Price testing is non-negotiable.** Untested pricing is guesswork with a spreadsheet; test it live.
- **B2B and B2C are different games.** Bring the right pricing playbook to the right market.

---

## Recommended Resources

- *Monetizing Innovation* — Madhavan Ramaswamy & Georg Tacke
- *The Strategy and Tactics of Pricing* — Thomas Nagle & Georg Müller
- *Confessions of the Pricing Man* — Hermann Simon
- ProfitWell Recur — SaaS pricing benchmarks and research
- Patrick Campbell's pricing research (Paddle/ProfitWell blog)
