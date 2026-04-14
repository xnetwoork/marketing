# Part 49: Experimentation OS — A/B and Multivariate Governance

## Learning Objectives
- Build an organizational culture where experimentation is the default decision-making mechanism
- Design statistically valid A/B tests with proper hypothesis formation
- Apply multivariate testing for complex optimization problems
- Prioritize experiments systematically using ICE and PIE scoring
- Avoid the most common testing mistakes that produce false results
- Scale experimentation programs across marketing and product teams

---

## Why an Experimentation OS?

Most marketing decisions are made on intuition, precedent, or seniority. The result: teams repeat the same strategies, miss opportunities hidden in data, and can't explain why things work when they do.

An **Experimentation OS** is the combination of culture, process, tools, and governance that makes testing the default answer to "which is better?" Instead of debating whether a red CTA button outperforms green, you test it. Instead of assuming a longer landing page converts better, you measure it.

> **Real-world benchmark**: Companies with mature experimentation programs—Amazon, Netflix, Booking.com—run thousands of tests per year. Booking.com attributes much of its conversion dominance to a culture where every team member can propose, run, and learn from experiments.

---

## A/B Test Fundamentals

### The Anatomy of a Valid Test

**1. Hypothesis**
A testable, falsifiable statement: *"Changing the CTA copy from 'Get Started' to 'Start Free Trial' will increase click-through rate because it clarifies the offer's risk-free nature."*

A strong hypothesis includes:
- **What** you're changing
- **What outcome** you expect
- **Why** (the mechanism)

**2. Control vs Variant**
- **Control**: current experience (A)
- **Variant**: modified experience (B)
- Never test more than one change per A/B test; otherwise you can't attribute the result

**3. Statistical Significance**
- Standard threshold: **95% confidence** (p < 0.05)
- Means: there's only a 5% probability the observed difference is due to chance
- **Do not interpret results below this threshold as wins**

**4. Statistical Power**
- Typical target: **80% power**
- Power = probability of detecting a real effect when one exists
- Low power → high false negative rate (you miss real wins)

### Sample Size Calculation
Use a calculator (Evan Miller's tool, AB Testguide) before launching:

| Baseline CVR | Minimum Detectable Effect | Required Visitors (per variant) |
|-------------|--------------------------|--------------------------------|
| 2% | 20% relative improvement | ~19,000 |
| 5% | 10% relative improvement | ~31,000 |
| 10% | 10% relative improvement | ~15,000 |

If you don't have the traffic, **don't run the test**—underpowered tests produce unreliable results.

---

## Multivariate Testing (MVT)

MVT tests multiple variables simultaneously, measuring the effect of each and their interactions.

**Example**: Testing headline (2 variants) × CTA copy (2 variants) × hero image (2 variants) = 8 combinations

### When to Use MVT
- You have very high traffic (100K+ monthly visitors to the page)
- You need to understand interaction effects (does headline A work better with CTA A or CTA B?)
- You're optimizing a mature, high-stakes page

### When NOT to Use MVT
- Low-traffic pages (results take months; noise dominates)
- Early-stage products (run A/B tests to find large gains first)
- When you want clear causal attribution of which element drove change

**Tools**: Google Optimize (sunset 2023, migrate to GA4 + Firebase), VWO, Optimizely, Adobe Target

---

## Test Prioritization Frameworks

You'll always have more experiment ideas than capacity. Prioritize rigorously.

### ICE Scoring
Rate each experiment 1–10 on three dimensions:

| Dimension | Question |
|-----------|---------|
| **Impact** | How much will this move the needle if it works? |
| **Confidence** | How sure are we the hypothesis is correct? |
| **Ease** | How easy/fast is this to implement? |

**ICE Score** = (Impact + Confidence + Ease) ÷ 3

### PIE Scoring
| Dimension | Question |
|-----------|---------|
| **Potential** | How much improvement is possible on this page/flow? |
| **Importance** | How much traffic/revenue does this area represent? |
| **Ease** | How easy is implementation? |

**PIE Score** = (Potential + Importance + Ease) ÷ 3

### Prioritization in Practice
- Maintain a backlog of experiment ideas (use Notion, Airtable, or Linear)
- Score every idea before adding to queue
- Run weekly backlog grooming: score new ideas, archive stale ones
- Assign experiment owners with clear deadlines

---

## Experiment Documentation and Knowledge Management

Every experiment should be documented, regardless of outcome. This is the **institutional memory** of your experimentation program.

### Experiment Brief Template
```
Title: [Descriptive experiment name]
Date: [Start – End]
Owner: [Name]
Hypothesis: [If we change X, then Y will happen because Z]
Primary Metric: [e.g., Sign-up CVR]
Secondary Metrics: [e.g., Bounce rate, Session duration]
Traffic Split: [50/50 or segmented]
Sample Size Required: [Pre-calculated]
Results: [Lift %, confidence level, p-value]
Decision: [Ship / Iterate / Abandon]
Learning: [What did we learn regardless of outcome?]
```

### Knowledge Management
- Store all experiment results in a shared, searchable repository
- Tag by page, funnel stage, hypothesis type, and outcome
- Review past tests before running new ones to avoid repeating failed ideas
- Run quarterly "experimentation retrospectives" to identify patterns in what works

---

## Common Testing Mistakes

### 1. Peeking (Stopping Early)
**Problem**: Checking results daily and stopping when you hit significance inflates false positive rates dramatically. At 95% confidence, "peeking" can push actual false positive rates to 30%+.
**Fix**: Pre-commit to a sample size. Don't look at significance until you've hit it.

### 2. Running Underpowered Tests
**Problem**: Not enough traffic → can't detect real effects → learning nothing.
**Fix**: Calculate sample size before launch. If traffic is insufficient, test on higher-traffic pages or wait.

### 3. Testing Too Many Variants
**Problem**: 5-way tests require 5× the traffic and are harder to interpret.
**Fix**: Test one or two variants at a time. Run sequential tests if needed.

### 4. Novelty Effect
**Problem**: Users respond to change itself, not the quality of the change. Early results look good; performance degrades over time.
**Fix**: Run tests for at least 2 full business cycles (typically 2 weeks minimum).

### 5. Ignoring Segment-Level Results
**Problem**: Aggregate results hide heterogeneous effects. A change that hurts mobile users but helps desktop users may look neutral overall.
**Fix**: Always segment results by device, traffic source, and user type.

### 6. Shipping "Not Significant" Results
**Problem**: Teams declare a winner because the trend looks positive, even without statistical significance.
**Fix**: Pre-define significance threshold. A result at 80% confidence is not a winner.

---

## Scaling Experimentation Programs

### Phase 1: Foundation (1–3 tests/month)
- Pick one CRO tool (VWO or Optimizely)
- Establish hypothesis format and documentation template
- Designate an experimentation owner
- Focus on high-traffic, high-impact pages (home, pricing, sign-up)

### Phase 2: Momentum (10–20 tests/month)
- Train all channel owners to write test hypotheses
- Integrate experiment results into weekly marketing reviews
- Build out backlog scoring process
- Share wins and learnings in team Slack channel

### Phase 3: Scale (50+ tests/month)
- Dedicated experimentation team or CRO specialist
- Statistical infrastructure in data warehouse
- Feature flagging system (LaunchDarkly, Statsig, Growthbook)
- Experimentation integrated into product roadmap sprints

---

## Integrating Experimentation into Workflows

### Marketing Workflow Integration
- **Campaign briefs**: include a measurement plan and hypothesis
- **Landing page launches**: always paired with a baseline test
- **Email programs**: test subject lines, send times, and sequences

### Product Workflow Integration
- **Sprint planning**: dedicate 20% of sprint capacity to experiment follow-through
- **Roadmap items**: "we think this feature will improve activation by X%—here's how we'll test it"
- **Shared test calendar**: prevent conflicting experiments from polluting results

---

## Key Takeaways

- **Culture first, tools second**: experimentation works when failure is safe and learning is celebrated
- **Underpowered tests are worse than no tests**—they produce false confidence
- **Peeking is the #1 statistical error** in marketing experimentation
- **Document everything**: the learning from a failed test is often more valuable than the result
- **Prioritize ruthlessly** with ICE/PIE scoring; not all experiments are equal
- **Scaling experimentation** requires process and tooling, not just more ideas

---

## Actionable Next Steps

1. **This week**: Pick one high-traffic page and write three testable hypotheses using the hypothesis format
2. **This month**: Run your first properly powered A/B test with pre-committed sample size and success criteria
3. **This quarter**: Build an experiment backlog with ICE scores and run a cadence of 2–4 tests/month
4. **This year**: Establish an experimentation repository and run a quarterly retrospective on test learnings
